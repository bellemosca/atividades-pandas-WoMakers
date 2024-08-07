# Pandas

### O que é pandas?

O pands, um pacote Python dedicado à manipulação de daods, também possuí funcionalidade para a visualização de dados. Sua estrutura é fundamentada em dois pacotes essenciais do Python: Numpy e Matplotlib. Enquanto o Numpy oferece objetos de matriz multidimensionais para facilitar a manipulação de dados, o Matplotlib proporciona ao pandas capacidades robustas de visualização de dados.

Com uma ampla base de usuários, o panda registrou aproximadamente 14 milhões de downloads no PyPi em dezembro de 2019. Essa cifra representa praticamente toda a comunidade de ciência de dados em Python!

## Introdução a DataFrames
### Formato de dados
Guardar informações pode ser feito muitas maneiras, mas a mais comum é como uma tabela, que chamamos de "dados retangulares" ou "dados tabulares". Vamos imaginar isso como uma folha de papel dividida em linhas e colunas. No exemplo dos cachorros, cada cachorro é uma linha, e as coisas diferentes sobre eles, como nome e cor, são as colunas.

(adicionar uma imagem aqui)

### Criando um DataFrame
---
#### - Utilizando listas e dicionários
Podemos criar dataframes de várias formas, umas das mais simples é utilizando dicionários e listas:

(adicinar imagem aqui)

(adicinar imagem aqui)

#### - Lendo um arquivo e transformando-os em dataframe
Existem vários tipos de arquivos que podem ser lidos diretamente em um dataframe...

(adicinar imagem aqui)

### Primeiros métodos para entender seu DataFrame
---
#### df.head()
Quando a gente ganha uma tabela nova, é legal dar uma olhada rápida né?

O pandas tem um truque chamado "head" que mostra as primeiras linhas da tabela. Se tiver muitas linhas, isso ajuda bastante!

(adicinar imagem aqui)

#### df.info()
Tem um jeito do pandas nos contar os nomes das colunas, que são como etiquetas, e se tem alguma informação faltando, ele usa um método chamado "info" para isso.

(adicinar imagem aqui)

#### df.shape()
A tabela do pandas tem um de mostrar quantas linhas e quantas colunas ela tem, como se fosse um resuminho. Não precisa usar parêntese, é só chamar "shape".

      1  df_cachorros.shape

      (10, 6)

#### df.describe()
O pandas também sabe fazer as contas! Com o "describe", ele conta coisas legais sobre os números na tabela, tipo média e mediana. Ele até fala quantos números tem em cada coluna.

(adicinar imagem aqui)

### Componentes de um DataFame
___
#### Peças especiais do DataFrame
A tabela do pandas é como um quebra-cabeça com três partes:

- .values: os valores(que são os dados mesmo);
- .columns: as etiquetas (labels) das colunas;
- .index: etiquetas das linhas;

Isso ajuda a entender melhor cada pedacinho!

(adicinar imagem aqui)

(adicinar imagem aqui)

(adicinar imagem aqui)

## Ordenação e subconjunto
### Ordenação
Você pode ordenar as linhas usando o método sort_values, passando o nome da coluna pela qual você deseja ordenar...

      df.sort_values('coluna')

(adicinar imagem aqui)

Definir o argumento ascending como False ordenará os dados de forma inversa, do cachorro mais pesado para o cachorro mais leve...

      df.soft_values('coluna',ascending=False)

(adicinar imagem aqui)

Podemos ordenar por várias variáveis passando uma lista de nomes de colunas para sort_values. Aqui, ordenamos primeiro por peso e depois por altura...

      df.soft_values(['Altura(cm)','Peso(kg)'])

(adicinar imagem aqui)

#### Ordenação por múltiplas variáveis
Para alterar a direção da ordenação, passe uma lista para o argumento ascending para especificar em qual direção a ordenação deve ser feita para cada variável...

      df.soft_values(['Altura(cm)','Peso(kg)'], ascending=[True, False])

(adicinar imagem aqui)

