# Exercício 2
Crie o seguinte endpoint com query builder:

## Get Purchase by id
- method HTTP (GET)
- path ("/purchases/:id")
- response
  - status 200
  - um objeto contendo:
    - id da compra
    - valor total da compra
    - quando foi criada
    - status do pagamento
    - id de quem fez a compra
    - email de quem fez a compra
    - nome de quem fez a compra
