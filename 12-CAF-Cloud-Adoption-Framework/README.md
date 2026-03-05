# 🧭 AWS Cloud Adoption Framework (CAF)

## 📌 O que é?
O AWS CAF é um framework de transformação em nuvem que organiza estratégia, pessoas, governança, plataforma, segurança e operações. Ele ajuda empresas a sair do estado atual para um modelo cloud escalável com menor risco.

## 🧠 Analogia Simples
Pense no CAF como o plano diretor de uma cidade: não basta construir prédios, é preciso organizar trânsito, segurança, orçamento e serviços públicos para tudo funcionar.

## 🏗️ Como funciona
O framework combina fases de execução com perspectivas de capacidade organizacional.

```text
Envision -> Align -> Launch -> Scale
		|         |         |        |
	Estratégia  Gaps     Pilotos  Escala

Perspectivas: Business | People | Governance | Platform | Security | Operations
```

## 🎯 Casos de Uso Comuns
- Planejar jornada de migração corporativa para AWS
- Estruturar programa de transformação digital com metas claras
- Reduzir riscos de adoção cloud por falta de governança

## 💰 Modelo de Preço
O CAF em si não é cobrado. O custo vem da implementação das capacidades e dos serviços AWS usados na transformação.

## ⚙️ Comandos CLI Úteis
```bash
aws organizations list-accounts
aws configservice describe-config-rules
aws ce get-cost-and-usage --time-period Start=2026-03-01,End=2026-03-31 --granularity MONTHLY --metrics UnblendedCost
```

## 🔗 Links Oficiais
- https://docs.aws.amazon.com/whitepapers/latest/aws-caf/
- https://aws.amazon.com/cloud-adoption-framework/
