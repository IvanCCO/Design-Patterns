<p align="center">
  <img src="https://www.livropedia.com/imagens/livro-padroes-de-projetos-solucoes-reutilizaveis-de-software-orientados-a-objetos.jpg" width="25%" >  
</p>

# Padrões de Projeto - Soluções reutilizáveis de software orientado a objetos.

Esse repositório tem como objetivo ser um local de colocar em prática os aprendizados
derivados do livro **Padrões de Projeto**, onde irei colocar descrições sobre o Padrão apresentado
e uma implementação em Java do padrão.

## Como será abordado?

Os padrões nesse projeto estarão em um projeto Java, apenas para demonstrar um esboço da implementação, onde será separado cada padrão em pacotes diferentes,
com um texto MARKDOWN explicando o padrão e sua utilizadade, e trazendo um problema real, diferente do que foi abordado no livro, tentando ser algo mais
moderno e identificável no dia a dia.

## O que são Padrões de Projeto?

Padrões de projeto são soluções que foram previamente testadas e são adotadas por diversos desenvolvedores para resolver um problema,
mas isso não se limita a desenvolvimento de software.
Padrões facilitam no desenvolvimento de soluções e a comunicação sobre essas soluções, identificar e dar um nome a um padrão facilita
no seu melhoramento contínuo e uso.

No contexto de Engenharia de Software padrões são como "templates" que podem ser usados, e serem aptados ao domínio do negócio.
Onde esse template consegue ser facilmente(quando bem aplicado) identificado por outros desenvolvedores e assim conseguirem discutir sobre
e propor melhorias.

Padrões do projeto não são algoritmos prontos, que se pode deixar guardado no seu projeto para serem utilizados quando conveniente, eles são adaptáveis
ao contexto, e vários padrões podem interagir entre SI.

No caso dos livro, os padrões serão direcionados e explicados utilizando o conceito de POO (Programação orientada a objetos) e muitos padrões só são possíveis
por utilizar esse conceito, trazendo consigo Interfaces, Herança, Polimorfismo.

### Programe orientado a interface, não a implementação

Essa é uma das premissas mais básicas do livro pois com isso é possível expandir, e evitar over acoplamento entre os objetos.

Existem dois benefícios claros em manipulação de interfaces ao invés de implementação, são eles:

- Os clientes(quem utiliza a interface) permancem sem conhecimento dos tipos específicos dos objetos, contanto que o os objetos tenham aderência a interface
- Os clientes permanecem sem conhecimento das classes que implementam esses objetos. O cliente tem apenas conhecimento da classe abstrata que define a interface.

Não declarar variáveis como instâncias de classes concretas(implementação), faz com que seu código fique muito mais fácil de ser expandido, invés disso atribua para
essa variável o contrato que ela precisa, e deixe as implementações necessárias com esses contrato. Porém em algum momento é inevitável ter que instanciar uma implementação
mas para isso também existem padrões (os de criação) que ajudam a abstrair o processo de criação de objeto, dando diferentes maneiras de associar uma interface com a implementação
de forma transparente.

> Os padrões de criação asseguram que seu sistema esteja escrito em termos de interface, não de implementação.

### Relacionamento de classes,

<p align="center">
  <img src="https://i.stack.imgur.com/jNyV5.jpg" width="25%" >
</p>
