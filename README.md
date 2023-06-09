# skytef-product-rental

Esse foi um desafio que envolveu a criação de uma aplicação Java (Spring Boot) foram adotados conceitos fundamentais da linguagem Java.

## Durante o desenvolvimento, foram adotadas boas práticas de programação, como Clean Code e tratamento de exceções. Certifique-se de seguir essas práticas ao trabalhar com o código.

## Cenário: A empresa XYZ trabalha com aluguel de produtos que são utilizados em uma loja de eletronicos.

1. cada produto possui um valor cobrado por hora, o sistema aceita apenas valores inteiros para o campo hora.
2. funcionário recebe uma comisão baseada no valor total cobrado pelo produto.

## Produtos e comissões:
Para OCULOS_VR:
Preço por hora: R$50,00
Porcentagem funcionário: 15.6%

Para LAPTOP:
Preço por hora: R$50,00
Porcentagem funcionário: 15.6%

Para GAMING_CONSOLE:
Preço por hora: R$40,00
Porcentagem funcionário: 10.3%

Para PROJECTOR:
Preço por hora: R$25,00
Porcentagem funcionário: 9%

Para CAMERA:
Preço por hora: R$25,00
Porcentagem funcionário: 8.1%

## Descrição dos campos da classe ProductOrder.
1. userName: Login do usuário;
1. productType: Tipo do produto;
1. timeHour: Tempo em horas que o produto ficou locado;
1. productValue: Valor do produto por hora;
1. productTotal: Valor do produto vezes tempo em horas locado;
1. userAmount: Comissão a ser recebida pelo usuário(Funcionário);

## Exemplo:
Funcionário Pedro alugou o produto OCULOS_VR por 4h.
Pedro vai receber uma comissão no valor de R$31,20 pelo aluguel do produto OCULOS_VR.

JSON Request para criar um pedido:
```bash
{
  "userName": "João",
  "productType": "CAMERA",
  "timeHour": 16
}
```
JSON Response ao solicitar um pedido pelo userName:
```bash
[
    {
        "productType": "CAMERA",
        "timeHour": 16,
        "productValue": 400.0,
        "productTotal": 6400.0,
        "userAmount": 659.2
    }
]
```

## Testes Unitarios
Boas práticas de testes unitários foram empregadas, utilizando os frameworks JUnit e Mockito para construir e executar os testes. Isso inclui a criação de cenários de testes abrangentes para cobrir uma gama de situações, o uso de asserções para verificar os resultados dos testes e a criação de mocks de dependências para isolar o código sob teste.

## Tecnologias
Java 17, Spring Boot, Git, Spring Data JPA, JUnit, Mockito, Banco de dados H2, FlyWay para versionamento do banco de dados.
