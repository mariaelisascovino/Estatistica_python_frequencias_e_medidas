# Estatistica_python_frequencias_e_medidas

Exercícios de Frequências e medidas com Pyhton e uso das bibliotecas e extensões: Pandas, Seaborn, Scipy, Numpy - Matplotlib.

- Cálculo de médias, modas, medianas, amplitude, desvio padrão, variância, quartis, IQR
- Plotagem e interpretação de histogramas e boxplots
- Identificação, exibição, definição de limite e remoção de outliers


Uso das bibliotecas e extensões: Pandas, Seaborn, Scipy, Numpy - Matplotlib


DATAFRAME ENEM 2023

O dataframe apresenta dados sobre notas dos candidatos nas disciplinas de linguagens, ciências humanas, ciências da natureza, matemática e redação, e ainda um campo "Sexo" com o gênero daqueles que fizeram o exame no ano de 2023.

Verificamos que o dataframe possui 1000 linhas e 6 colunas, com maioria dos dados float(numérico) e um object (categórico). Verificamos que há valores de notas nulos.

<strong>Tratar dados nulos num dataframe depende sempre do contexto e do tipo de análise que será feita:</strong>

<ul>
<li>Excluir as linhas com valores nulos:</li>

Essa é a abordagem mais simples, mas pode levar à perda de informações valiosas, especialmente se a quantidade de dados nulos for significativa.
Recomendado quando os dados nulos são poucos e aleatórios, e não representam um padrão importante.

<li>Substituir por zero:</li>

Essa opção pode ser adequada se os valores nulos realmente significarem "zero" ou "nota não obtida" na sua análise.
Isso pode distorcer as estatísticas e análises subsequentes.

<li>Substituir pela média, mediana ou moda:</li>

Substituir os valores nulos pela média, mediana ou moda da coluna/disciplina pode ser uma boa opção quando você deseja preservar o máximo de informações possível.
Essa abordagem assume que os valores nulos são aleatórios e não representam um padrão específico.

A mediana pode ser preferível à média, pois é menos sensível a outliers.
</ul>

Aqui vamos utilizar as três abordagens dependendo da análise e algumas vezes vamos usar duas ou três para comparar os resultados.  

LEITURA INICIAL DO DATAFRAME

![PRINT1](https://github.com/user-attachments/assets/827ddcdd-bbce-4af4-9913-9bb1ab13021b)


<strong>Cálculos e contagens para fins de análise </strong>
MEAN, MEDIAN, MODE, STD, VAR, QUANTILE, IQR, SORT_VALUES

Foram feitos cálculos de média, mediana, moda, desvio padrão, amplitude, variância, quartis, intervalo interquartil, outliers, e usado top e sort_values. 

Esse projeto é direcionado para demonstrar como é feita análise inicial e cálculos que servirão de base para levantar e responder questões, e não tem foco em trazer insights e tirar conclusões sobre os dados. 

Assim podemos entender melhor os dados apresentados:

AMPLITUDE

A amplitude é uma medida estatística que indica a diferença entre o maior e o menor valor em um conjunto de dados. 

Amplitude= Valor Máximo - Valor Mínimo

df com nulos=0

![amplitude_0](https://github.com/user-attachments/assets/8dd3ecc1-7452-4b3a-84c6-afd1277ed4fa)

df com nulos excluídos

![amplitude_sem_nulos](https://github.com/user-attachments/assets/7544daea-dadf-422f-b8f5-fa4d0acc9485)

df com nulos =mediana

![amplitude_mediana](https://github.com/user-attachments/assets/bb72f7d2-d20b-49ca-b5c9-c5e5ca178f40)

A amplitude entre os valores mínimos e máximos é maior para a disciplina de Redação, indicando uma maior variação das notas dos candidatos nessa disciplina. As disciplinas de Matemática, Linguagens e Ciências da Natureza apresentam amplitudes intermediárias e a de Ciências Humanas possui a menor amplitude, sugerindo uma menor variação nos escores dos candidatos. 

MÉDIA 

A média é uma medida estatística que representa o valor central de um conjunto de dados. 

Média = Soma dos valores das notas / número total de notas

df com nulos=0

![media_0](https://github.com/user-attachments/assets/495f6d31-fffc-4f78-9b96-fc4bea2e33d7)

df com nulos excluídos

![media_sem_nulos](https://github.com/user-attachments/assets/fb13799d-4633-452c-a27b-b43c833a0555)

df com nulos = mediana

![media_sub_med](https://github.com/user-attachments/assets/e8bec98d-c778-4aea-a7b4-7d8bc4abdade)

A média de redação sendo a mais alta pode indicar maior desempenho/facilidade dos candidatos nessa disciplina. A média é maior para as disciplinas de Redação e Matemática, sugerindo um desempenho geral mais alto. As médias das disciplinas de Linguagens, Ciências da Natureza e Ciências Humanas são relativamente próximas entre si e inferiores às de Redação e Matemática.

MODA

A moda é uma medida estatística que representa o valor ou valores que aparecem com mais frequência em um conjunto de dados. Em outras palavras, a moda é o número que ocorre mais vezes em um conjunto de observações.

df nulos=0

![moda_0](https://github.com/user-attachments/assets/89caf80c-b83a-4527-8268-8e64c54b1af5)

df nulos excluídos

![moda_sem_nulos](https://github.com/user-attachments/assets/edbc6304-9771-4211-8f28-87ece0ec78a0)

df nulos= mediana

![moda_med](https://github.com/user-attachments/assets/33ea0c0e-3dbf-4980-94de-65a312150c44)


Podemos observar que ao substituir nulos=0 a moda é igual a zero, mostrando que o valor distorce as métricas significativamente. 

MEDIANA

A mediana é uma medida de tendência central que representa o valor que divide um conjunto de dados em duas partes iguais. Em outras palavras, é o valor que está no meio de um conjunto de dados ordenados.

Mediana total de números ímpar= é o valor que está na posição central, dividindo ao meio. 

Mediana total de números par = dois valores centrais /2

df nulos =0

![mediana_0](https://github.com/user-attachments/assets/0b85d1a3-7df1-4265-8cdf-450f54c816f1)

df com nulos excluídos

![mediana_sem_nulos](https://github.com/user-attachments/assets/51b1d5f2-1617-475d-b76d-f7ecd9fef7e7)

df com nulos = mediana

![mediana_sub_med](https://github.com/user-attachments/assets/94436426-0cbf-43b8-be3b-f60468829261)


A mediana é maior para as disciplinas de Matemática e Redação, indicando que metade dos estudantes obtiveram notas acima desses valores. As disciplinas de Linguagens, Ciências da Natureza e Ciências Humanas apresentam medianas intermediárias.

DESVIO PADRÃO

O desvio padrão é uma medida de dispersão que indica o quanto os valores de um conjunto de dados variam em relação à média. Em outras palavras, ele quantifica a quantidade de variação ou dispersão de um conjunto de valores.

df com nulos =0

![desvio_0](https://github.com/user-attachments/assets/89e9316b-a5df-4fb5-a73f-9e9a27382c7d)

df com nulos excluídos

![desvio_sem_nulos](https://github.com/user-attachments/assets/52d40c1c-aa4a-4b43-b458-74ceffd9dd9d)

df com nulos = mediana

![desvio_sub_med](https://github.com/user-attachments/assets/26e3b8d3-6965-4591-944c-039eef6f7266)

O desvio padrão maior no dataframe de nulos =0 indica maior dispersão dos dados em relação à media, ou seja maior variabilidade dos valores observados. 

Conclusão sobre as métricas 

Em resumo, os dados indicam que o desempenho dos estudantes é mais heterogêneo na disciplina de Redação, com maior amplitude. Possuindo maior desvio padrão em todas as análises sugere notas extremas e possíveis outliers.
Matemática e Redação apresentam médias e medianas mais elevadas em comparação às demais áreas. Isso pode sugerir, por exemplo, que um curso preparatório para o ENEM  precisa investir mais nas demais disciplinas para que os candidatos melhorem seu desempenho. 
Em relação a melhor maneira de usar os nulos depende do entendimento desse valor. Se realmente representa nota 0 no exame, o ideal é substituir por zero. Caso seja ausência por não ter o dado da nota daquele aluno, a melhor forma seria usando a mediana que apresenta menor distorção dos dados com menor desvio padrão. 

<strong>Mesmo não sendo o foco, é possível verificar  o uso desses cálculos para responder questões, tais como:</strong>

- Quais os 500 mais bem colocados para ingresso no curso de Ciência da computação? Qual gênero do primeiro colocado? Qual a quantidade de homens e mulheres dentro dos 500 primeiros?

Calculando a média ponderada de todas as disciplinas foi possível verificar a classificação para entrada em determinado curso (no caso, Ciências de Computação). Foi feito o cálculo da média ponderada para as três situações, nulos=0 , nulos excluídos e nulos=mediana e foi verificada uma diferença entre valores o que espelhou na classificação dos candidatos. Também foi realizado o cálculo da média geral e desvio padrão levando em consideração a média ponderada para comparar os valores. Temos, portanto 3 listagens de classificados dos 500 melhores. No primeiro caso temos 233 mulheres e 244 homens, para nulos excluídos temos 221 mulheres e 258 homens e no último caso 253 mulheres e 226 homens. Lembrando que não soma 500 pois temos candidatos sem a informação de gênero, estando como "Não identificado" no campo. Em todos, a primeira classificada é uma mulher. 

Média geral

![media_geral_500](https://github.com/user-attachments/assets/1c6a59c7-2fd0-4382-a1d0-7c80cbe19f37)

Desvio padrão geral

![desvio_geral_500](https://github.com/user-attachments/assets/0f8a6ebb-2f6c-4a4a-b993-8342f89564ba)


A maior média geral é do df com nulos = mediana pois o df com nulos = 0 os valores com zero puxam a média geral para baixo. O maior desvio padrão, que mais distorce os dados, é do dataframe com nulos excluídos. 

Qual dessas classificações devemos levar em conta ? depende de como vamos considerar os valores nulos. 

-Se todos esses estudantes aplicassem para ciência da computação e existem apenas 40 vagas, qual seria a variância e média da nota dos estudantes que entraram no curso de ciência da computação?

A partir do dataframe dos 500 melhores foram selecionados os 40 primeiros e depois calculado a média e variância da média ponderada desses 40 primeiros classificados. 

VARIÂNCIA

A variância é uma medida estatística que indica o grau de dispersão ou espalhamento de um conjunto de dados em relação à sua média. Em outras palavras, a variância mede o quanto os valores individuais se desviam da média.

Variância = soma (valores individuais - média) ² / número total de valores

df com nulos = 0

![var_0](https://github.com/user-attachments/assets/de477252-1e31-4dfd-9156-a2c8e32ade4e)


- Qual o valor do teto do terceiro quartil para as disciplinas de matemática e linguagens? 

QUARTIS

Os quartis são medidas de posição que dividem um conjunto de dados ordenados em quatro partes iguais. 

Q1- É o valor que divide os 25% menores valores do conjunto de dados.
Q2- É a Mediana. Divide o conjunto em duas partes iguais, com 50% dos dados abaixo e 50% acima. 
Q3- É o valor que divide os 75% menores valores do conjunto de dados.
Q4- É o valor máximo do conjunto de dados, ou seja, 100%. 

Aqui o cálculo dos quartis serviu para identificar outliers. 

OUTLIERS

Outliers são valores que estão fora do padrão esperado para o conjunto de dados. Eles se distanciam consideravelmente da média ou mediana do conjunto, sendo muito maiores ou menores. 

Para tanto foram calculados o limite inferior e superior (ou teto) para identificação dos outliers. 

Foram calculados os outliers das disciplinas de redação e ciências da natureza.


HISTOGRAMAS

Histogramas são gráficos que representam a distribuição de frequência de uma variável numérica contínua. 

df com nulos =0

![hist1_red_0](https://github.com/user-attachments/assets/0049d3de-2d6d-4a2d-97a8-5a4bd46527ce)

df com nulos excluídos

![hist2_red_sem_nulos](https://github.com/user-attachments/assets/2d7da772-734f-4eba-81d3-753eae9ab928)

df com nulos= mediana

![hist3_red_med](https://github.com/user-attachments/assets/fb93e990-b4ce-45f7-bb9b-05248ef7945b)


O primeiro histograma apresenta distribuição muito assimétrica à direita, com a maioria das notas concentradas entre 0 e 200.
Muitas notas baixas, provavelmente devido à substituição dos valores nulos por 0. O segundo já apresenta uma distribuição mais simétrica, com uma curva de distribuição mais próxima de uma normal, com maioria das notas concentrada entre 400 e 600. Já o último possui uma distribuição mais próxima de uma curva normal, com maior dispersão.A maioria das notas estão entre 500 e 800, com uma cauda à esquerda mais longa.

A escolha do método de tratamento dos valores nulos impacta significativamente a análise da distribuição das notas. A substituição pela mediana parece ser a abordagem que menos distorce a distribuição. 

BOXPLOTS

Boxplots, também conhecidos como diagramas de caixa, são uma representação gráfica que resume visualmente a distribuição de um conjunto de dados numéricos. Eles fornecem informações importantes sobre a localização, dispersão e simetria dos dados.

- A caixa representa o intervalo entre o primeiro quartil (Q1) e o terceiro quartil (Q3), também conhecido como intervalo interquartílico (IQR).
-A linha horizontal dentro da caixa representa a mediana (Q2) dos dados.
-Os "bigodes" são as linhas que se estendem a partir da caixa.
Eles se estendem até o valor máximo ou mínimo, excluindo os outliers.
-Os outliers são valores que estão fora do intervalo definido pelos bigodes.Eles são representados por pontos individuais fora da caixa.

df com nulos=0

![box_1](https://github.com/user-attachments/assets/de57140f-1b80-4040-9024-455aad7e1694)

df com nulos excluídos

![box_2](https://github.com/user-attachments/assets/08540ab3-0413-4059-936b-0d63b5e6f5c1)

df com nulos= mediana

![box_3](https://github.com/user-attachments/assets/04580e65-113e-420c-a632-f5872f26f498)

A mediana da disciplina de Ciências da Natureza é mais alta do que a mediana da disciplina de Redação.Há alguns outliers em ambas as disciplinas, indicando a presença de valores extremos. Há menos outliers no dataframe com nulos excluídos, indicando que alguns dos valores extremos provavelmente continha nulos. E no dataframe com nulos substituídos pela mediana há menos outliers em comparação com o primeiro boxplot, mas mais do que no segundo boxplot.A caixa do boxplot para Ciências da Natureza é maior, sugerindo uma maior variabilidade nos dados dessa disciplina.

Conclusão geral:

A análise exploratória dos dados revelou que o tratamento dos valores nulos tem um impacto significativo nas métricas estatísticas calculadas, como média, mediana, moda, desvio padrão e amplitude.

Ao substituir os valores nulos por 0, observou-se uma forte distorção das métricas, com a média e moda sendo puxadas para baixo. Já ao excluir os valores nulos, obteve-se uma visão mais realista da distribuição, porém com possível perda de informações importantes. A substituição dos nulos pela mediana mostrou-se a abordagem mais adequada, pois preservou melhor a estrutura dos dados sem distorcer excessivamente as análises. Porém é importante entender a origem e contexto da coleta desses dados para entender se as notas nulas realmente são notas que não se sabe o valor ou se se tratam de faltosos ou candidatos que não obtiveram pontuação, nesse caso o mais realista seria usar a abordagem de substituição de nulos por zero. 

As disciplinas de Matemática e Redação apresentaram médias, medianas e amplitudes mais elevadas em comparação às demais áreas, sugerindo um melhor desempenho geral dos candidatos nessas matérias. O desvio padrão mais alto na disciplina de Redação indica uma maior heterogeneidade nas notas, com possíveis outliers.

Esses cálculos e análises iniciais fornecem uma base importante para responder perguntas mais específicas, como a classificação dos melhores candidatos para um determinado curso, a comparação de desempenho por gênero e a identificação de padrões e tendências nos dados do ENEM.

Concluindo, o tratamento adequado dos valores nulos e a compreensão das métricas estatísticas são fundamentais para uma análise robusta e confiável dos dados educacionais, permitindo tirar insights relevantes e embasar tomadas de decisão.
