
A **representação atômica e a faturada** abordadas anteriormente no curso serão de bastante utilizade para a parte de satisfação de condições, basicamente recapitulando, a representação atômica diz respeito a respeito a representação de cada estado como apenas um bloco ou uma unidade sem atributos, enquanto a fatorada os estados adquirem atributos internos que as caracterizam, no caso de problemas de satisfação de condições o que se usa a representação fatorada o qual por meio dos atributos aos estados procuraremos suprimir uma condição dada pelo usuario.

<p align="center">
  <img width="687" height="182" src= IMG2.jpg title="Breadth-first search">
</p>

<p align="center">
  <img width="687" height="182" src= img3.jpg title="Breadth-first search">
</p>

**CSP (Constraint Satisfaction Problem)** é um conceito importante na inteligência artificial que consiste em um problema em que o objetivo é encontrar uma atribuição de valores às variáveis (Conjunto de atributos que recebem valor) de um domínio (conjuntos de valores possíveis para cada variável.), de modo que todas as restrições (São as condições que devem ser satisfeitas pelas combinações de valores atribuídos às variáveis) sejam satisfeitas, são muito utilizados em problemas complexos de inteligência artificial.

Os problemas de satisfação de condições possuem algumas caracterizações já apresentadas as quais são um conjunto dominio de valores possiveis, um conjunto de todas as variaveis é um conjunto de condições, dentro dos diversas condições podemos classificar em tipos que são **restrições unarias** que são restrições que limitam ou especificam apenas uma variavel, **restrições binarias** que limita ou especifica duas variaveis, **restrições globais** que limitam ou espeficam mais de duas variaveis **restrições numéricas** restrições que se dão por meio de relações matematicas e **restrições condicionais** que são restrições ativadas por meio de certas condições.

Nesse tópico de problemas de satisfação de condições, algo muito importante são as **propagações de condições** que no contexto diz respeito a transmição das condições é informações nas variaveis do problema, podem ser uteis para se limitar o espaço de busca é propriedades do codigo, pode ser uma propagação local ou global das variaveis.

As **consistências** são a forma de administração do problema de satisfação,  na **consistência de nó** cada variavel é verificada para garantir a consistência, na **consistência de arco** a verificação se dá por meio de pares de variaveis, a **consistência de trajeto** verifica conjuntos de variaveis, a **consistência k** verifica a consistência entre conjuntos de k variaveis é a **consistência global** verifica todas as variaveis.

O **algoritmo AC-3 (Arc-Consistency 3)** é um algoritmo usado na resolução de problemas de restrições. O algoritmo AC3 reduz os domínios de valores das variáveis em problemas de restrição, eliminando as inconsistências de acordo com o que se foi especificado pelo projetista. A consistência do arco é definida como: para cada par de variáveis conectados por restrição binário, o arco (X,Y) é consistente se para cada valor de X existe um valor de Y que satisfaz as especificações.


**Pesquisa backtracking CSP:** por meio de técnicas buscamos soluções a variáveis que não foram atribuidas durante a solução do problema. Essa pesquisa dita backtracking utiliza de tais técnicas por meio do encontrado na Caso retornando ou uma outra solução ou uma falha. As técnicas são de diversas formas que se organizam em ordenação de execução é de maneira sequêncial, estática, aleatório ou qualitativa e entre outras maneiras. Entre os métodos de pesquisa estão interleaving, parallellizing e combining que podem ser combinadas para encontrar a solução.

Abaixo um exemplo de codigo de backtracking csp.

<p align="center">
  <img width="687" height="182" src= img4.jpg title="Breadth-first search">
</p>
<p align="center">
  <img width="687" height="182" src= img5.jpg title="Breadth-first search">
</p>

**Busca local para CSP:** pega as variáveis que ainda possuem inconsistência é se checa as heuristicas para verificar as variáveis de minimizando os estados em busca aleatória e assim realizando uma resolução possível minimizando o menor número de regras possíveis.

Abaixo um exemplo de codigo de backtracking csp.

<p align="center">
  <img width="687" height="182" src= img6.jpg title="Breadth-first search">
</p>

<p align="center">
  <img width="687" height="182" src= img7.jpg title="Breadth-first search">
</p>

No problema de satisfação de restrições temos as **estruturas** do codigo, que é responsavel pela modelagem é resolução do problema o problema pode ser colocado em uma arvoré contendo um nó raiz o qual se começara o problema, os nós filhos que descendem dos nós pais, os caminhos que é a conexão entre dois nós é a hierarquia ue coloca cada nó e camiinho em suas devidas posições ou classificações, podendo as arvores se decompor em arvores menores é assim dividir a constituição do problema.

<p align="center">
  <img width="687" height="182" src= img1.jpg title="Breadth-first search">
</p>

<p align="center">
  <img width="687" height="182" src= img8.jpg title="Breadth-first search">
</p>

As aplicações dos problemas de satisfação de condição por exemplo tem muitas aplicações empresariais como agendamentos e planejamentos de qualquer tipo em um evento ou transporte público por exemplo, alocação de recursos atribuição de recursos a maquinas para disciplina, roteamento e entrega planejamento de rotas ou tarefas para entrega, design e layout da empresa ou dos sites podem ser mais bem administrados e diagnosticos é soluções de problemas nas diversas maquinas.
