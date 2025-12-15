# 05 – Redes e Conectividade

Este módulo aborda os conceitos e serviços de redes na AWS, explicando como os recursos se comunicam entre si, como garantir **segurança**, **baixa latência**, **alta disponibilidade** e como integrar a nuvem com ambientes **on-premises** e aplicações globais.  

<br>

## Tópicos Principais

---

## 1. Conceitos Fundamentais de Rede na AWS

### Região (Region)

Uma região é uma área geográfica onde a AWS possui data centers.  
Cada região é isolada das demais, permitindo resiliência, isolamento de falhas e atendimento a requisitos legais.

**Serve para:**
- Reduzir latência para usuários
- Atender compliance e leis locais
- Isolar ambientes críticos

---

### Zona de Disponibilidade (Availability Zone – AZ)

São data centers fisicamente separados dentro de uma região, com energia, rede e refrigeração independentes.

**Servem para:**
- Alta disponibilidade
- Tolerância a falhas
- Arquiteturas resilientes

📌 Boas práticas sempre distribuem recursos em **múltiplas AZs**.

---

### Edge Locations

São pontos de presença globais usados por serviços como **Amazon CloudFront**.

**Servem para:**
- Entregar conteúdo mais próximo do usuário
- Reduzir latência
- Melhorar desempenho global

📌 Edge Locations **não são regiões nem AZs**.

---

## 2. VPC (Virtual Private Cloud)

A VPC é uma rede virtual privada e isolada, criada e gerenciada pelo cliente.

Ela permite:
- Definir endereçamento IP (CIDR)
- Criar subnets
- Configurar rotas
- Controlar tráfego
- Integrar com internet e on-premises

📌 Toda aplicação na AWS roda dentro de uma VPC.

---

### Subnets

Subnets são divisões da VPC e sempre pertencem a uma única AZ.

**Tipos:**

- **Subnet pública**  
  Possui rota para Internet Gateway. Usada para ALB público, NAT Gateway e bastion host.

- **Subnet privada**  
  Não possui rota direta para a internet. Usada para aplicações e bancos de dados.

**Servem para:**
- Separar camadas da aplicação
- Aumentar segurança
- Organizar arquitetura

📌 Uma subnet só é pública se **a rota permitir**.

---

## 3. Controle de Tráfego e Rotas

### Route Tables

Definem para onde o tráfego de rede é encaminhado.

**Servem para:**
- Direcionar tráfego para IGW, NAT Gateway, VPN, Transit Gateway ou VPC Peering
- Controlar comunicação entre redes

📌 Toda subnet deve estar associada a uma Route Table.

---

### Internet Gateway (IGW)

Permite comunicação entre a VPC e a internet.

**Serve para:**
- Tornar recursos acessíveis publicamente
- Permitir saída de tráfego para a internet

📌 O IGW não é firewall, apenas conectividade.

---

### NAT Gateway

Permite que recursos em subnets privadas acessem a internet sem receber conexões de entrada.

**Serve para:**
- Atualizações de sistema
- Acesso a APIs externas
- Download de dependências

📌 “Acesso à internet sem exposição” → **NAT Gateway**

---

## 4. Segurança de Rede (Camada de Rede)

### Security Groups (SG)

Firewall aplicado no nível do recurso (EC2, ALB, RDS).

- Stateful
- Apenas regras **ALLOW** (permissão)
- Controle fino de acesso

---

### Network ACL (NACL)

Firewall aplicado no nível da subnet.

- Stateless
- Regras **ALLOW** e **DENY**
- Avaliação por ordem numérica

📌 **Prova:**  
- SG → instância  
- NACL → subnet

---

## 5. Comunicação entre Redes AWS

### VPC Peering

Conecta duas VPCs de forma privada.

- Comunicação direta
- Não transitivo
- Escala mal

---

### AWS Transit Gateway

Hub central de conectividade.

- Conecta múltiplas VPCs, VPNs e Direct Connect
- Roteamento transitivo
- Altamente escalável

---

### VPC Endpoints

Permitem acesso privado a serviços AWS sem usar a internet.

**Tipos:**
- **Gateway Endpoint** → Amazon S3 e DynamoDB
- **Interface Endpoint (PrivateLink)** → outros serviços AWS e SaaS

---

### AWS PrivateLink

Permite a exposição de serviços específicos entre VPCs de forma privada.

📌 PrivateLink expõe **serviços**, não redes inteiras.

---

## 6. Conectividade Híbrida (On-Premises ↔ AWS)

### AWS VPN (Site-to-Site)

Conexão criptografada via internet.

- Menor custo
- Latência variável
- Boa para ambientes híbridos iniciais

---

### AWS Direct Connect

Conexão física dedicada.

- Baixa latência
- Alta previsibilidade
- Ambientes críticos

📌 “Menor latência possível” → **Direct Connect**

---

## 7. DNS, Roteamento e Alta Disponibilidade

### Amazon Route 53

Serviço de DNS gerenciado e altamente disponível da AWS.

**Serve para:**
- Traduzir nomes de domínio em endereços IP
- Roteamento inteligente de tráfego
- Alta disponibilidade de aplicações

**Principais funcionalidades:**
- DNS público e privado
- Health Checks
- Failover automático
- Roteamento geográfico

**Políticas de roteamento (muito cobradas na prova):**
- **Simple** – Um único recurso
- **Weighted** – Divide tráfego por peso
- **Latency-based** – Menor latência para o usuário
- **Failover** – Ativo/passivo
- **Geolocation** – Baseado na localização do usuário

📌 Route 53 é **global**, não regional.

---

## 8. Distribuição de Conteúdo e Melhora no Desempenho

### Amazon CloudFront

Rede de entrega de conteúdo (CDN) global da AWS que distribui conteúdo via Edge Locations.

- Cache de conteúdo
- Redução de latência
- Integração com WAF e Shield

---

### AWS Global Accelerator

Aceleração de tráfego dinâmico melhorando o desempenho e disponibilidade de aplicações globais.

- IPs Anycast fixos
- Suporte a TCP/UDP
- Ideal para APIs e aplicações em tempo real

📌 **CloudFront** → conteúdo  
📌 **Global Accelerator** → tráfego dinâmico

📌**Prova**:
- Melhora trafego para QUALQUER tipo de app: Global Accelerator
- Conteúdo estático: CloudFront
