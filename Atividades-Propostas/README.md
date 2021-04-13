# SQL

## Atividades Propostas

### Exercícios Resolvidos

1 ) Considere um banco de dados relacional e as tabelas seguintes que fornecem detalhes acerca de clientes, caminhões e encomendas. As encomendas são solicitadas por clientes e transportadas por caminhões.

```"
CLIENTE (
    cli_id, 
    cli_nome, 
    cli_endereco
)

CAMINHAO (
    cam_id, 
    cam_placa
)

MOTORISTA (
    mot_id, 
    mot_nome, 
    cam_id, 
    turno_trabalho
)

ENCOMENDA (
    enc_id, 
    mot_id, 
    cli_id, 
    enc_data_solicit, 
    peso, 
    enc_data_hora_receb
)
```

Escreva comandos SQL para as seguintes necessidades:

a) Selecionar destinações de encomendas que recebem mais do que 10 pacotes.  

<!--https://www.devmedia.com.br/sql-select-guia-para-iniciantes/29530-->
```"
SELECT C.Destino, E.Encomenda, COUNT(*)
FROM CLIENTE C
INNER JOIN ENCOMENDA E
ON C.cli_id = E.cli_id
HAVING COUNT(*) >= 10
GO
```

b) Selecionar nome dos clientes que encomendaram pelo menos 1 pacote de mais de 1 Kg para destino ‘São Paulo’.  

```"
SELECT C.Nome_Cliente, E.Encomenda, E.Peso
FROM CLIENTE C
INNER JOIN ENCOMENDA E
ON C.cli_id = E.cli_id
E.peso >=1
GO
```

c) Selecionar o endereço dos clientes e a placa dos caminhões cujo pacote foi entregue por um motorista chamado 'Carlos Augusto Martins'.  

```"
SELECT C.Nome_Cliente, C.Endereco, E.Placa, M.Nome_Motorista
FROM CLIENTE C
INNER JOIN MOTORISTA M
```

d) Selecionar os 3 maiores clientes em fator de peso de encomenda acumulada.  

```"
```

e) Selecionar o id e a data/hora do recebimento das encomendas cujos motoristas que as entregaram trabalham no turno 'Diurno', a placa do caminhão tenha final '68' e que o cliente tenha feito duas ou mais encomendas  

```"
```
