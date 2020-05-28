# CoRINs (Comparator of Residue Interaction Networks)
O CoRINs é uma ferramenta Web de comparação de múltiplos arquivos provenientes de redes de interação de resíduos do software RING 2.0 (https://protein.bio.unipd.it/ring/) gerando resultados de fácil compreensão através de tabelas, gráficos interativos e arquivos de texto. Desenvolvida em linguagem Python com bibliotecas de alta performance como Pandas (https://pandas.pydata.org/), Numpy (https://numpy.org) e Matplotlib (https://matplotlib.org/), juntamente com os frameworks de desenvolvimento Web Django (www.djangoproject.com/), Bootstrap (https://getbootstrap.com/), D3.js (https://d3js.org/) e um módulo de geração de parâmetros de grafos (betweness e coeficiente de clusterização) desenvolvido em linguagem R (https://www.r-project.org/).

### Autores: 
Felipe Vieira da Fonseca (Author, Data Scientist), Thiago Dantas Soares (Web Developer, Technical Support), Diego Morais (R Developer), João Paulo Matos Santos Lima (Coordinator, Author, Maintainer).

### Citation: 
https://www.biorxiv.org/------------

# How does it work?
A entrada dos dados do CoRINs consiste nos arquivos nodes.txt e edge.txt ou sua forma compactada gerada pela versão web do RING 2.0 (https://protein.bio.unipd.it/ring/), de cada RIN a ser comparada. Os nodes e edges são convertidos em dataframes, separados por cadeias proteicas e comparados um a um de acordo com a posição dos aminoácidos e das diferentes cadeias das proteínas. Assim são obtidos os resultados de acordo com a comparação dois a dois de cada cadeia para cada proteína, incluindo a comparação entre as cadeias de uma mesma proteína.

# Interpreting Results
O CoRINs é capaz de mostrar algumas informações úteis para a análise das redes, de forma global, ou seja, uma comparação entre todos as RINs carregadas e local, comparando as RINs cadeia a cadeia.

* Standard deviation of degree of all comparisons
  ![alt text](https://github.com/ffvieira18/teste/blob/master/grafico%201%20%20standard%20deviation%20of%20degree%20of%20all%20comparisons.png)
  
  A análise global consiste em um gráfico que representa a variação na formação de interações de todos os resíduos. O gráfico é construído a partir do desvio padrão de todos os valores de degrees dos aminoácidos equivalentes em posição, respeitando a condição da existência de 80% e ao menos dois degrees na posição referida.
Este gráfico apresenta como eixo x, a posição do aminoácido e como eixo y, o desvio padrão com o seu resultado refletido negativamente para melhor visualização da variação do degree na posição referida. Também foram traçadas duas linhas guias, nos valores de desvio de padrão de 0.5 e 1.5, onde foram estabelecidos os critérios das cores dos pontos (Tabela). 

  | Intervalo        | Cor          | 
  | ---------------- |:------------:|
  | >= 0.0 e <= 0.5  | Azul         |
  | > 0.5 e < 1.5    | Marrom       | 
  | >= 1.5           | Vermelho     |   

  Desvios padrões em torno do valor de degree médio com variação acima de 0.5 já indicam resíduos que variam consideravelmente o seu número de conexões. Valores de desvio padrão maiores que 1.5 indicam prováveis posições de variação conformacional.


# Installing


```js
teste
```
<a href="#interpolateOrRd" name="interpolateOrRd">#</a> d3.<b>interpolateOrRd</b>(*t*) [<>](https://github.com/d3/d3-scale-chromatic/blob/master/src/sequential-multi/OrRd.js "Source")
<br><a href="#schemeOrRd" name="schemeOrRd">#</a> d3.<b>schemeOrRd</b>[*k*]
<img src="https://raw.githubusercontent.com/d3/d3-scale-chromatic/master/img/OrRd.png" width="100%" height="40" alt="OrRd">
