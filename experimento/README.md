# Experimento

Notebook do experimento fatorial descrito no Capítulo 2 (Metodologia).

## Como executar

1. Abra o `experimento_drift.ipynb` no Google Colab (Arquivo → Fazer upload de notebook, ou Arquivo → Abrir notebook → GitHub).
2. Execute todas as células (Ambiente de execução → Executar tudo).
3. Ao final, o arquivo `resultados.zip` é baixado com:
   - `*.csv`: resultados brutos por execução, médias por condição, sinais do detector, orientação, sensibilidade, detector ideal e análises complementares;
   - `figuras/`: figuras em PDF e PNG;
   - `tabelas/`: tabelas LaTeX prontas para `\input`.

A execução completa (180 condições × 10 repetições, mais a análise de sensibilidade e as análises complementares de janela de treino, drift virtual, orçamento, validação do detector e rótulos atrasados) leva cerca de uma hora no Colab. As sementes são fixas, portanto os resultados são reprodutíveis.

## Organização no repositório

- `experimento/experimento_drift.ipynb`: notebook;
- `experimento/resultados/`: CSVs e resumo (`resumo.json`) da execução usada no texto;
- `figuras/resultados/`: figuras geradas pelo notebook;
- `tabelas/`: tabelas geradas pelo notebook.

## Versões e reprodução

Os resultados do texto foram obtidos com Python 3.13 e as versões listadas em `requirements.txt`; com elas, uma nova execução reproduz os resultados de forma idêntica (as sementes são fixas). No Colab, para usar exatamente essas versões, execute antes do notebook:

```
!pip install -r https://raw.githubusercontent.com/gaubiela/tcc-gabriela/v1.0/experimento/requirements.txt
```

e reinicie o ambiente de execução. A ANOVA em parcelas subdivididas (Tabela 8 do texto) é gerada na Seção 7.1 do notebook; as reanálises (streams lentas, reset × janela e ANOVA sem o controle), na Seção 13.

## Dependências

Python 3, NumPy, pandas, SciPy, scikit-learn, XGBoost, statsmodels, matplotlib e joblib (todas disponíveis no Colab; o notebook instala XGBoost e statsmodels se faltarem).
