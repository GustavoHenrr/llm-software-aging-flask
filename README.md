# Envelhecimento de Software em Aplicações Flask Geradas por LLM

Este repositório contém os artefatos, scripts e a configuração experimental utilizados no estudo sobre **envelhecimento de software em aplicações web Python/Flask geradas por LLMs**.

O projeto investiga se aplicações web geradas automaticamente por Large Language Models (LLMs) apresentam sinais de envelhecimento de software durante execuções prolongadas, como aumento progressivo no consumo de memória e degradação no tempo de resposta.

## Objetivo

O principal objetivo deste projeto é analisar se sistemas gerados por LLMs também estão sujeitos aos efeitos de envelhecimento de software comumente observados em softwares desenvolvidos de forma tradicional.

Mais especificamente, o estudo avalia:
- mudanças progressivas no **uso de memória**
- variações no **tempo de resposta**
- comportamento do **uso de CPU**
- mudanças no **número de processos em execução**

## Contexto da Pesquisa

Estudos recentes sobre código gerado por LLMs têm se concentrado principalmente em aspectos como corretude, qualidade, segurança e eficiência. No entanto, ainda há evidências limitadas sobre se aplicações geradas por LLMs são propensas a apresentar **sintomas de envelhecimento de software** durante execuções prolongadas.

Para investigar essa lacuna, este repositório disponibiliza o material utilizado para executar experimentos controlados de longa duração com aplicações web geradas automaticamente.

## Desenho Experimental

Os experimentos foram conduzidos com aplicações web Python/Flask geradas a partir de prompts em linguagem natural.

Cada aplicação foi executada continuamente por **48 horas**, enquanto métricas relacionadas ao desempenho e ao uso de recursos foram coletadas.

### Métricas monitoradas
- Consumo de memória
- Utilização de CPU
- Número de processos
- Tempo de resposta das requisições

### Análise estatística
Para identificar tendências nas séries temporais coletadas, o estudo aplica:
- **Teste de tendência de Mann-Kendall**
- **Estimativa da inclinação de Sen (Sen’s slope)**

Esses métodos são utilizados para verificar se há degradação progressiva estatisticamente significativa ao longo do tempo.

## Estrutura do Repositório

Uma estrutura sugerida para o repositório é:

```bash
.
├── apps/                  # Aplicações Flask geradas
├── scripts/               # Scripts de automação, monitoramento e análise
├── data/
│   ├── raw/               # Métricas coletadas em formato bruto
│   └── processed/         # Dados processados para análise
├── results/               # Figuras, tabelas e saídas geradas
├── notebooks/             # Notebooks de análise exploratória e estatística
├── docs/                  # Materiais do artigo ou documentação
├── requirements.txt       # Dependências Python
└── README.md
