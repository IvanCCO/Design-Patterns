# Chain of Responsability

Um design pattern comportamental, que serve para termos uma cadeia (chain) de objetos,
que o cliente não sabe quem tratará a solicitação, e a solicitação vai sendo passada
de objeto em objeto até um trata-lo.

## Use Case:

(Exemplo da cabeça que não foi validada)
Trazendo para o contexto de microservicos, digamos que temos 3 microservicos que conseguimos
capturar os dados do cliente:

- Service João
- Service Pedro
- Service Miguel

Digamos que o o cliente precise saber os dados do cliente, ele envia para nossa cadeia um método
`getClientData(userId)` e espera como retorno os dados do cliente que está sendo buscado.
Quando a solicitação entra na cadeia(chain) primeiro ele tenta buscar o dado do cliente no João,
e João tem uma referência para o próximo serviço, então se nossa solicitação der um HTTP status
500 por exemplo (server error -> digamos que esse status signifique o serviço está indisponível)
ele vai mandar a mesma solicitação para o próximo da cadeia.

## Implementação

Para implementarmos o **pattern** precisamos primeiro de uma interface que vai implementar nossos handlers\*

\_\_

- - Handlers objetos que executam a operação da nossa cadeia
