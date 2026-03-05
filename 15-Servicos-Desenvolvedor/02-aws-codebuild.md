# AWS CodeBuild

## O que é
Serviço de build e teste contínuo totalmente gerenciado.

## Quando usar
- Compilar, testar e empacotar aplicações em pipeline CI/CD.
- Executar builds sob demanda sem gerenciar servidores.

## Pontos de prova
- Escala automática por job de build.
- Configuração central via buildspec.

## CLI útil
```bash
aws codebuild list-projects
aws codebuild batch-get-projects --names MeuProjeto
```
