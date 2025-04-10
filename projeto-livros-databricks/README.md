# 📚 Projeto de Análise Literária com Databricks

## 🧠 Objetivo

Este projeto tem como objetivo analisar um grande volume de dados sobre livros, leitores e avaliações para descobrir padrões de comportamento, preferências literárias e tendências de leitura ao redor do mundo. A proposta foi desenvolvida como parte do curso de pós-graduação em Ciência de Dados e Analytics da PUC Rio.

---

## 🔗 Fontes de Dados

Utilizei o dataset público [Book Recommendation Dataset (Kaggle)](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset), que inclui três arquivos CSV:

- `Books.csv` — Informações sobre os livros (título, autor, editora, ano, imagens)
- `Ratings.csv` — Avaliações feitas por leitores (usuário, ISBN, nota)
- `Users.csv` — Dados dos leitores (ID, localização e idade)

---

## 🏗️ Pipeline de Processamento

O projeto foi estruturado em camadas para garantir a organização e a rastreabilidade do tratamento dos dados:

### 🔸 Bronze — Ingestão
- Upload e leitura dos arquivos CSV
- Armazenamento bruto no formato Delta Table

### 🔸 Silver — Limpeza e Padronização
- Tratamento de valores nulos e formatos inconsistentes
- Normalização de autores, localização, idade e campos textuais
- Deduplicação de registros

### 🔸 Gold — Análises e Visualizações
- Derivação de novas tabelas para análises estratégicas
- Exploração de comportamento por autor, faixa etária, país e ordem de publicação
- Geração de insights com suporte visual (gráficos e clusterizações)

---

## 🔍 Perguntas de Negócio

- ✅ O autor tende a melhorar (ou piorar) suas avaliações ao longo do tempo?
- ✅ O leitor mais jovem prefere livros mais novos?
- ✅ Existe padrão de leitura por país?
- ✅ Qual o grau de consistência do autor ao longo da carreira?
- ✅ Qual faixa etária é mais diversa na escolha de autores?
- ❌ Qual o impacto do gênero literário na avaliação média dos livros?
- ❌ O leitor de diferentes gêneros (masculino/feminino/outros) avalia de maneira distinta?
- ❌ Existem diferenças regionais de gosto literário associadas ao tipo de livro (ficção, romance, técnico)?
- ❌ Qual a relação entre o gênero do autor e o público leitor que mais o consome?
- ❌ Livros de certos gêneros têm maior longevidade ou relevância ao longo do tempo?

---

## 📊 Principais Descobertas

- **Autores mais consistentes:** com menor desvio de avaliação entre livros
- **Sequência de notas:** tendência geral de estabilização ou queda após o segundo livro
- **Leitores jovens:** concentram-se em livros mais recentes
- **Clusterização de países:** padrões etários de leitura são similares entre grupos regionais
- **Diversidade de autores:** leitores entre 30-45 anos tendem a explorar mais autores distintos

---

## 📁 Organização dos Notebooks

- `notebooks/00_resumo_projeto.ipynb` — Visão geral e resumo executivo do projeto
- `notebooks/01_bronze_ingestao.ipynb` — Carregamento dos dados
- `notebooks/02_silver_tratamento.ipynb` — Limpeza e padronização
- `notebooks/03_gold_analises.ipynb` — Derivações e métricas agregadas
- `notebooks/04_gold_visualizacoes.ipynb` — Gráficos e insights
- `notebooks/05_gold_clusterizacoes.ipynb` — Agrupamentos e perfis de leitor

---

## 🚀 Como Executar

1. Faça o upload dos CSVs para o Databricks
2. Execute os notebooks na ordem sugerida (00 → 05)
3. Os dados serão organizados automaticamente em camadas (Bronze, Silver, Gold)
4. Os resultados são salvos como Delta Tables e visualizações no notebook

---

## 📌 Observações Finais

Este projeto foi desenvolvido para fins educacionais e exploratórios. As análises podem ser expandidas com o uso de APIs externas (como OpenLibrary) ou dados adicionais sobre gêneros, vendas e editoras.

---

## 📄 Outras formas de leitura

- A visão geral também está disponível em [formato Markdown](docs/resumo_projeto.md) para facilitar a leitura fora do Databricks.

---

## Autoavaliação

Ao finalizar este projeto, sinto que consegui cumprir os objetivos definidos inicialmente. A proposta era construir um pipeline completo de dados dentro do ambiente Databricks, passando por todas as camadas — da ingestão à análise — e gerar insights relevantes a partir de dados literários. Esse processo foi seguido com cuidado e o projeto foi evoluindo de forma consistente até a entrega final.

Durante o desenvolvimento, enfrentei alguns desafios importantes. Um dos pontos que mais exigiu atenção foi o tratamento dos dados brutos, especialmente os nomes dos autores. Eles apresentavam muitos ruídos e inconsistências, o que nos levou a revisar a lógica de limpeza várias vezes, até alcançar um padrão aceitável. Outro desafio foi lidar com visualizações mais elaboradas, como os gráficos de bolhas e os mapas de calor, que exigiram uma preparação cuidadosa dos dados e ajustes de escala e suavização para se tornarem claros e informativos.

Por outro lado, foi muito satisfatório perceber como as perguntas de análise foram ganhando profundidade ao longo do projeto. Começamos com algumas hipóteses iniciais e, conforme os dados iam sendo tratados novas ideias surgiram naturalmente. A estrutura em notebooks separados e bem organizados ajudou bastante a manter o projeto compreensível e reutilizável.

Como próximo passo, acredito que seria interessante enriquecer o dataset com informações complementares — como gênero literário, nacionalidade dos autores ou perfil mais detalhado dos leitores —, o que abriria espaço para novas perguntas e análises ainda mais aprofundadas. Também vejo potencial para conectar os resultados deste projeto com modelos de recomendação de livros, aproveitando os padrões identificados.

De forma geral, considero que o trabalho cumpriu bem seu papel acadêmico e também representa uma boa adição ao meu portfólio pessoal, refletindo tanto domínio técnico quanto interesse genuíno pelo tema.

---

## 👨‍💻 Autor

**Vinícius Berkembrock Marcon**  
10/04/2025  
Pós-graduação em Ciência de Dados e Analytics — PUC Rio