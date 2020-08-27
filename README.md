# dio-restaurant

Este é um projeto simples de um restaurante utilizando uma arquitetura de microsserviços. Exitem 2 APIs (Garçom e App), onde o cliente pode fazer os seus pedidos. Essas APIs enviam o pedido para a cozinha, já separando o que é para o cozinheiro fazer e o que é para o barman fazer. Depois o cozinheiro e o barman enviam o pedido para o balcão, de onde o garçom pega e entrega na mesa, ou para o balcão do delivery, onde os pedidos são separados para serem entregues pelo motoboy.

![dio-restaurant (1)](https://user-images.githubusercontent.com/34447259/91495746-5f993700-e891-11ea-97fc-75dbbdcaf99e.jpg)

Os microsserviços são:

- [Garçom](https://github.com/felipe-tomino/dio-waiter)
- [Cozinha (Para o cozinheiro e barman)](https://github.com/felipe-tomino/dio-kitchen)
- [App](https://github.com/felipe-tomino/dio-delivery-app)

Todos foram feitos em [Node.js](https://nodejs.org/en/), utilizando o [Express](https://expressjs.com/) como servidor. A comunicação entre eles é feita utilizando [Kafka](https://kafka.apache.org/). Também foi utilizado o [Redis](https://redis.io/) para gerenciar os pedidos do [App](https://github.com/felipe-tomino/dio-delivery-app).

```JSON
{
  "id": "uuid",
  "table": 1,
  "address": "address",
  "food": ["food1", "food2"],
  "drinks": ["drink1", "drink2"],
}
```
