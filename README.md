# Simulador de Carteira de Investimentos

## Pergunta que o projeto responde
Será que rebalancear periodicamente uma carteira de ativos supera simplesmente comprar e segurar (*buy-and-hold*), no mercado brasileiro?

## Objetivo
Construir um simulador de carteira de investimentos que compara o desempenho histórico de diferentes estratégias de alocação, usando dados reais de ativos da B3, avaliando retorno, risco e métricas ajustadas ao risco.

## Estratégias comparadas
- **Buy and hold** — compra inicial, sem movimentações.
- **Rebalanceamento periódico** (ex: mensal/trimestral) — retorno da carteira aos pesos-alvo originais.
- **Pesos iguais vs pesos por valor de mercado** — comparação de critérios de alocação inicial.

## Dados
- Fonte: [yfinance](https://pypi.org/project/yfinance/) (dados históricos gratuitos do Yahoo Finance).
- Ativos: a definir (ex: 5–10 ações da B3 + um ETF de referência, como BOVA11).
- Período: a definir (ex: últimos 5–10 anos).

## Métricas de avaliação
- Retorno total e retorno anualizado
- Volatilidade (desvio padrão dos retornos)
- Índice de Sharpe
- Máximo drawdown

## Estrutura do projeto
notebooks/    # exploração inicial e prototipagem
src/          # funções reutilizáveis (cálculo de retorno, Sharpe, etc.)
requirements.txt
README.md

## Limitações / simplificações assumidas
- Não considera custos de transação nem impostos.
- Rebalanceamento com regras fixas (sem otimização dinâmica).
- Foco em ilustrar o comportamento das estratégias, não em recomendação de investimento.

## Próximos passos (v2, opcional)
- Otimização de carteira via Teoria Moderna de Portfólio (Markowitz).
- Dashboard interativo (Streamlit) para explorar diferentes composições.
