# 📊 Análise da Violência Contra Pessoas LGBTQIA+ no Brasil

Repositório oficial do projeto final do curso de Inteligência Artificial organizado por PertaLabs.  
**Grupo**: Análise da violência contra a população LGBTQIA+ utilizando dados do Grupo Gay da Bahia (GGB)

📄 **Fonte dos dados**: [Base dos Dados - Relatório de Violência LGBTQIA+ (GGB)](https://basedosdados.org/)

---

## 🏳️‍🌈 Contexto

O Brasil lidera rankings mundiais de violência contra pessoas LGBTQIA+.  
Esta análise utiliza dados anuais do **Grupo Gay da Bahia**, uma das instituições mais antigas de defesa dos direitos LGBTQIA+ no país.  
O objetivo do projeto é compreender **padrões territoriais e demográficos** nos registros de assassinatos dessa população.

---

## ❓ Perguntas Orientadoras

- Quais estados têm as maiores taxas de violência contra a população LGBTQIA+?
- Há padrões sazonais ou demográficos (idade, raça ou identidade de gênero) nos crimes?

---

## ⚙️ Metodologia

- Os arquivos CSV foram previamente baixados da plataforma e carregados no ambiente do **Google Colab**.
- O tratamento dos dados foi realizado com **Pandas**, incluindo:
  - Remoção de valores nulos
  - Padronização dos nomes das colunas
- As visualizações foram criadas com **Seaborn** e **Matplotlib** para responder às perguntas orientadoras.

### 📈 Visualizações

- **Gráficos de barras** para destacar:
  - Estados com mais homicídios
  - Raça/cor das vítimas
  - Identidade de gênero das vítimas

---

## 🤖 Análise com Machine Learning: Previsão de Risco

Foi explorada uma aplicação inicial de **Machine Learning** para prever o número de homicídios com base em atributos demográficos, utilizando o dataset por raça/cor (`df_raca`).

### 🔍 Metodologia

- A variável categórica `raca_cor` foi transformada em variáveis dummy (**one-hot encoding**).
- A variável alvo (`y`) foi o **número de homicídios**.
- As variáveis explicativas (`X`) foram as colunas dummy das raças.
- O modelo escolhido foi o **Random Forest Regressor**, robusto para tarefas de regressão.
- Dividimos o dataset em treino e teste (`random_state=42` para reprodutibilidade).
- O modelo foi treinado com os dados de treino e avaliado com os dados de teste.

### 📊 Resultados

- Avaliamos o desempenho com o **Erro Médio Absoluto (MAE)**.
- Um gráfico de densidade (**KDE plot**) foi gerado para comparar a distribuição entre os valores reais e previstos.
- Utilizamos uma paleta de cores suaves e um estilo clean para facilitar a leitura e interpretação.

---

## 👥 Integrantes do Grupo

| Nome              | GitHub                        |
|-------------------|-------------------------------|
| Griselda Justo    | [@GriseldaJusto](https://github.com/GriseldaJusto)         |
| Camille Nogueira  | [@camizsn](https://github.com/camizsn)                     |
| Priscila Estevao  | [@priscilaestevao](https://github.com/priscilaestevao)     |
| Amanda Amani      | [@AmandaAmani](https://github.com/AmandaAmani)             |
| Manuela Oliveira  | [@Manuelaoliveira97](https://github.com/Manuelaoliveira97) |
| Raysa Leide       | [@raysaleide](https://github.com/raysaleide)               |
