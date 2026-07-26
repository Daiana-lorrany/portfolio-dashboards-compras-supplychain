#  Portfólio de Analytics em Compras & Supply Chain

## Dashboard 1: Performance de Compras

> Parte 1 de uma série de dashboards em Power BI aplicados à área de Compras e Supply Chain — próximos: Supplier Scorecard, Gestão de Estoque/MRP, Redução de Desperdício.

### Objetivo

Este dashboard responde à pergunta: **"Onde estamos perdendo dinheiro na cadeia de suprimentos?"**

Construído para simular a rotina de um analista de Strategic Sourcing, consolidando spend, savings, prazos de entrega e concentração de risco de fornecedores em uma visão executiva única.

### Principais KPIs

- **Spend Total** e **Savings Realizado** — com variação Mês a Mês e acumulado YTD
- **% OTIF** (On Time In Full) — pontualidade e integridade das entregas
- **% Compras Emergenciais** — indicador de planejamento vs. urgência
- **Lead Time Médio** — tempo entre pedido e entrega
- **% Spend concentrado nos Top 5 Fornecedores** — indicador de risco de dependência

### Estrutura do modelo de dados

Modelo em esquema estrela:
- `FatoCompras` (tabela fato — 700 pedidos)
- `DimFornecedor`, `DimItem`, `DimCategoria`, `DimCalendario` (dimensões)

16 medidas DAX customizadas, incluindo classificação ABC calculada, ranking dinâmico de fornecedores e medidas de concentração de risco com tratamento correto de contexto de filtro.

###  Funcionalidades

- 3 páginas: Visão Executiva, Diagnóstico de Risco, Detalhe de Pedidos
- Navegação entre páginas via botões customizados
- Tooltip customizado com contexto por fornecedor
- Drill-through para detalhamento de pedidos por fornecedor
- Tema visual customizado (paleta azul petróleo) com cabeçalhos e cartões formatados

### Ferramentas

Power BI Desktop · DAX · Modelagem de dados (esquema estrela) · Power Query

### Nota sobre os dados

Os dados utilizados são **fictícios**, gerados para fins de demonstração — não representam informações reais de nenhuma empresa.

---
**Autora:** Daiana Tavares da Costa
**Área:** Compras Estratégicas & Supply Chain
