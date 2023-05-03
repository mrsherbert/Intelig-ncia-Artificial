# Algoritmos de busca

Nessa aula basea-se principalmente em agentes de solução de problemas que são agentes baseados em objetivos, que usam a representação atômica para chegar ao resultado, é como dito anteriormente é uma representação indivisivel e sem atributos contidos.

Existem basicamente dois tipos de problemas, o que pode ser resolvido de modo deterministico e esse pode-se simplesmente integrar as ferramentas computacionais já provenientes tranquilamente, é o segundo que se trata da resolução por meio de um processo de pesquisa e esse já se necessita de uma inteligência artificial com metódos de busca.

O primeiro passo para se encontrar uma solução é necessario estabelecer o objetivo que se deseja, é logo em seguido implementar o metódo de busca. Os estado são as possibilidades é o objetivo é exatamente um desses estados que se deseja alcançar apartir de um estado inicial, e as ações são as transições de estados por meio da função definida entre os estados.Caminho é o percurso entre estados, passando do estado inicial até o objetivo pelos diversos outros estados, passando pelo espaço de estados.

## Busca cega

A busca cega é uma busca que se resume basicamente a fazer com que o problema  se transforme em um problema de percorrer um espaço de estados, que por meio do estado inicial percorre os caminhos até o estado final desejado, para isso pode-se fazer com que execute o mesmo com o menor custo, para tudo isso pode se implementar diferentes estratégias, que podem ser avaliadas de acordo com suas especificações e desempenho, que será visto depois.

