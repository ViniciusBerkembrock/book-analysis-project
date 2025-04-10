
# 📊 Projeto de Análise Literária — Resumo Executivo

## ✅ Visão Geral

Este projeto tem como objetivo analisar dados de livros, leitores e avaliações com o intuito de gerar insights estratégicos sobre o comportamento literário global. Os dados foram tratados em camadas e explorados em diferentes direções, com foco em autores, leitores, países e padrões de avaliação.

---

## 🔁 Pipeline de Dados

- **Bronze**: Ingestão de dados brutos (Books.csv, Ratings.csv, Users.csv)
- **Silver**: Limpeza e padronização dos dados
- **Gold**: Geração de análises, visualizações e modelos de clusterização

---

## 🧠 Principais Análises Realizadas

### 📈 Tendência de Avaliações por Ordem de Lançamento
- Análise da média das notas ao longo da sequência de publicações dos autores.
- Resultado: livros iniciais tendem a ter avaliações ligeiramente melhores.

### ⏱️ Intervalo Entre Lançamentos x Nota
- Autores com grandes intervalos não necessariamente têm melhores avaliações.
- A consistência parece influenciar mais do que o tempo de espera.

### 📚 Volume de Publicações x Avaliação Média
- Autores com muitos livros tendem a ter médias de nota mais estáveis.
- Identificação de outliers altamente produtivos com excelente avaliação.

---

## 👥 Perfil dos Leitores

### 📅 Faixa Etária x Ano dos Livros Lidos
- Leitores mais jovens preferem livros mais recentes.
- Leitores com mais idade tendem a ler livros publicados em décadas anteriores.

### 💬 Avaliação por Faixa Etária e Época do Livro
- Heatmap com avaliação média cruzando faixa etária do leitor com década de publicação.
- Suavização para revelar zonas quentes de apreciação por geração.

### 📖 Diversidade de Autores por Leitor
- Leitores entre 30–45 anos apresentam maior diversidade de autores avaliados.
- Leitores jovens tendem a se concentrar em um número menor de autores.

---

## 🌍 Clusterizações

### 🧑‍💻 Clusterização de Autores
- KMeans baseado em quantidade de livros, média de nota, desvio padrão e ano médio.
- Identificação de perfis como autores prolíficos, consistentes, novos ou polarizadores.

### 🌎 Clusterização de Países
- Proporção de leitores por faixa etária em cada país.
- Agrupamento de países com padrões demográficos similares de leitura.

---

## 📌 Conclusões

- O projeto revela padrões temporais, demográficos e culturais no consumo de literatura.
- Clusterizações ajudam a entender grupos de comportamento.
- Muitas análises podem ser expandidas com uso de metadados externos (ex: gênero do livro).

---

## 📁 Organização Técnica

- `01_bronze_ingestao.ipynb` → Ingestão de dados
- `02_silver_tratamento.ipynb` → Limpeza e padronização
- `03_gold_analises.ipynb` → Métricas e tabelas derivadas
- `04_gold_visualizacoes.ipynb` → Gráficos explicativos
- `05_gold_clusterizacoes.ipynb` → Agrupamentos e segmentações
