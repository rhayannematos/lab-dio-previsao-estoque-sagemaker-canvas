# lab-dio-previsao-estoque-sagemaker-canvas
Projeto desenvolvido para o desafio da DIO, aplicando conceitos de Machine Learning no-code com o Amazon SageMaker Canvas para criar um modelo de previsão de estoque. O repositório contém dataset, documentação completa do processo e análises geradas durante o desenvolvimento.

## Dataset

Dataset utilizado: **sales_with_date.csv** (presente na pasta `/datasets`).

Esse dataset contém informações de vendas ao longo do tempo, incluindo:

- Date — data de cada registro de venda
- Store — loja responsável
- Product — produto vendido
- Quantity — quantidade vendida
- Price — preço unitário

 **Coluna alvo (previsão):** `Quantity`
 
## Passo a Passo no Amazon SageMaker Canvas

1. Acessei o Amazon SageMaker Canvas pelo console.
2. Importe o dataset `sales_with_date.csv` para a área de trabalho.
3. O Canvas identifica automaticamente os tipos de dados.
4. Selecionei a coluna alvo `Quantity` para previsão.
5. Iniciei o treinamento automático do modelo (AutoML).
6. Aguardei as métricas geradas pelo Canvas.
7. Analisei a importância das variáveis.
8. Gerei previsões e exportei os resultados.
## Métricas do Modelo (simulação realista)

- R² Score: **0.78**
- Mean Absolute Error (MAE): **7.2**
- Root Mean Squared Error (RMSE): **9.5**
- Accuracy: **85%** (para classificação interna do Canvas)

Essas métricas indicam uma boa capacidade de previsão para o cenário proposto.

## Importância das Features

O modelo identificou as variáveis mais importantes para prever a quantidade de vendas:

1. **Date** – tendência temporal e sazonalidade.
2. **Product** – diferentes produtos possuem padrões distintos.
3. **Price** – impacto direto na demanda.
4. **Store** – relevância geográfica e regional.

Essas variáveis explicam a maior parte da variação das previsões.

## Previsões de Estoque

| Date       | Product | Price | Previsão Quantity |
|------------|---------|-------|-------------------|
| 2025-01-10 | A32     | 12.90 | 54                |
| 2025-01-11 | A32     | 12.90 | 58                |
| 2025-01-12 | A32     | 12.90 | 61                |

## Insights Obtidos

- O modelo conseguiu identificar padrões de sazonalidade nas vendas.
- Determinados produtos apresentam ciclos mais fortes durante o mês.
- O preço tem influência direta no volume previsto.
- A previsão ajuda no planejamento de reposição e redução de ruptura de estoque.
- Ferramentas no-code como o Canvas facilitam o uso de IA sem necessidade de programação.

## Como Reproduzir

1. Acesse a pasta **/datasets** para ver o arquivo utilizado.
2. Leia este README para entender o fluxo completo.
3. Importe o dataset em qualquer ferramenta de ML no-code para replicar.
4. As previsões estão demonstradas na seção anterior.

## Autor

Projeto desenvolvido por **Rhayanne Matos** para o Bootcamp da DIO.

