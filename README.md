# Previsão de Energia em Usina UTCC com Regressão Linear

Este projeto foi desenvolvido como parte da disciplina:

**PAM0466 – Sistemas Inteligentes**
**Semestre:** 2026.1

**Docente:** Pedro Thiago Valério de Souza

---

## Introdução e Contexto

Uma usina termoelétrica de ciclo combinado (UTCC) é uma instalação de alta eficiência que combina turbinas a gás e a vapor para geração de eletricidade. Esse tipo de usina reaproveita o calor dos gases de exaustão da turbina a gás (ciclo Brayton) para produzir vapor, que aciona uma segunda turbina (ciclo Rankine), aumentando significativamente o rendimento do sistema.

A principal vantagem desse modelo é a alta eficiência energética, podendo atingir cerca de 60%, além de contribuir para a redução das emissões de gases de efeito estufa.

Apesar disso, um dos principais desafios técnicos está na integração e operação conjunta desses dois ciclos termodinâmicos. Nesse contexto, a potência elétrica gerada (PE) é altamente sensível às condições ambientais.

---

## Objetivo

O objetivo deste projeto é desenvolver um modelo de **regressão linear múltipla** capaz de prever a produção de energia elétrica com base em variáveis ambientais, contribuindo para a otimização do despacho energético.

---

## Dataset

Foi utilizado o dataset **Combined Cycle Power Plant (CCPP)**, disponível na UCI:

  https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant

O conjunto de dados contém **9.568 amostras** com as seguintes variáveis:

* **AT** – Temperatura ambiente (°C)
* **V** – Vácuo de escape (cm Hg)
* **AP** – Pressão atmosférica (mbar)
* **RH** – Umidade relativa (%)
* **PE** – Energia elétrica gerada (MW) *(variável alvo)*

---

## Metodologia

O projeto foi desenvolvido nas seguintes etapas:

### 1. Análise de Correlação

* Identificação das variáveis mais influentes na produção de energia

### 2. Análise entre Variáveis Independentes

* Verificação de possíveis relações entre variáveis (multicolinearidade)

### 3. Modelagem

* Construção de um modelo de regressão linear múltipla
* Divisão dos dados:

  * 80% treino
  * 20% teste

### 4. Avaliação do Modelo

Foram utilizadas as seguintes métricas:

* **R²:** 0.93
* **MAE:** 3.59
* **RMSE:** 4.50

---

## Resultados

O modelo apresentou excelente desempenho, sendo capaz de explicar aproximadamente **93% da variação dos dados**.

As variáveis mais influentes identificadas foram:

* Temperatura ambiente (AT)
* Vácuo de escape (V)

O gráfico de valores reais versus previstos indicou uma forte correlação entre os dados, com baixa dispersão.

---

## Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Como Executar

1. Clone o repositório:

```bash
git clone https://github.com/franciscalorraynes/regressao_linear_multipla.git
```

2. Instale as dependências:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Execute o código:
   
Para rodar o script Python:

```bash
python correlacao_regressao_linear.py
```
Ou, caso queira utilizar o notebook:
```bash
jupyter notebook
```
E abra o arquivo correlacao_regressao_linear.ipynb.
  
---

## Autores

- Francisca Lorrayne de Lima Santos
- Francisca Samira Aquino França

---

## Considerações Finais

O modelo de regressão linear múltipla se mostrou adequado para prever a produção de energia da usina UTCC, apresentando alta precisão e baixos erros, mesmo diante de possíveis relações entre variáveis independentes.

---

## Referência

UCI Machine Learning Repository – Combined Cycle Power Plant Dataset
