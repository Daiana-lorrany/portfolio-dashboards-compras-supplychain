## Dashboard 2: Supplier Scorecard — Gestão de Fornecedores

Segundo dashboard da série, focado em avaliação e classificação de fornecedores por desempenho.

### Objetivo
Este dashboard responde à pergunta: "Quais fornecedores estão performando bem, e quais representam risco para a operação?" Construído para simular a rotina de avaliação trimestral de fornecedores em Compras Estratégicas, consolidando qualidade, prazo, preço e risco em uma nota geral ponderada.

### Principais KPIs
- **Nota Geral do Fornecedor** — média ponderada de qualidade, prazo, preço e risco
- **% Fornecedores Estratégicos** — sobre o total avaliado
- **Total de Não Conformidades**
- **Quantidade de Fornecedores Avaliados**

### Estrutura do modelo de dados
Modelo em esquema estrela: tabela fato de 150 avaliações trimestrais, dimensões de Fornecedor e Calendário, e uma tabela auxiliar de radar para comparação multi-critério. Classificação do fornecedor em Estratégico, Aprovado, Em Observação ou Crítico, calculada a partir da nota geral ponderada.

### Funcionalidades
- 2 páginas: Scorecard Geral e Ficha do Fornecedor
- Gráfico de dispersão cruzando nota de qualidade, nota de prazo e não conformidades, por fornecedor
- Drill-through com radar comparativo e histórico de evolução da nota por trimestre
- Tema visual escuro customizado, próprio da série

### Ferramentas
Power BI Desktop · DAX · Modelagem de dados (esquema estrela) · Power Query

### Nota sobre os dados
Os dados utilizados são fictícios, gerados para fins de demonstração — não representam informações reais de nenhuma empresa.

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

## Dashboard 3: Gestão de Estoque & MRP

Terceiro dashboard da série, focado em controle de estoque, MRP (inventário rotativo) e redução de desperdício.

### Objetivo
Este dashboard responde à pergunta: "Onde o estoque está em risco, e onde o desperdício está concentrado?" Inspirado na experiência real de gestão de MRP e substituição estratégica de insumos, que resultou em 60% de redução de desperdício de matéria-prima sem impacto na qualidade.

### Principais KPIs
- **Giro de Estoque** e **Cobertura de Estoque (dias)**
- **% SKUs Abaixo do Estoque de Segurança** — indicador de risco de ruptura
- **% Perda sobre Volume Total** — com comparação ano a ano
- **Custo da Perda** por categoria de insumo
- **% SKUs com Fonte Única** — risco de dependência de fornecedor

### Estrutura do modelo de dados
Modelo em esquema estrela: **FatoMovimentacaoEstoque** (tabela fato — 960 registros, 40 SKUs x 24 meses), **DimSKU**, **DimFornecedor**, **DimCategoria**, **DimCalendario** (dimensões). 17 medidas DAX customizadas, incluindo classificação de criticidade por SKU (Alto Risco / Atenção / Estável) e curva ABC por custo de consumo acumulado.

### Funcionalidades
- 3 páginas: Visão Geral, Curva ABC & Criticidade, Ficha do SKU
- Matriz de dispersão cruzando Giro x Cobertura x Custo da Perda, por SKU
- Drill-through para histórico individual de movimentação por SKU
- Tema visual customizado, consistente com os demais dashboards da série

### Ferramentas
Power BI Desktop · DAX · Modelagem de dados (esquema estrela) · Power Query

### Nota sobre os dados
Os dados utilizados são fictícios, gerados para fins de demonstração — não representam informações reais de nenhuma empresa.

---
**Autora:** Daiana Tavares da Costa
**Área:** Compras Estratégicas & Supply Chain
