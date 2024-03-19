# Pizzaria  🍕🍔

Bem-vindo ao repositório da INNER JOIN - PIZZARIA! Aqui você encontrará os scripts SQL relacionados a uma pizzaria fictícia. Abaixo estão os principais recursos deste repositório.

## Arquivo SQL 📄

- [Script SQL](https://github.com/adsluizapaiva/script_pizzaria/blob/main/Script_Pizzaria_luiza.sql) - O arquivo SQL contém as tabelas e consultas relacionadas à pizzaria.

## Diagrama do Banco de Dados 📊

![Diagrama do Banco de Dados](https://github.com/adsluizapaiva/script_pizzaria/blob/main/Script_Pizzaria_diagrama.png)

## Consultas SQL 📝

Aqui estão algumas consultas SQL de exemplo que você pode executar no banco de dados da pizzaria:

### Clientes Que Mais Pedem 🍕

```sql
-- Exemplo: CLIENTE QUE MAIS PEDE
SELECT C.NOME AS NOME_CLIENTE, C.TELEFONE, pv.VLR_PEDIDO_VENDA
FROM PEDIDO_VENDA pv
INNER JOIN CLIENTE C ON C.COD_CLIENTE = pv.COD_CLIENTE;

```

### Todas as Cotações Realizadas 💱

```sql
-- Exemplo: TODAS AS COTAÇÕES REALIZADAS
SELECT C.VLR_COTACAO, F.NOME AS NOME_FORNECEDOR, P.NOME AS NOME_PRODUTO
FROM COTACAO C
INNER JOIN FORNECEDOR F ON F.COD_FORNECEDOR = C.COD_FORNECEDOR
INNER JOIN PRODUTO P ON P.COD_PRODUTO = C.COD_PRODUTO;
```

### Produto Mais Comprado e Valor do Produto 💰
```sql
-- Exemplo: PRODUTO MAIS COMPRADO E VALOR DO PRODUTO
SELECT IPC.COD_PRODUTO, P.NOME AS NOME_PRODUTO, IPC.QTD_ITEM_PEDIDO_COMPRA, P.VLR_PRODUTO_COMPRA
FROM ITEM_PEDIDO_COMPRA IPC
INNER JOIN PRODUTO P ON P.COD_PRODUTO = IPC.COD_PRODUTO;
```

### Conclusão
Este trabalho faz parte do curso de Análise e Desenvolvimento de Sistemas da Faculdade Newton Paiva e foi desenvolvido por Luiza Paiva (ads.luizapaiva@gmail.com). Contribuições e feedback são bem-vindos para aprimorar ainda mais este projeto simulado.

Agradecemos por explorar o repositório do PIZZARIA!
```
