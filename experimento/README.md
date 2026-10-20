# Experimento

Notebook do experimento fatorial descrito no Capítulo 2 (Metodologia).

## Como executar

1. Abra o `experimento_drift.ipynb` no Google Colab (Arquivo → Fazer upload de notebook, ou Arquivo → Abrir notebook → GitHub).
2. Execute todas as células (Ambiente de execução → Executar tudo).
3. Ao final, o arquivo `resultados.zip` é baixado com:
   - `*.csv`: resultados brutos por execução, médias por condição, sinais do detector, orientação e sensibilidade;
   - `figuras/`: figuras em PDF e PNG;
   - `tabelas/`: tabelas LaTeX prontas para `\input`.

A execução completa (180 condições × 10 repetições, mais a análise de sensibilidade) leva cerca de 15 minutos no Colab. As sementes são fixas, portanto os resultados são reprodutíveis.

## Organização no repositório

- `experimento/experimento_drift.ipynb`: notebook;
- `experimento/resultados/`: CSVs e resumo (`resumo.json`) da execução usada no texto;
- `figuras/resultados/`: figuras geradas pelo notebook;
- `tabelas/`: tabelas geradas pelo notebook.

## Dependências

Python 3, NumPy, pandas, SciPy, scikit-learn, XGBoost, statsmodels, matplotlib e joblib (todas disponíveis no Colab; o notebook instala XGBoost e statsmodels se faltarem).
