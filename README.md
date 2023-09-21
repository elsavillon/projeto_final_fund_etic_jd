<h1> Análise de dados aplicada à base Pólis PCDaS</h1>

O conteúdo proposto é exigência para o projeto final da disciplina de Fundamentos e Ética no Jornalismo de dados, ministrada por Luiz Fernando Toledo e Natalia Mazotte para o primeiro trimestre do curso de Jornalismo de Dados, Automação e Data Storytelling do Insper.

A base escolhida oi a Pòlis PCDaS, da Fiocruz, disponibilizada no seguinte [portal](https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/), por sua vasta complexidade e muitas variáveis disponíveis em todos os municípios brasileiros, com última atualização em outubro de 2022 . 

A Plataforma de Ciência de Dados à Saúde é a autora da base de dados, mantida pelo time de Engenharia de Governança e Engenharia de Dados e há um [dicionário de variáveis](https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/dicionario-de-variaveis/). A documentação dos dados está disponível no [site](https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/documentacao/).

Os dados foram obtidos pelo IBGE e a Secretaria de Avaliação e Gestão de Informação, tratados e enriquecidos por meio de uma metodologia própria da ETL da PCDas. Segundo o site da plataforma: "As colunas com nomes em MAIÚSCULO representam dados originais advindos do IBGE, Secretaria de Avaliação e Gestão da Informação ou DATASUS e colunas com nomes iniciando em minúsculo representam dados resultantes de transformação, enriquecimento ou cálculo da PCDaS", segundo informações no próprio [site](https://pcdas.icict.fiocruz.br/conjunto-de-dados/polis-pcdas/).

<h2>Perguntas feitas à base</h2>

Pensando na limpeza e análise dos dados a ser feita, foram pensadas as seguintes questões:

<li>Qual é o município com a maior taxa de suicídios a cada 100 mil habitantes?</li> 
<li>Essa taxa pode ter sido influenciada pelo tamanho do município?</li> 
<li>Quais são os 10 municípios com a maior taxa de suicídios a cada 100 mil habitantes?</li> 
<li>Onde estão localizados estes municípios?</li> 
<li>Há concentração em algum estado? E região?</li> 

<h2> Etapas no Orange</h2>

Para a seleção e limpeza de dados, foi utilizado o Orange, conforme o [documento anexo](https://github.com/elsavillon/projeto_final_fund_etic_jd/blob/main/suic%C3%ADdios_final.ows) a este repositório, seguindo as seguintes etapas

<li>Após abrir o arquivo completo, a primeira etapa foi usar um Data Table para checar se todos os dados foram carregados corretamente.</li> 

<li>A partir disso, começamos a trabalhar especificamente em cima dos dados de interesse. Usamos o widget “select columns” e selecionamos “tx_obitos_suicidio_2019”, “uf_SIGLA_UF” e mun_MUNNOME.</li> 

<li>Criamos outra data table, já com os dados filtrados. Ordenando os municípios por ordem decrescente de taxa de suicídio, chegamos à conclusão de que os cinco maiores índices ficam no Rio Grande do Sul.</li> 

<li>Depois usamos o widget “group by” para fazer um agrupamento por estado, usando a média da taxa em cada unidade da federação. Como esperado, o RS apareceu na primeira colocação, seguido por SC, PI e PR.</li>  

<li>Por fim, acrescentamos também um filtro para analisar apenas cidades com pelo menos 10 mil habitantes, como forma de evitar possíveis distorções na taxa em cidades muito pequenas. Esse é o caso da primeira colocada do ranking, Capão Bonito do Sul, que tem uma taxa de 180 suicídios/100 mil habitantes – muito influenciada pelo fato de ser um município com menos de 2 mil habitantes). Mesmo com esse filtro, RS e SC seguem nas duas primeiras colocações.</li>

<h2>Resultados da Análise</h2>

Foi observado que o Rio Grande do Sul é o estado com o maior número de suicídios: média de 17.3 a cada 100 mil habitantes. Em segundo lugar, está Santa Catarina em segundo lugar, com 15,2 a cada 100 mil habitantes e Paraná em quarto lugar, com 10,6 a cada 100 mil habitantes.

Os cinco primeiros municípios com a maior taxa de suicídios estão localizados no Rio Grande do Sul, além de dois adicionais entre os dez primeiros, conforme relação abaixo:

1 - Capão Bonito do Sul (RS)
2 - Nicolau Vergueiro (RS)
3 - Sério (RS)
4 - Novo Tiradentes (RS)
5 - Cristal do Sul (RS)
6 - Mundo Novo (GO)
7 - Sete de Setembro (RS)
8 - Engenho Velho (RS)
9 - Lajeado (TO)
10 - Prata do Piauí (PI)

Mesmo com o filtro para cidades com mais de 10 mil habitantes, Rio Grande do Sul continua na primeira posição, seguido de Santa Catarina. Em relação aos municípios, Vera Cruz (RS) aparece em quarto lugar e Sobradinho (RS)  em quinto, e Dionísio Cerqueira (SC), em oitavo, dentre as 10 primeiras.

<h2>Sugestão de pauta</h2>

Entender por que os habitantes da região sul do país representam os maiores índices de suicídio. 

<h2> Bases complementares </h2>

Outras possibilidades para dar andamento à pauta seriam bases de dados complementares com faixas etárias e gêneros que pudessem dar um recorte mais específico sobre a taxa de suicídios por localidade.

<h2> Fontes sugeridas</h2>

<li>Christian Dunker: psicanalista e professor Titular do Instituto de Psicologia da USP, junto ao Departamento de Psicologia Clínica, obteve o título de Livre Docente em Psicologia Clínica após realizar seu Pós-Doutorado na Manchester Metropolitan University</li>

<li>Lorival Blanco, presidente do Centro de Valorização à Vida (CVV)</li>

<li>Centro Estadual de Vigilância em Saúde do Rio Grande do Sul</li>

<li>Kátia Rodrigues, psicóloga da Política de Saúde Mental do Departamento de Atenção Primária e Políticas de Saúde (DAPPS) da Secretaria Estadual da Saúde do Rio Grande do Sul</li>

<li>Centro de Atenção Psicossocial (CAPS)</li>

<li>Responsável do IBGE pela contrução da base de dados</li>

<h2>Membros do grupo</h2>

<li>Beatriz Capirazi</li>
<li>Elsa Villon</li>
<li>João Barbosa</li>
<li>Laura Intrieri</li>
<li>Marcos Cony</li>
