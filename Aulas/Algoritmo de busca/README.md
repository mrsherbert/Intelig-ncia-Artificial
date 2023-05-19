# Algoritmos de busca

Nessa aula basea-se principalmente em agentes de solução de problemas que são agentes baseados em objetivos, que usam a representação atômica para chegar ao resultado, é como dito anteriormente é uma representação indivisivel e sem atributos contidos.

Os agentes de solução de problemas são agentes de objetivo que por meio das diversas possibilidades possíveis pode decidir o que fazer por meio da comparação e busca, com tal processo vizando encontrar um estado objetivo com o menor custo possivel.

Existem basicamente dois tipos de problemas, o que pode ser resolvido de modo deterministico e esse pode-se simplesmente integrar as ferramentas computacionais já provenientes tranquilamente, é o segundo que se trata da resolução por meio de um processo de pesquisa e esse já se necessita de uma inteligência artificial com metódos de busca.

Existem ainda dois possíveis tipos de sistemas que podem ser encontrados, os de malha aberta ou de malha fechada, os sistemas de malha aberta não tem realimentação com os vizinhos é assim sendo a saída será proporcional apenas as entradas, e os problemas de malha fechada contém essa realimentação entre os estados é desse modo dependem das condições dos estados e condições iniciais bem como as entradas

O primeiro passo para se encontrar uma solução é necessario estabelecer o objetivo que se deseja, é logo em seguido implementar o metódo de busca. Os estado são as possibilidades é o objetivo é exatamente um desses estados que se deseja alcançar apartir de um estado inicial, e as ações são as transições de estados por meio da função definida entre os estados.Caminho é o percurso entre estados, passando do estado inicial até o objetivo pelos diversos outros estados, passando pelo espaço de estados.

## Busca cega

A busca cega se trata basicamente de uma busca ao qual inicialmente não se tem um direcionamento do que será feito, sendo assim terá que se usar de algumas estrategias como método de resolução, assim se resume basicamente a fazer com que o problema  se transforme em um problema de percorrer um espaço de estados, que por meio do estado inicial percorre os caminhos até o estado final desejado, para isso pode-se fazer com que execute o mesmo com o menor custo, para tudo isso pode se implementar diferentes estratégias, que podem ser avaliadas de acordo com suas especificações e desempenho, que será visto depois.

### Busca em largura /  Breadth-first search

A busca em largura busca apartir de um estado meta é vai visitando seus estados vizinhos. Inicialmente a busca começa no estaco inicial é vai percorrendo todos os nós que se encontram logo abaixo, partindo dos nós abaixo vai percorrendo os nós mais abaixo e seus respectivos vizinhos, e assim sucessivamente até que tenha alcançado o objetivo. O algoritmo será satisfeito perfeitamente, alcançara o objetivo com o menor custo possível, entretanto será consumido bastante memória RAM.

<p align="center">
  <img width="687" height="182" src= BLA.jpg title="Breadth-first search">
  <h6 align="center">Breadth-first search</h6>
</p>


### Busca em custo uniforme / Uniform-cost search

Esse tipo de busca visa expandir os nós de acordo com o menor custo, sendo assim se busca o ramo com menor custo é o vai expandindo, mas a medida que o mesmo tem maior custo que outro ramo de nó, então se muda para o de menor custo é assim sucessivamente até que se chegue ao estado objetivo, seguindo uma ordem de expansão. A busca em custo uniforme pode não ser plausivel quando se tem muito nós e levar a caminhos não desejaveis, assim sendo pode consumir muito tempo.

<p align="center">
  <img width="677" height="267" src= BCU.jpg title="Uniform-cost search">
  <h6 align="center">Uniform-cost search</h6>
</p>

### Busca em profundidade /  Depth-first search

A busca em profundidade consiste no algoritmo aprofundar seus nós a medida em que se tem nós ainda não explorados é se parar assim que o mesmo não tiver mais nós abaixo, a medida que não se tem mais nós em profundade o mesmo volta ao nó anterior é procura se tem é assim sucessivamente seguindo em profundidade. A vantagem da  busca em profundidade é que a mesma é capaz de procurar soluções um espaço de estados enorme, as desvantagens são de que ela não vai procurar sempre o menor custo é além disso pode ficar presa em sistemas de malha fechada.

<p align="center">
  <img width="677" height="454" src= BPR.jpg title="Depth-first search">
  <h6 align="center">Depth-first search</h6>
</p>

## Busca informada

Ao contrario da busca cega, onde não se sabe qual o melhor nó para se começar a busca, na busca informada se aproxima tal informação com base em informações que são dadas a maquina,embora isso seja bom devido ao fato de não ser uma busca exaustiva não se tem certeza do menor custo do programa nem mesmo outas soluções. Tais informações que são dadas previamente ao programa são chamadas de informações heuristicas ela geralmente informa uma distância do inicio até o destino como forma de estimativa para tal, isso com base em funções heuristicas, heuristicas são algoritmos que embora se use para a exploração o mapeamento é dado com base em informações pre-estabelecidas.

## Funções heurísticas

As funções heuróisticas são funções que descrevem a inteligência artificial o quão longe o mesmo está do objetivo, sendo utilizadas amplamente em buscas que envolvem um grande espaço de estados, podendo auxiliar fortemente o encontro das soluções em menos tempo é mais eficientemente, existem dois tipos de funções heurísticas, sendo funções heurísticas admissiveis se ela não superestima os caminhos para solução, é funções heurísticas consistentes que é uma função heurística que a estimativa de custo da função heurística do nó inicial para um sucessor nunca é maior do que a soma do custo do nó inicial até o sucessor e a estimativa de custo da função heurística do sucessor para o objetivo, tais funções podem ser representadas por f(n) onde n é o nó da arvore é sendo assim f será portanto a relação que controla tal heurística.

### Busca gulosa / greedy best-first search

A busca gulosa tem como heuristica expandir os nós que estão mais proximos ao nó original, a distância do nó, desse modo o codigo não encontra realmente o melhor é menos custoso caminho, isso porque não leva em conta o custo total do inicio até o objetivo é muitas das vezes escolhe o proximo caminho com base em uma média dos caminhos proximos.

<p align="center">
  <img width="675" height="700" src= BGU.jpg title="greedy best-first search">
  <h6 align="center">greedy best-first search</h6>
</p>

### Algoritmo A* / A* search

O algoritmo A expande busca expandir o nó que está com menor valor de custo, usando para isso uma função heuristica f(n)=g(n)+h(n), o algoritmo A* tem muitos beneficios incluindo ser bem preciso uma vez que é um algoritmo muito mais preciso que a busca gulosa, eficiência devido ao fato de priorizar a melhor e promissora em em direção a solução é o fato de ser muito adaptavel a todo objetivo que se deseja.

<p align="center">
  <img width="543" height="787" src= APS.jpg title="A search">
  <h6 align="center">greedy best-first search</h6>
</p>

### RECURSIVE BEST-FIRST-SEARCH (RBFS)

Este é um algoritmo a* que tem como ideia limitar o número de nós da memoria, guardando apenas aqueles que foram expandidos, funciona expandindo o nó mais promissor, usando para isso uma função heuristica é por meio disso utiliza a busca em profundida limitada (depth-limited search)  para explorar os subcaminhos desse nó, caso a depth-limited search retornar resultado então se termina a busca, caso contrario novamente se inicia a busca, tal codigo tem os beneficios de evitar expansões desnecessarias é ser mais eficiente que grande parte de outros mecanismos de buscas.

### Procura em ambientes complexos

Um ambiente complexo é um ambiente com diversas variaveis que estão em constante mudança, podendo apresentar sensores ou atuadores com defeito, bem como incertezas de acordo com o ambiente ou de acordo com o aparelho, assim o tornando muito dificil, a procura em ambientes complexos é uma área da inteligência artificial que se concentra em desenvolver algoritmos para o mesmo, o que se importa mais é em se chegar a solução para o problema em que estamos interessado e não como chega-se nele. Para aprender a se desenvolver os algoritmos desse tipo de busca podem, fazer buscam em arvores proximas, aprender por meio de reforço, utilizar busca de monte carlo ou por meio de algoritmos genéticos.

### Busca local

A busca local se concentra em operar por meio dos estados vizinhos a uma resposta sem acompanhar os caminhos nem os estados já alcançados, que se deu sendo assim buscando encontrar a melhor solução, eles não se concentram em se encontrar a parte menos cara, entretanto em te dar uma solução razoavel usando pouca memória. Pode-se usar de diversas estratégias de busca local, Hill Climbing - a mesma se concentrar em encontrar a solução de uma função heurística que define um objetivo é desse modo se encontra-ra o maximo do picoda função objective x state, Gradiente Descent - por meio de uma função heurística que define um custo se busca encontrar o menor pico da função objective x state, Bean Search - essa tecnica consiste em manter varias soluções é buscar as soluções vizinhas de modo a encontrar a melhor possivel, Simulated Annealing - utiliza de probabilidades vizinhas as soluções para encontrar a melhor solução, algortimos géneticos - será discutida a seguir.

### Algoritmos genéticos

São uma técnica de busca inspirada na seleção natural é na genética, são algortimos que buscam uma população de soluções e evoluindo essa população ao longo de várias gerações carregam informações dos genés anteriores. A cada geração, as soluções melhores são selecionadas para se tornarem pais de uma nova geração, enquanto as soluções piores são eliminadas, podendo ocorrer mutações durante a combinação dos DNAs, para essa analogia entre os mesmos se utiliza dos parâmetros; tamanho da população, representação de cada individuo, número de parentes, seleção, processo de recombinação, taxa de mutação e nova geração, o método se dá por meio do seguinte, primeiro se inicializa a população com diversas combinações possível de maneira a ter diversas posições é exemplos possiveis, com isso avalia-se a possivel solução por meio dessas populações, seleciona as mais aptas a proxima geração, realiza a combinação genética, avalia a nova geração em busca da solução é retoma o processo de combinação caso não a alcançou.