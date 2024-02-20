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

Digamos que o João
