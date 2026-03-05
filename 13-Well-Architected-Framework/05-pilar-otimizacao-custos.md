# 💸 Pilar: Otimização de Custos

## 📌 O que é?
É o pilar que garante melhor relação entre custo e valor de negócio usando práticas de FinOps e consumo eficiente.

## 🧠 Analogia Simples
É a gestão financeira de uma empresa: orçamento, acompanhamento e corte de desperdícios recorrentes.

## 🏗️ Como funciona
Princípios: consumo sob demanda, medição de eficiência, alocação de despesas e governança financeira contínua.

```text
Medição de custo -> Rightsizing -> Compromissos (SP/RI) -> Economia sustentável
```

## 🎯 Casos de Uso Comuns
- Reduzir custo de instâncias subutilizadas
- Criar alertas com Budgets
- Aplicar Savings Plans em cargas estáveis

## 💰 Modelo de Preço
Sem custo do pilar; resultados vêm da otimização dos custos AWS existentes.

## ⚙️ Comandos CLI Úteis
```bash
aws ce get-cost-and-usage --time-period Start=2026-03-01,End=2026-03-31 --granularity MONTHLY --metrics UnblendedCost
aws budgets describe-budgets --account-id 123456789012
```

## 🔗 Links Oficiais
- https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/
- https://aws.amazon.com/aws-cost-management/
