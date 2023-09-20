Descrição da limpeza e análise de dados para o projeto final da discilplina.

Para o trabalho, foi escolhida a base da dados PolisPCDaS, da Fiocruz, disponibilizada em https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/, por sua vasta complexidade e muitas variáveis disponíveis para análise em todos os municípios brasileiros.  A Plataforma de Ciência de Dados à Saúde é a autora da base de dados, mantida pelo time de Engenharia de Governança e Engenharia de Dados. A última atualização aconteceu em outubro de 2021 e há um dicionário de variáveis disponível em https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/dicionario-de-variaveis/. A documentação dos dados está disponível em https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/documentacao/.

Os dados foram obtidos pelo IBGE e a Secretaria de Avaliação e Gestão de Informação, tratados e enriquecidos por meio de uma metodologia própria da ETL da PCDas. Segundo o site da plataforma: "As colunas com nomes em MAIÚSCULO representam dados originais advindos do IBGE, Secretaria de Avaliação e Gestão da Informação ou DATASUS e colunas com nomes iniciando em minúsculo representam dados resultantes de transformação, enriquecimento ou cálculo da PCDaS" (https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/ acessado em 20 set 2023, às 20h10).

Pensando na limpeza e análise dos dados a ser feita, foram pensadas as seguintes questões:

1) Qual é o município com a maior taxa de suicídios a cada 100 mil habitantes?
2) Essa taxa pode ter sido influenciada pelo tamanho do município?
3) Quais são os 10 municípios com a maior taxa de suicídios a cada 100 mil habitantes?
4) Onde estão localizados estes municípios?
5) Há concentração em algum estado? E região?

A partir disso, trabalhamos com o Orange, conforme o passo a passo abaixo:
1) Após abrir o arquivo completo no Orange, a primeira etapa foi usar um Data Table para checar se todos os dados foram carregados corretamente.

2)	A partir disso, começamos a trabalhar especificamente em cima dos dados de interesse. Usamos o widget “select columns” e selecionamos “tx_obitos_suicidio_2019”, “uf_SIGLA_UF” e mun_MUNNOME.

3)	Criamos outra data table, já com os dados filtrados. Ordenando os municípios por ordem decrescente de taxa de suicídio, chegamos à conclusão de que os cinco maiores índices ficam no Rio Grande do Sul.

4)	Depois usamos o widget “group by” para fazer um agrupamento por estado, usando a média da taxa em cada unidade da federação. Como esperado, o RS apareceu na primeira colocação, seguido por SC, PI e PR. 

5)	Por fim, acrescentamos também um filtro para analisar apenas cidades com pelo menos 10 mil habitantes, como forma de evitar possíveis distorções na taxa em cidades muito pequenas. Esse é o caso da primeira colocada do ranking, Capão Bonito do Sul, que tem uma taxa de 180 suicídios/100 mil habitantes – muito influenciada pelo fato de ser um município com menos de 2 mil habitantes). Mesmo com esse filtro, RS e SC seguem nas duas primeiras colocações.

Para dar andamento à pauta, seriam necessárias bases de dados complementares, que pudessem indicar um recorte por faixa etária, por exemplo.

Dentre as fontes sugeridas, estão:

Christian Dunker: psicanalista e professor Titular do Instituto de Psicologia da USP, junto ao Departamento de Psicologia Clínica, obteve o título de Livre Docente em Psicologia Clínica após realizar seu Pós-Doutorado na Manchester Metropolitan University.

Centro de Valorização à Vida (CVV)
Lorival Blanco, presidente do CVV

Centro Estadual de Vigilância em Saúde do Rio Grande do Sul

Secretaria Estadual de Saúde do Rio Grande do Sul
Kátia Rodrigues, psicóloga da Política de Saúde Mental do Departamento de Atenção Primária e Políticas de Saúde (DAPPS) da Secretaria Estadual da Saúde do Rio Grande do Sul

CAPS - Centro de Atenção Psicossocial

Especialista do IBGE que tenha sido responsável pelos dados da base

