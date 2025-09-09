# adcv-his-brasil
ADCV para HIS no Brasil (B6 – eletricidade para resfriamento)
Este repositório contém código e dados processados para reproduzir as figuras e tabelas do artigo:

Sistemas Construtivos e Transição Energética Brasileira: uma Avaliação Dinâmica do Ciclo de Vida (ADCV) para Habitação Social.

Como rodar (resumo)
Crie o ambiente: conda env create -f code/00_environment.yml && conda activate adcv
Baixe o EPW oficial (ver data/inputs/weather/README.md) e coloque na pasta indicada.
Rode na ordem:
python code/02_energyplus_runner.py → gera consumo anual (B6)
python code/03_mlp_grid_forecast.py → gera mix_projetado_*
python code/04_adcv_impact_calc.py → impactos anuais/acumulados
python code/05_monte_carlo.py → incerteza (n=1000)
Figuras e tabelas finais saem em results/.
Licenças e dados
Código: MIT (ver LICENSE).
Dados derivados: CC BY 4.0.
Inventários GaBi/ecoinvent não são redistribuídos. Disponibilizamos fatores derivados por fonte (data/processed/fatores_derivados_2015_por_fonte.csv) e scripts que recalculam esses fatores em instalações licenciadas.
Citar
Veja CITATION.cff. (Se houver DOI/Zenodo depois, será adicionado.)
