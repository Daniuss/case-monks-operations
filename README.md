# Case Técnico — Estágio Operations (Monks)

**Candidato:** Gabriel Danius  
**Data:** Abril 2026

---

## Como abordei o problema

Recebi uma planilha com 413 linhas de oportunidades comerciais com dados fictícios, baseados na estrutura de pipeline da Monks. O trabalho foi dividido em três etapas:

### Etapa 1 — Limpeza dos dados
Comecei explorando os campos categóricos (Stage, Lead_Source, Lead_Office) e comparando com os valores de referência do case brief. Identifiquei erros de grafia, formatação inconsistente nos valores numéricos e divergências entre o campo Amount e a soma dos produtos (Total_Product_Amount). Cada problema foi registrado em um log e corrigido no código. Também criei a coluna Lead_Source_Category, agrupando os 17 valores brutos de Lead_Source em 6 categorias conforme as instruções do case.

### Etapa 2 — Análise dos dados
Com os dados limpos, filtrei apenas as oportunidades no escopo (Project - Competitive, Project - Not Competitive e Change Order/Upsell), resultando em 203 oportunidades únicas. Calculei as métricas solicitadas e gerei um relatório HTML com 10 gráficos e tabelas interativos usando Chart.js.

### Etapa 3 — Apresentação
Selecionei os insights mais relevantes da análise e montei uma apresentação em PDF com 8 slides, incluindo contexto, erros encontrados, principais achados e recomendações de processo.

### Ferramentas utilizadas
- **Python** — pandas para manipulação e análise dos dados
- **Google Colab** — ambiente para execução do código
- **Chart.js** — gráficos interativos no relatório HTML
- **Claude (IA)** — assistente de IA para estruturação do código, validação da lógica e geração dos relatórios

---

## Resumo das entregas

| Arquivo | Descrição |
|---------|-----------|
| `opps_corrigido.xlsx` | Planilha com os dados limpos e a coluna Lead_Source_Category adicionada |
| `relatorio_erros.html` | Relatório com os 181 problemas identificados, organizados por categoria, com exemplos e correções aplicadas |
| `analise.html` | Relatório com 10 gráficos e tabelas interativos sobre o pipeline comercial |
| `apresentacao.pdf` | Apresentação de 8 slides com contexto, erros, insights e recomendações |
| `Monk_Case.ipynb` | Notebook com todo o código utilizado, documentado passo a passo |

---

## Números principais

- **413 linhas** auditadas, **261 oportunidades** únicas
- **181 problemas** identificados em **5 categorias**
- **203 oportunidades** no escopo da análise (305 linhas)
- **67 oportunidades** Closed Won = **R$ 27.2M** de receita em 2026
- **136 oportunidades** em pipeline aberto
