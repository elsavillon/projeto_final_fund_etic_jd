Descrição da limpeza e análise de dados para o projeto final da discilplina.

Para o trabalho, foi escolhida a base da dados PolisPCDaS, da Fiocruz, disponibilizada em https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/.
Após baixar o arquivo, foi feita uma análise pelo programa Orange, conforme o passo a passo abaixo:
1) Após abrir o arquivo completo no Orange, a primeira etapa foi usar um Data Table para checar se todos os dados foram carregados corretamente.

2)	A partir disso, começamos a trabalhar especificamente em cima dos dados de interesse. Usamos o widget “select columns” e selecionamos “tx_obitos_suicidio_2019”, “uf_SIGLA_UF” e mun_MUNNOME.

3)	Criamos outra data table, já com os dados filtrados. Ordenando os municípios por ordem decrescente de taxa de suicídio, chegamos à conclusão de que os cinco maiores índices ficam no Rio Grande do Sul.

4)	Depois usamos o widget “group by” para fazer um agrupamento por estado, usando a média da taxa em cada unidade da federação. Como esperado, o RS apareceu na primeira colocação, seguido por SC, PI e PR. 

5)	Por fim, acrescentamos também um filtro para analisar apenas cidades com pelo menos 10 mil habitantes, como forma de evitar possíveis distorções na taxa em cidades muito pequenas. Esse é o caso da primeira colocada do ranking, Capão Bonito do Sul, que tem uma taxa de 180 suicídios/100 mil habitantes – muito influenciada pelo fato de ser um município com menos de 2 mil habitantes). Mesmo com esse filtro, RS e SC seguem nas duas primeiras colocações.
