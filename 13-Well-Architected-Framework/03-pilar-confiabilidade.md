# 🧱 Pilar: Confiabilidade

## 📌 O que é?
Trata da capacidade do sistema continuar operando e se recuperar de falhas rapidamente.

## 🧠 Analogia Simples
É um hospital com gerador, redundância e plano de contingência testado.

## 🏗️ Como funciona
Princípios: recuperação automática, testes de falha, escala horizontal e automação de mudanças.

```text
Falha detectada -> Failover/Auto Recovery -> Serviço continua disponível
```

## 🎯 Casos de Uso Comuns
- Multi-AZ para banco de dados
- Auto Scaling para picos de demanda
- Failover DNS com health checks

## 💰 Modelo de Preço
Redundância aumenta custo, mas reduz impacto financeiro de indisponibilidade.

## ⚙️ Comandos CLI Úteis
```bash
aws autoscaling describe-auto-scaling-groups
aws route53 list-health-checks
```

## 🔗 Links Oficiais
- https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/
- https://docs.aws.amazon.com/route53/
