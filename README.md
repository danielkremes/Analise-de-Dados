# Vender Bermudas
## Aumentar numeros de vendas
- Base: Vendas.xlsx
## Quantitidades de lojas
- 5

## Trazer base para dentro do python e ver o que tem dentro dela
`import pandas as pd` - biblioteca para fazer analise

`tabela = pd.read_excel("Vendas.xlsx")` - lendo o arquivo de excel que é a nossa "base" e criando a "váriavel" que sera usada como base para as "analises"

`display(tabela)` - disponiblizando dados da nossa base
- Exemplo base
  
![snapshot base](https://github.com/user-attachments/assets/35e5be86-2889-404d-a51f-b4f32493ca8d)

# Pegar panorama geral da empresa
## Ver faturamento total da empresa

`faturamento_total = tabela['Valor Final'].sum()` - criando faturamento total de todas as lojas

`print(faturamento_total)` - disponibilizando faturamenteo total de todas as lojas

![image](https://github.com/user-attachments/assets/afeb4d86-c24f-4383-b53d-e1ebb358f9ee)


# Analise TOP DOWN 

`faturamento_por_loja = tabela[['ID Loja','Valor Final']].groupby('ID Loja').sum()` - criando faturamento de cada loja

`display(faturamento_por_loja)` - disponibilizando faturamenteo de cada loja

# Entrar no detalhe de cada loja

`faturamento_loja_por_produto = tabela[['ID Loja','Valor Final','Produto']].groupby(['ID Loja','Produto']).sum()` - criando faturamento de cada loja e agrupando os produtos com seus numeros de vendas

`display(faturamento_loja_por_produto)` - disponbilizando a informação de cada loja com seus produtos vendidos

![image](https://github.com/user-attachments/assets/be79bac5-fe42-4356-9648-1f00fbb89cc2)

![image](https://github.com/user-attachments/assets/17b8b3b8-2b7a-410a-a4ce-acf24d890423)






