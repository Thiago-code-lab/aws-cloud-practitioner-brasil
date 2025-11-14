# 03 - Segurança e Conformidade

Este módulo cobre os serviços e conceitos essenciais para proteger sua conta e seus recursos na AWS. É um dos pilares da certificação.

## Tópicos Principais

### 1. Modelo de Responsabilidade Compartilhada
- Define o que a AWS protege ("Segurança da Nuvem") e o que o cliente protege ("Segurança na Nuvem").
- **AWS:** Hardware, Data Centers, Rede Global, Serviços gerenciados (S3, RDS).
- **Cliente:** Dados do cliente, Criptografia (dos dados), Configuração de IAM, Patches de SO (no EC2), Configuração de Security Groups.

### 2. IAM (Identity and Access Management)
- O "porteiro" da AWS. Controla "quem" (identidade) pode fazer "o quê" (permissão).
- **Users (Usuários):** Entidades (pessoas, serviços).
- **Groups (Grupos):** Coleções de usuários para facilitar o gerenciamento de permissões.
- **Policies (Políticas):** Documentos JSON que definem as permissões (Allow/Deny).
- **Roles (Funções):** A forma mais segura. Permissões temporárias que são "assumidas" por usuários ou serviços (ex: uma instância EC2 assumindo uma Role para acessar o S3).
- **MFA (Multi-Factor Authentication):** Camada extra de segurança essencial para o login, especialmente para o usuário Root.

### 3. Proteção de Rede (VPC)
- **VPC (Virtual Private Cloud):** Sua rede virtual privada e isolada na AWS.
- **Security Groups (SGs):**
  - Firewall da instância (Nível do EC2).
  - **Stateful:** Se o tráfego de entrada é permitido, o de saída (resposta) é automaticamente permitido.
- **NACLs (Network Access Control Lists):**
  - Firewall da sub-rede (Nível da VPC).
  - **Stateless:** Regras de entrada e saída devem ser configuradas explicitamente.

### 4. Serviços de Proteção e Detecção
- **AWS Shield:**
  - Proteção contra ataques **DDoS** (Distributed Denial of Service).
  - **Shield Standard:** Gratuito e automático.
  - **Shield Advanced:** Pago, para proteção avançada.
- **AWS WAF (Web Application Firewall):**
  - Protege aplicações web (Camada 7) contra ataques comuns como **SQL Injection** e **Cross-Site Scripting (XSS)**.
- **AWS GuardDuty:**
  - "Detetive" inteligente da conta. Usa Machine Learning para detectar comportamento malicioso (ex: mineração de criptomoedas, acesso de IPs suspeitos).

### 5. Auditoria, Monitoramento e Conformidade
- **AWS CloudTrail:**
  - Auditoria. Responde: "**Quem fez o quê?**". Loga todas as chamadas de API na sua conta.
- **AWS CloudWatch:**
  - Monitoramento. Responde: "**Como estão minhas aplicações?**". Coleta métricas (CPU, Rede), logs de aplicação e permite criar alarmes.
- **AWS Artifact:**
  - Portal de documentos. Onde você baixa os **relatórios de conformidade** da AWS (ISO, PCI-DSS, etc.) para seus auditores.