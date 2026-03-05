# 🚀 Pilar: Eficiência de Desempenho

## 📌 O que é?
Busca o melhor uso de recursos para atender requisitos de desempenho com elasticidade e baixa latência.

## 🧠 Analogia Simples
É escolher veículo e rota ideais para cada entrega, ajustando em tempo real conforme trânsito.

## 🏗️ Como funciona
Princípios: seleção correta de recursos, revisão contínua, monitoramento e trade-offs arquiteturais.

```text
Medição de desempenho -> Ajuste de arquitetura -> Melhor latência/custo
```

## 🎯 Casos de Uso Comuns
- Uso de CloudFront para entrega global
- Caching com ElastiCache
- Escolha de instâncias adequadas por workload

## 💰 Modelo de Preço
Boas decisões de performance evitam overprovisioning e reduzem custo.

## ⚙️ Comandos CLI Úteis
```bash
aws cloudfront list-distributions
aws ec2 describe-instance-types --instance-types t3.micro c7g.large
```

## 🔗 Links Oficiais
- https://docs.aws.amazon.com/wellarchitected/latest/performance-efficiency-pillar/
- https://aws.amazon.com/products/compute/
