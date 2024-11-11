# K-means-Mall-Customers

## Alunos:
-  Felipe Leão
-  Danilo Scheltes
-  Henrique Lyrio
-  Rafael Santos
## Objetivos:
O objetivo deste projeto é aplicar o algoritmo de KMeans para realizar a segmentação de clientes com base em duas variáveis: idade e renda anual. Para encontrar o número ideal de clusters, utilizamos a métrica Silhouette Score, que ajuda a avaliar a qualidade da separação entre os clusters. O número de clusters será selecionado automaticamente com base no valor máximo do Silhouette Score.
## Passo a passo:
### 1. Carregar o Dataset e Ajustar os Dados
Carregamos o dataset usando o `pandas` a partir do arquivo CSV, disponivel no `kaggle`. Em seguida, selecionamos as primeiras 200 linhas para realizar a análise.
Tratamos os dados ajustando os valores negativos nas colunas `Age` e `Annual Income (k$)`, substituindo-os pela média dessas variáveis. Também preenchemos valores ausentes com a média.
### 2. Escalonamento dos Dados
Utilizamos o `MinMaxScaler` da `sklearn` para normalizar os dados, escalonando as variáveis Age e Annual Income (k$) para o intervalo de 0 a 1. Esse processo é importante para evitar que as variáveis com maiores escalas dominem as distâncias no KMeans.
### 3. Cálculo do Silhouette Score
Para determinar o número ideal de clusters, implementamos uma função que calcula o `Silhouette Score` para diferentes números de clusters, variando de 2 a 10. O Silhouette Score avalia a qualidade da separação entre os clusters, e o número de clusters com o maior Silhouette Score é considerado o melhor.
### 4. Treinamento do Modelo KMeans
Usando o número de clusters selecionado com base no Silhouette Score, aplicamos o `KMeans` para segmentar os dados em clusters. Cada cliente é atribuído a um cluster, e os resultados são adicionados ao DataFrame original.
### 5. Visualização dos Resultados
Geramos um gráfico de barras que mostra os Silhouette Scores para diferentes números de clusters, permitindo visualizar o número de clusters ideal.
Em seguida, geramos um gráfico de dispersão que exibe os clusters encontrados pelo KMeans, com cada cluster representado por uma cor diferente e os centróides dos clusters marcados.
### 6. Avaliar a Qualidade do Modelo
Após o treinamento, avaliamos o modelo usando o Silhouette Score para garantir que a segmentação dos clientes esteja bem definida. A visualização dos clusters também ajuda a entender a distribuição dos dados.

## Video de demonstração dos resultados:


https://github.com/user-attachments/assets/03351087-cf08-426a-a87a-20c9d0f03b3b

