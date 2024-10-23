# Padrão Estrutural Bridge

## Explicação
A intenção do uso do Bridge é desacoplar a **abstração** da **implementação**.

Neste contexto, estamos nos referindo ao seguinte:

- **Abstração**: Código de alto nível que delega ações para outro objeto.
- **Implementação**: O código que realmente faz o trabalho.

## Exemplo
Vamos considerar um cenário para o uso do **Bridge**. Suponha que precisamos criar uma classe *Veiculo*, onde teremos dois tipos de veículos: **Elétricos** e **de Combustão**.

Se fizéssemos o código utilizando somente *Herança*, ele teria uma estrutura semelhante a esta:

![Problem-Bridge](imagens/problem.jpg)

Note que, ao estruturar o nosso código dessa forma, teremos problemas ao implementar mais tipos de veículos. Considere agora que, além de *Carros* e *Caminhões*, queremos também adicionar *Motos* **Híbridas** ao nosso código.

Não é um código escalável e também não é o que desejamos para nossas manutenções.

Em vez de *Herança*, por que não fazer uma relação de *Composição* entre *Veiculo* e *Motor*?

![Solution-Bridge](imagens/solution.jpg)

Agora temos a flexibilidade para implementar qualquer nova *feature* que for conveniente. Por exemplo, agora queremos implementar um *Veiculo* que utilize um *Motor* de **Hidrogênio**:

![Solution-Bridge](imagens/solution2.jpg)

Dessa forma, *Veiculo* e *Motor* podem escalar de forma independente e separada, sem que uma classe interfira na outra.
