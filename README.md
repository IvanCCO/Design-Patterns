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

### Relacionamento de classes

<p align="center">
  <img src="https://i.stack.imgur.com/jNyV5.jpg" width="25%" >
</p>

Relacionamento de classes são muito imporantes quando vamos falar de Design Patterns pois nos ajudam a identificar a "raiz" da classe/objeto
o seu tempo de vida e seu acoplamento com outras classes.

### Projetando o sistema para mudanças

Sempre faça um sistema com o pensamento de que o escopo inicial pode e vai mudar, e que mesmo que não mude na sua vez vai mudar na vez do próximo
então é sempre importante construir um sistema aberto para mudanças.

> "Um projeto que não leva em consideração a possibilidade de mudanças esta sujeito ao risco de uma grande reformulação no futuro"

- Um sistema não deve ter dependências muito acopladas, quando acoplamos demais o software ao SO ou Alguma API externa estamos ficando reféns
  dessa API, é importante projetar o sistema para limitar suas dependências de outras plataformas. Para isso existem padrões como Bridge

  > Não sei o quanto isso vale quando falamos dentro do contexto de microserviços e sistemas construidos em cima de fraweworks como o spring,
  > pois essa absrtação pode trazer mais dor de cabeça e acabar realizando um overenginneringn pesado para resolver um problema simples.

- Dependências de operações específicas, quando colocamos operações hard-coded torna-se mais dificil mudar a maneira que a solicitação é atendida
  em tempo de compilação e execução, para isso existem padrões como o (Chain of responsability, Command)

- **Dependências algoritmas**, quando temos algoritmos que com certeza vão ser mudados, ou que irão se estender, os objetos que dependem desse algoritmos
  também deverão ser alterados, portanto algortimos que serão alterados devem ficar isolados. Padrões que ajudam com isso são
  -> Strategy, Iterator, Builder, Template Method, Visitor

- Acoplamentos fortes entre classes fazem com que o sistema vire um só, e que seja dificil fazer uma mudança sem impactar diversos pontos do código, um acoplamento fraco faz com
  que seja menos provável que uma classe precise de outra para ser usada, isso faz com que, o sistema possa ser modificado mais facilmente.

- Estender a funcionalidade pelo uso de subclasses é algo perigoso, e que a ao decorrer do projeto pode se pegar tendo que criar
  mais e mais classes para atender uma operação simples, invés disso é melhor usar a **composição** para estender classes, pois dessa
  forma se cria uma alternativa mais flexível á herança para combinação de comportamentos. Porém o uso intenso de composição, pode
  deixar o projeto menos compreensível(e isso é algo muito importante).
