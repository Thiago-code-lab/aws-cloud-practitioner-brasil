# 2. Amazon Elastic Compute Cloud (EC2)

Obs.: Baseado no "Amazon EC2 User Guide (ec2-ug.pdf)", simplificado para CLF-C02.

## 2.1. O que é o Amazon EC2?
- **Definição:** Serviço web que fornece capacidade computacional segura e redimensionável na nuvem. Você inicia "instâncias" (máquinas virtuais) conforme a necessidade.
- **Modelo de serviço:** IaaS. Você controla SO convidado, pacotes, firewall de instância (Security Groups) e volumes anexos.

## 2.2. Conceitos Principais do EC2
- **AMIs (Amazon Machine Images):**
  - O que são: Templates de software que incluem SO e, opcionalmente, apps e configurações.
  - Uso: Escolher uma AMI ao iniciar uma instância define o ambiente base.
  - Tipos: AMIs da AWS, de marketplace ou personalizadas.
- **Tipos de Instância (Instance Families):**
  - Ideia: Famílias otimizadas por uso, com tamanhos (vCPU/memória/rede) variados.
  - Famílias comuns:
    - Uso Geral (ex: t, m): equilíbrio CPU/memória/rede.
    - Otimizadas para Computação (ex: c): alto desempenho de CPU.
    - Otimizadas para Memória (ex: r, x): bancos de dados/memória intensiva.
    - Otimizadas para Armazenamento (ex: i, d): I/O de disco alto.
    - Aceleradas (ex: p, g, inf, trn): GPU/ML e aceleradores.
- **Grupos de Segurança (Security Groups):**
  - O que são: Firewalls virtuais em nível de instância.
  - Função: Controlam tráfego de entrada e saída por porta/protocolo/origem-destino.
  - Comportamento: Stateful (respostas são automaticamente permitidas). Por padrão, entrada é negada e saída é permitida.

## 2.3. Modelos de Preços e Compra do EC2
- **On-Demand:** Pagamento por hora/segundo sem compromisso. Ideal para cargas imprevisíveis, testes e desenvolvimento.
- **Savings Plans:** Compromisso de gasto compute (USD/h) por 1 ou 3 anos em troca de descontos. Tipos: Compute Savings Plans (mais flexíveis) e EC2 Instance Savings Plans (amarrados a família/região).
- **Reserved Instances (RIs):** Compromisso por 1 ou 3 anos com desconto. Standard RIs (maior desconto, menos flexíveis) e Convertible RIs (mais flexíveis). Úteis para cargas estáveis.
- **Spot Instances:** Usam capacidade ociosa com grande desconto. Podem ser interrompidas com aviso curto. Boas para workloads tolerantes a interrupção (big data, testes distribuídos, renderização).

## 2.4. Serviços Relacionados (Visão Geral)
- **EBS (Elastic Block Store):** Volumes de armazenamento em bloco persistentes anexados às instâncias. Suporta snapshots no S3.
- **ELB (Elastic Load Balancing):** Distribui tráfego entre múltiplas instâncias/targets. Tipos: ALB (camada 7), NLB (camada 4), GWLB (appliances).
- **Auto Scaling (EC2 Auto Scaling):** Ajusta automaticamente o número de instâncias com base em métricas para desempenho e custo.