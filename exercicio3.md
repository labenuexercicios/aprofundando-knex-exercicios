# Exercício 3
Refatore o endpoint criado no exercício anterior para que o resultado bem sucedido também retorne a **lista de produtos** que tem relação com a compra pesquisada.


## Exemplo de saída (output)
```typescript
// GET /purchases/:id sendo id = "pur001"
// status 200 OK
{
  purchaseId: "pur001",
  totalPrice: 1321.25,
  createdAt: "2023-01-20 16:15:22",
  isPaid: false,
  buyerId: "u002",
  email: "fulana@email.com",
  name: "Fulana",
  productsList: [
    {
      id: "p002",
      name: "Teclado gamer",
      price: 200.00,
      description: "Com uma estrutura de alumínio sólido, esse teclado foi projetado para estabilidade quando as teclas estão voando rapidamente.",
      imageUrl: "https://picsum.photos/200",
      quantity: 2
    },
    {
      id: "p003",
      name: "Mouse gamer",
      price: 300.00,
      description: "Projetado para conforto, esse mouse possui empunhaduras de borracha em seu redor para controle adicional.",
      imageUrl: "https://picsum.photos/200",
      quantity: 3
    },
    {
      id: "p005",
      name: "Pasta térmica",
      price: 21.25,
      description: "A Pasta térmica é um produto de alta performance, indicado para ser aplicado em processadores de notebooks e computadores, ela é altamente eficiente no resfriamento do processador do seu notebook e PC.",
      imageUrl: "https://picsum.photos/200",
      quantity: 1
    }
  ]
}
```

## Dicas
Esboce o algoritmo imaginando como você pode modelar os dados e ter a saída esperada. <br>
Uma solução simples é criar duas requisições separadas no banco de dados:
1. uma para o que você já fez no exercício anterior;
2. e outra para buscar os dados específicos de cada produto baseado na sua id.

_Você já tem o conhecimento e a prática necessária para fazer cada passo separado, o desafio agora é juntar tudo em um único fluxo e unir com a manipulação de arrays e objetos no typescript para modelar a estrutura da resposta._
