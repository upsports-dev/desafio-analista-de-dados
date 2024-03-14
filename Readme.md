<div>
   <img src=".github/logo-mini.png" height="30">
</div>

# Desafio de análise de dados

## Recursos
### Banco de dados com acesso a tabelas de clientes e apostas.
```
Postgresql
Host: 144.22.211.147
Port: 5436
User: bear
Password: dev!!!00
Database: upbet
```
Utilize as credenciais fornecidas para acessar o banco de dados PostgreSQL. <br>
Explore as tabelas relacionadas aos clientes e apostas para obter informações relevantes e realizar a consulta das somas de apostas dos clientes.


```diff
- Não há necessidade de criação de tabelas, usar os dados que já existem no banco.
```

### CSV de pagamentos dos afiliados. [Baixe aqui](/affiliates.csv)

!No CSV estão disponíveis as informações dos dados de pagamento e do cliente de cada afiliado.
 
## Objetivo
- Gerar um novo relatório de pagamento dos afiliados.
- Calcular a soma total de apostas do cliente no banco de dados de cada afiliado encontrado no arquivo CSV.
- Utilizando os totais das apostas e os dados da tabela limites, determinar a porcentagem aplicada ao pagamento final.
- Determine a porcentagem necessária para calcular o valor de acréscimo com base nas  informações fornecidas na tabela limites.
- Aplique a porcentagem encontrada ao valor na coluna "pagamentos" do CSV para obter o pagamento final.
- Usar alguma ferramente de BI (Databricks, Tableau, Apache Spark, Python Pandas e Jupiter) ou relacionadas.
- No assunto do email coloque essa chave [Desafio-Dados]. 

## Cálculo do pagamento

`(Porcentagem encontrada / 100) * (Coluna pagamentos do csv)`

### Exemplo
```
Para uma soma total de apostas de R$340 a porcentagem aplicada será de 42%.
O valor está dentro do limite de R$444.
```

| Valor  | Porcentagem  |
|--------|--------------|
| 120    | 8%           |
| 286    | 16%          |
| 310    | 35%          |
| 444    | 42%          |
| 540    | 60%          |

Tabela de exemplo, para realizar o cálculo utilize a tabela `limits` do bando de dados.

#### * Valores maiores que R$500 é aplicado 50%

## Resultado final
### Dados essenciais no relatório
```
ID de afiliado (affiliate_id) - CSV
ID do usuário (customer_id) - (obtida do banco de dados)
Valor do pagamento - CSV
Soma das apostas do cliente - (obtida do banco de dados)
Porcentagem do acréscimo - (calculada com base na tabela limits)
Pagamento final - (resultado da aplicação da porcentagem ao valor do pagamento do CSV)
```

## Diferencial
- Implementação ou integração de ferramenta para visualização do relatório final.

## Pontos que devem ser mostrados:

- Consulta somando as apostas dos clientes.
- Estratégia utilizada para obter a porcentagem que o pagamento se qualifica utilizando a tabela limits.
- Como foi realizado o cálculo de acréscimo do pagamento final
Apresentação dos novos resultados.
- Atenção ao enunciado do desafio.

## Envio do projeto / Dúvidas
- Arquivos
- Ferramentas
- Imagens
- Consultas SQL


**Enviar para o email [dev@upbet.com](mailto:dev@upbet.com)**
