# 1. Introdução à Computação em Nuvem (Cloud Computing)

## 1.1. O que é Computação em Nuvem?
- **Definição:** Entrega de recursos de TI (servidores, armazenamento, bancos de dados, redes e software) sob demanda pela internet, com pagamento conforme o uso.
- **Analogia simples:** Em vez de comprar um gerador (data center próprio), você “liga na tomada” de uma concessionária (nuvem) e paga só pelo que consome.
- **Características-chave:** Elasticidade, escalabilidade, self-service, medição de uso, ampla rede, disponibilidade global.

## 1.2. Modelos de Implantação da Nuvem
- **Nuvem Pública:** Infraestrutura pertence ao provedor (ex: AWS). Recursos compartilhados entre clientes, com isolamento lógico. Exemplos: Hospedar aplicações no Amazon EC2, S3, RDS.
- **Nuvem Privada:** Infraestrutura dedicada a uma única organização, on‑premises ou hospedada por terceiros. Exemplos: VMware privado, AWS Outposts para trazer serviços AWS ao seu data center.
- **Nuvem Híbrida:** Combina nuvem pública e privada/on‑premises com orquestração entre ambientes. Exemplos: Workloads divididos entre on‑prem e AWS; uso de VPN/Direct Connect.

## 1.3. Modelos de Serviço da Nuvem
- **IaaS (Infrastructure as a Service):**
  - Definição: Infraestrutura básica (computação, rede, armazenamento) como serviço.
  - Exemplos: Amazon EC2, Amazon EBS, Amazon VPC.
  - Responsabilidades:
    - Cliente: SO convidado, runtime, dados, apps, patches do SO, configuração de rede de instância.
    - AWS: Hardware, virtualização, datacenter físico, hypervisor.
- **PaaS (Platform as a Service):**
  - Definição: Plataforma gerenciada para deploy de apps sem gerenciar servidores/OS.
  - Exemplos: AWS Elastic Beanstalk, AWS Fargate, AWS Lambda (muitas vezes categorizado como FaaS).
  - Responsabilidades:
    - Cliente: Código, dependências, configurações de app.
    - AWS: Infra, SO, escalabilidade automática (em muitos casos), orquestração.
- **SaaS (Software as a Service):**
  - Definição: Aplicações completas entregues via web.
  - Exemplos: Gmail, Salesforce; no ecossistema AWS, apps de parceiros no AWS Marketplace.
  - Responsabilidades:
    - Cliente: Configurações de uso, dados, usuários.
    - Provedor: Aplicação, plataforma e infraestrutura subjacente.

## 1.4. Vantagens da Computação em Nuvem (6 da AWS)
- **Trocar CapEx por OpEx:** Sem grandes investimentos iniciais; paga‑se pelo uso.
- **Economias de escala:** Provedores repassam custos menores por volume.
- **Parar de adivinhar capacidade:** Escala para cima/baixo conforme a demanda.
- **Aumentar velocidade e agilidade:** Provisionamento em minutos, experimentação rápida.
- **Parar de manter data centers:** Reduz esforço em infraestrutura física e operação.
- **Tornar‑se global em minutos:** Implantar em múltiplas regiões rapidamente.

---

### Recomendações de Estudo (CLF-C02)
- **Responsabilidade compartilhada:** O que você gerencia em IaaS vs PaaS vs SaaS.
- **Modelos de implantação:** Quando usar público, privado ou híbrido.
- **Benefícios-chave:** Fixar as 6 vantagens e exemplos práticos.