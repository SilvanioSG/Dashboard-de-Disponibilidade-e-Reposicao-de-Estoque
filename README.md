# Dashboard de Disponibilidade e Reposição de Estoque

Dashboard analítico desenvolvido em Power BI para monitoramento da saúde do estoque, priorização de reposição e produção, análise de cobertura de pedidos e valorização por Curva ABC. O projeto foi construído a partir de uma base operacional de 100 itens, com foco em decisão executiva e operacional.

**Autor:** Silvanio Gois — Gestor de Operações e Negócios Orientado a Dados

**Links profissionais:**
- Site: https://www.silvaniogois.com.br
- LinkedIn: https://www.linkedin.com/in/silvanio-gois/
- GitHub: https://github.com/SilvanioSG

**Dashboard publicado:** https://app.powerbi.com/view?r=eyJrIjoiMjQwMThiOWQtNTgzMS00NWM2LTg0ODAtZDAzNDFjZjUzYjc4IiwidCI6IjJlYmQyYzU0LWY1ZDMtNGVmYi05ZGE3LWU4Yzk0YmQyMWQzOSJ9

---

## 1. Objetivo do projeto

Construir uma solução analítica capaz de responder, em uma única experiência de navegação, às seguintes perguntas de negócio:

1. Qual é a saúde geral do estoque?
2. Quais itens estão em nível crítico, abaixo do mínimo ou acima do máximo?
3. Quanto é necessário repor e qual a prioridade de reposição?
4. Onde está concentrado o valor financeiro do estoque (Curva ABC)?
5. Como as vendas com e sem carga impactam a cobertura de pedidos?
6. É possível detalhar item a item para ação operacional?

A entrega final contempla seis páginas analíticas, uma capa de navegação, uma base tratada, colunas calculadas, medidas DAX e storytelling executivo orientado a decisão.

---

## 2. Estrutura do dashboard

O relatório é composto por 7 páginas — uma de navegação e seis analíticas — sem redundância de visuais ou métricas entre elas. Cada página responde a uma pergunta específica e alimenta a próxima em uma sequência lógica de leitura.

### Página 0 — Início

Capa de navegação com identidade visual do projeto, links diretos para todas as páginas e resumo do contexto analítico. Funciona como ponto de entrada único para o usuário executivo.

![Página 0 - Início](./pagina0.png)

---

### Página 1 — Visão Executiva

**Objetivo:** responder "Qual é a saúde geral do estoque?" em uma única tela.

**Indicadores principais:** Total de Itens, Estoque Disponível Total, Necessidade de Reposição Total, Valor de Estoque Total, % de Itens Críticos, % de Demanda Coberta e Gap de Demanda.

**Análises entregues:**
- Distribuição de itens por status de estoque (donut).
- Top 10 itens com maior necessidade de reposição (barras horizontais).
- Valor de estoque por classe ABC (colunas).
- Matriz cruzada entre Status de Estoque e Prioridade de Reposição, com quantidade de itens e necessidade total.

![Página 1 - Visão Executiva](./pagina1.png)

---

### Página 2 — Disponibilidade e Cobertura

**Objetivo:** analisar cobertura, posicionamento do estoque frente aos reguladores mínimo e máximo e dias de estoque.

**Indicadores principais:** Cobertura, Dias de Estoque Médio, % de Itens Abaixo do Mínimo, % de Itens Acima do Máximo.

**Análises entregues:**
- Dispersão entre Estoque Disponível e Regulador Mínimo, com cor por status.
- Distribuição de itens por faixa de cobertura de pedidos.
- Comparativo por item entre Estoque Disponível, Regulador Mínimo e Regulador Máximo.
- Top 10 itens com menor cobertura.

![Página 2 - Disponibilidade e Cobertura](./pagina2.png)

---

### Página 3 — Reposição e Produção

**Objetivo:** priorizar o que produzir ou comprar e identificar itens em excesso.

**Indicadores principais:** Necessidade de Reposição Total, Excesso Total de Estoque, Quantidade de Itens Urgentes, Valor Total de Pedidos e Necessidade Líquida.

**Análises entregues:**
- Top 20 itens com maior necessidade de reposição.
- Distribuição da necessidade de reposição por prioridade (treemap).
- Tabela operacional com Item, Descrição, Estoque Disponível, Regulador Mínimo, Necessidade de Reposição e Valor de Pedidos.

![Página 3 - Reposição e Produção](./pagina3.png)

---

### Página 4 — Valorização e Curva ABC

**Objetivo:** entender onde está concentrado o valor financeiro do estoque e quais itens pertencem à Classe A.

**Indicadores principais:** Valor Total do Estoque, Valor Total dos Pedidos, % do Valor da Classe A e Custo Unitário Médio.

**Análises entregues:**
- Diagrama de Pareto dos 20 itens de maior valor de estoque com curva de percentual acumulado.
- Donut de participação do valor por Classe ABC.
- Valor de estoque por status.
- Matriz cruzada entre Classe ABC e Status de Estoque, com valor, quantidade e percentual de itens.

![Página 4 - Valorização e Curva ABC](./pagina4.png)

---

### Página 5 — Pedidos e Cargas

**Objetivo:** comparar vendas com e sem carga e mensurar o impacto da produção na cobertura de pedidos.

**Indicadores principais:** Vendas com Carga, Vendas sem Carga, Cobertura de Cargas com Produção, Cobertura de Cargas sem Produção e Cobertura Média de Pedidos.

**Análises entregues:**
- Dispersão entre Vendas com Carga e Vendas sem Carga, com tamanho proporcional ao valor de pedidos.
- Série comparativa entre cobertura com e sem produção por item.
- Top 10 itens com menor cobertura de pedidos.
- Tabela de desempenho com vendas, coberturas e valor de pedidos.

![Página 5 - Pedidos e Cargas](./pagina5.png)

---

### Página 6 — Detalhamento

**Objetivo:** exploração granular e exportação operacional.

**Análises entregues:**
- Tabela curada com as colunas essenciais para ação: Item, Descrição, Status, Prioridade, Classe ABC, Estoque Físico, Estoque Disponível, Reguladores, Necessidade, Excesso, Cobertura, Valor de Estoque e Valor de Pedidos.
- Formatação condicional em Status, Prioridade e Necessidade de Reposição.
- Cards contextuais no topo que reagem aos filtros da página.
- Slicers por Descrição, Status, Prioridade, Classe ABC e Faixa de Cobertura.

![Página 6 - Detalhamento](./pagina6.png)

---

## 3. Metodologia técnica

### 3.1 Tratamento de dados

A base bruta `DisponibilidadeEstoque.xlsx` foi importada no Power Query e submetida às seguintes etapas de preparação:

- Promoção de cabeçalho e tipagem explícita de colunas.
- Substituição de valores nulos por zero nas colunas numéricas.
- Criação de dimensão `dItem` a partir da desduplicação de `Item` e `Descricao_do_Item`.
- Manutenção da tabela fato `fEstoque` com granularidade de um registro por item.

### 3.2 Modelagem

Modelo em esquema estrela simplificado:

- `fEstoque` (fato) — 1 linha por item.
- `dItem` (dimensão) — relacionamento 1:N com `fEstoque`.
- Tabela `_Medidas` dedicada ao armazenamento de todas as medidas DAX, isolando o cálculo da modelagem.

### 3.3 Colunas calculadas

Foram criadas colunas para enriquecer a análise sem onerar o modelo:

- `Estoque_Total`, `Estoque_Comprometido` e `Estoque_Disponivel_Calc` para validação cruzada com a origem.
- `Status_Estoque` com quatro faixas: Crítico-Negativo, Abaixo do Mínimo, Normal e Acima do Máximo.
- `Prioridade_Reposicao` com quatro níveis: Urgente, Alta, Média e Baixa.
- `Necessidade_Reposicao` e `Excesso_Estoque` calculados a partir dos reguladores.
- `Faixa_Cobertura_Pedidos` com cinco faixas de cobertura.
- `Rank_Valor_Estoque`, `Valor_Acumulado_ABC`, `Percentual_Acumulado_ABC` e `Classe_ABC` para construção da Curva ABC.
- Colunas de ordenação (`Ordem_Status`, `Ordem_Faixa`, `Ordem_Prioridade`, `Ordem_Classe_ABC`) para garantir ordenação correta nos visuais.

### 3.4 Medidas DAX

As medidas foram organizadas em blocos funcionais:

- **Volumetria:** Total de Itens, Quantidade de Itens Urgentes.
- **Saldo:** Estoque Disponível Total, Necessidade de Reposição Total, Excesso Total.
- **Financeiro:** Valor de Estoque Total, Valor de Pedidos Total, Custo Unitário Médio, % do Valor da Classe A.
- **Cobertura:** Cobertura Real, Cobertura de Cargas com e sem Produção, Cobertura Média de Pedidos.
- **Qualidade:** % de Itens Críticos, % de Itens Abaixo do Mínimo, % de Itens Acima do Máximo.
- **Curva ABC dinâmica:** medida de acumulado recalculado sobre o Top N visível, garantindo que o Pareto reflita apenas os itens exibidos.

### 3.5 Decisões analíticas relevantes

- A coluna original `Produzir` foi descartada por ser redundante com `Estoque_Disponivel`; em seu lugar foi implementada a medida `Necessidade_Reposicao`, que respeita o Regulador Mínimo de cada item.
- A métrica de cobertura foi reformulada. A razão direta entre `Estoque_Disponivel` e vendas gera valores negativos e de leitura ambígua, pois o saldo já desconta as vendas. A cobertura passou a ser calculada pela razão entre `Estoque_Total` e o volume vendido, resultando em percentual positivo e interpretável.
- A Curva ABC foi construída por ranking de valor de estoque, com cortes em 80% (Classe A), 95% (Classe B) e 100% (Classe C).
- A página de detalhamento foi curada para conter apenas as colunas com função decisória, evitando o efeito "planilha no Power BI".

---

## 4. Insights extraídos da base

A análise dos 100 itens revelou um cenário de déficit sistêmico de estoque, com as seguintes leituras:

- **74% dos itens estão em estado crítico-negativo**, ou seja, o saldo disponível é insuficiente para cobrir as vendas já comprometidas.
- O **estoque disponível total é de -33.499 unidades**, enquanto a **necessidade de reposição soma 74.678 unidades**.
- A **demanda coberta é de aproximadamente 67%**, indicando que um terço da demanda não possui lastro em estoque.
- **Nenhum item está acima do máximo**, o que elimina a hipótese de excesso e reforça o diagnóstico de déficit.
- A **Curva ABC é fortemente concentrada**: 48 itens (48% do total) respondem por 80% do valor de estoque, sendo classificados como Classe A. Cerca de 80% do valor financeiro está em itens que, em sua maioria, estão em estado crítico.
- As **vendas com carga superam as vendas sem carga** em aproximadamente 17%, o que indica dependência operacional relevante do processo de carga para o escoamento.
- O **valor total de pedidos é de R$ 13,5 milhões**, superando em mais de 50% o valor total de estoque (R$ 8,9 milhões), reforçando a pressão por reposição.

---

## 5. Stack técnica

- **Power BI Desktop** — modelagem, DAX e construção visual.
- **Power Query (M)** — extração, limpeza e transformação.
- **DAX** — colunas calculadas, medidas e inteligência de Curva ABC.
- **Excel** — origem dos dados operacionais.
- **PDF** — exportação do relatório para versionamento no repositório.

---

## 6. Estrutura de arquivos do repositório
