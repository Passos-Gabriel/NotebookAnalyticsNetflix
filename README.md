# 🎬 Análise de Clientes com RFM e KMeans - Dados da Netflix

Este projeto realiza uma análise de segmentação de clientes com base na metodologia **RFM (Recência, Frequência e Valor Monetário)** aplicada aos dados de avaliações da Netflix. Utilizamos **Spark para processamento distribuído**, **Pandas para transformação final** e **KMeans (Sklearn)** para clusterização.


## 🔍 Objetivo

- Agrupar usuários da Netflix de acordo com o comportamento de avaliação de filmes.
- Utilizar a técnica de RFM para extrair métricas representativas.
- Aplicar **KMeans Clustering** para identificar segmentos de clientes.
- Explorar visualmente os clusters para interpretação de perfis.

---

## ⚙️ Tecnologias Utilizadas

- Apache Spark (Databricks)
- Python 3.8+
- Pandas, Scikit-learn, Seaborn, Matplotlib
- Google Drive + gdown (para ingestão dos dados)

---

## 🔢 Etapas do Pipeline

1. **Extração dos Dados**  
   - Download e descompactação dos arquivos `.txt` com avaliações da Netflix.
   - Leitura e consolidação em um único arquivo `data.csv`.

2. **Carga e Processamento com Spark**
   - Leitura do CSV via Spark.
   - Criação das métricas **Recency**, **Frequency** e **Monetary** com SQL.

3. **Transformação e Escalonamento**
   - Conversão para Pandas.
   - Normalização das colunas com `MinMaxScaler`.

4. **Clusterização com KMeans**
   - Clusterização em 4 grupos com `KMeans`.
   - Análise e visualização dos resultados com `pairplot`.

---

## 📊 Visualização dos Clusters

![Pairplot dos Clusters](plots/pairplot.png)

---

## 💡 Interpretação (Exemplo de Insights)

- **Cluster 0**: Clientes com alta frequência e alto valor de avaliação, com avaliações recentes.
- **Cluster 1**: Clientes inativos, com baixa frequência e avaliações antigas.
- **Cluster 2**: Clientes moderadamente ativos.
- **Cluster 3**: Clientes novos ou pouco engajados.

---

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repo.git
   cd nome-do-repo
