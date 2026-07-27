#  Portfólio de Analytics em Compras & Supply Chain

## Dashboard 2: Supplier Scorecard (Gestão de Fornecedores)

> Parte 2 de uma série de dashboards em Power BI aplicados à área de Compras e Supply Chain - próximos: Gestão de Estoque/MRP, Redução de Desperdício.

---

## 📁 Dashboards do Portfólio

| # | Dashboard | Status |
|---|---|---|
| 1 | [Performance de Compras](./DASH%20FINAL) | ✅ Publicado |
| 2 | [Supplier Scorecard](./dashboard-2-supplier-scorecard) | ✅ Publicado |
| 3 | Gestão de Estoque/MRP | 🔜 Em breve |
| 4 | Redução de Desperdício | 🔜 Em breve |
### Objetivo

Este dashboard responde à pergunta: **"Quais fornecedores merecem continuar, quais precisam de atenção, e quais representam risco?"**

Construído para simular a rotina de avaliação e homologação de fornecedores, cruzando notas de qualidade, prazo, preço e risco em um scorecard executivo.

### Principais KPIs

- **Nota Geral do Fornecedor** - média ponderada de Qualidade, Prazo, Preço e Risco
- **% Fornecedores Estratégicos** - proporção classificada como nota ≥ 8
- **Total de Não Conformidades** - ocorrências registradas no período
- **Classificação por fornecedor** - Estratégico / Aprovado / Em Observação / Crítico

### Estrutura do modelo de dados

- `FatoAvaliacaoFornecedor` (tabela fato — 150 avaliações trimestrais)
- `DimFornecedor`, `DimCalendario` (dimensões)
- `TabelaRadar` (tabela auxiliar para visualização comparativa por critério)

### Funcionalidades

- 2 páginas: Scorecard Geral e Ficha do Fornecedor
- Gráfico de dispersão (Qualidade × Prazo) para identificar fornecedores-problema
- Drill-through por fornecedor com gráfico de radar comparando os 4 critérios
- Histórico de evolução da nota ao longo dos trimestres
- Tema visual escuro customizado, com identidade própria dentro do portfólio

###  Ferramentas

Power BI Desktop · DAX · Modelagem de dados (esquema estrela) · Power Query

###  Nota sobre os dados

Os dados utilizados são **fictícios**, gerados para fins de demonstração — não representam informações reais de nenhuma empresa.

---
**Autora:** Daiana Tavares da Costa
**Área:** Compras Estratégicas & Supply Chain
