# Clusterização de Vinhos com PCA e K-Means

### Objetivo

O objetivo deste projeto é agrupar diferentes tipos de vinhos em clusters com base em suas características químicas.
Utilizamos o PCA (Análise de Componentes Principais) para reduzir o número de variáveis e o K-Means para identificar grupos (clusters) de vinhos semelhantes.

### Dataset

Foi utilizado o Wine Dataset do Scikit-learn, que contém:
- 178 amostras de vinhos;
- 13 variáveis químicas (como teor alcoólico, magnésio, fenóis, cor, etc.);
- 3 classes reais, representando vinhos de três produtores diferentes.

### Entendendo o Problema

Imagine que recebemos dados químicos de vários vinhos, mas sem saber de qual produtor eles vieram.
A tarefa é agrupar os vinhos que são quimicamente parecidos, formando grupos com base nas semelhanças dos atributos.

### Por que usar PCA?

O dataset tem 13 dimensões, o que dificulta a visualização.
O PCA reduz essas dimensões para 2 componentes principais, mantendo a maior parte da informação dos dados.
Isso nos permite plotar os vinhos em um gráfico 2D e visualizar como se agrupam naturalmente.

### Por que usar K-Means?

Depois da redução com o PCA, aplicamos o K-Means, um algoritmo de clusterização que agrupa os pontos próximos uns dos outros.
Como sabemos que há 3 tipos de vinho, definimos k = 3.

### O Código

O código segue a seguinte estrutura:
- Carrega o dataset Wine do Scikit-learn.
- Escala os dados (o PCA é sensível à escala).
- Reduz as dimensões de 13 para 2 com o PCA.
- Aplica o K-Means com 3 clusters.
- Gera gráficos comparando os clusters encontrados com as classes reais.

### Resultados Obtidos

Após a execução, dois gráficos foram gerados:

🔹 Clusters Encontrados pelo K-Means

Mostra os grupos criados automaticamente pelo algoritmo com base na similaridade dos vinhos.
Os pontos coloridos representam os clusters e os “X” vermelhos são os centróides dos grupos.

🔹 Classes Reais dos Vinhos

Mostra as classes verdadeiras (os três produtores de vinho) para comparação.

### Conclusão

Os resultados mostram que o PCA conseguiu separar bem os grupos no espaço bidimensional, e o K-Means identificou clusters muito próximos das classes reais.
A variância explicada pelos dois primeiros componentes principais ficou acima de 55%, indicando que a maior parte da estrutura dos dados foi preservada.

Este projeto demonstra como PCA e K-Means podem ser combinados para entender e visualizar padrões ocultos em conjuntos de dados complexos, sem a necessidade de rótulos prévios.
