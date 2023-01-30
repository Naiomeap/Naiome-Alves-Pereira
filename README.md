# Trabalho Individual 1 
## Saúde Mental


  Um tema que vem sendo muito discutido no Brasil e no mundo, é a saúde mental. Após a pandemia do Covid 19 esse problema se tornou cada vez mais recorrentes e muitos estudos andam abordando as consequências ocasionadas por problemas mentais na vida do indivíduo como sua vida profissional, social, amorosa etc (Machado et al, 2022: doi 10.47626/1679-4435-2022-680; Pinho et al, 2021: doi 10.2196/24298).

  O contexto escolhido para a analise de dados foi um estado que fica na região sul do Brasil. O Paraná é um estado que possui 399 municipíos e é a 4º maior econômia do país. Com os dados disponibilizados pelo governo federal iremos analisar se há diferença entre esses municipios, se é possivel medir a saúde mental de uma determinada população e se ações de promoção a saúde, um conjunto de politicas, programas e plano de saúde pública que visa melhorar o bem estar e a qualidade de vida da população, podendo ser realizadas por individuos, coletivamente ou por organizações.

  O objetivo desse trabalho busca descobrir se quanto mais ações de promoção a saúde e mais profissionais relacionados a saúde mental melhor será a saúde mental da população.

  Foi criado para facilitar o entendimento um dicionário de dados, podendo ser visto a seguir:
  
Assist_Soc - Assistente Sociais

Psic - Psicólogo

Psiqui	- Psiquiatra

Acoes_prom	- Ações de Promoções e Prevenções a saúde

Acoes_comp - Ações Complementares de atenção a saúde

Ar_Ter_km2	- Área Territorial

Pop_Est - Estimativa da População

IDH	- Índice de Desenvolvimento Humano

PIB - Produto Interno Bruto Per Capita

O processo do desenvolvimento desse trabalho se deu da seguinte forma:

  Foi utilizado dados no Tabnet - DATASUS (Quantidade de Assistentes Sociais, Psicólogos, Psiquiatra, Ações de Promoções e Prevenções a Saúde e Ações Complementares de atenção a saúde, além da quantidade de atendimentos realizados nos anos de 2017, 2018, 2019, 2020 e 2021)  e do IBGE (Área Territorial, Estimativa da População, Índice de Desenvolvimento Humano e Produto Interno Bruto).
  
  Foi realizado a limpeza dos arquivos csv, eliminando cabeçalhos e rodapés e combinando mais de um banco de dados; houve tratamento de caracteres não numerais  e a codificação para latin-1.
  
  Na parte de pré-processamento foi criado 4 Data Frames e cada um referente a uma tabela, sendo: 
  
DF1 - Tabela referente a ocupações de niveis superior. Foi utilizada apenas as colunas referentes as profissões de assistente social, psicólogo e psiquiatra

DF2 - Tabela referente a copiladoss de dados da saúde de 2021. Foi utilizado os dados apresentados em ações de promoção e prevenção em saúde e
       ações complementares de atenção a saude

DF3 - Tabela referente a ações complementares da atenção a saúde. Foi utilizado os dados dos anos de 2017 a 2021 para uma melhor análise dos anos e as quantidade de medidas tomadas

Foi realizada a junção das 3 tabelas (ocupação nivel superior, copilados dados de saúde 2021 e ações complementares da atenção a saúde) tornando um único data frame, no qual as linhas são os municipios e cada coluna veio de diferentes data frame.

DF4 - Tabela referente a dados do IBGE. Dados utilizados da área territorial, estimativa da população, índice de desenvolvimento humano e produto interno bruto.

 Como a tabela possuía todos os municípios selecionei apenas os do estado do Paraná (Os municípios do Paraná começam com o número 41, pois é 4º região e o 1º estado); como também escolhi na tabela de profissionais disponibilizadas pelo governo os profissionais de assistência social, psicólogos e psiquiatras pois são os profissionais que lidam com saúde mental.

A análise descritiva e exploratória se deu da seguinte forma:

O data frame é composto por 15 variavéis distribuidas em 399 entradas. Os dados não apresentam nenhum dado nulo, e todas as colunas de números estão como números, sendo a única coluna de string a coluna dos municípios.

A média de psicologos nas cidades do estado do Paraná é de 13, porém o desvio padrão é de 81,26, sendo a quantidade maxima de profissionais no estado é de 1500. Em contra partida o número de psiquiatras é em média 1,28, com desvio padrão 11,27 e a quantidade máxima de profissionais é 217. 

Foi realizada um plot de correlação dos dados e retirado a parte de cima do gráfico para não ficar espelhada para uma melhor vizualização, assim sendo possivel analisar melhor as variavéis e podendo ser feito uma escolha mais assertiva de quais variáveis influenciam mais. Nesse gráfico conseguimos analisar que a coluna dos assistentes sociais se correlaciona bastante com psicólogos, um pouco menos com psiquiatras e média correlação com ações de promoção a saúde. E a linha de Assistentes sociais se correlaciona bastante com psicologos, um pouco a menos com psiquiatras e média correlação com ações promocionais. Nesse momento não foi correlacionado as colunas de 2017, 2018, 2019, 2020 e 2021, pois esses dados é referente a quantidade de ações complementares a saúde em cada cidade, e ela será usada no machine learning para conseguir achar um padrão.

Foi realizado um plot de psicólogos nos municipios com os seguintes intervalos: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 100, 250, 500, 1000, 1500

Foi realizado um plot de psiquiatras nos municipios com os seguintes intervalos: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100, 200, 250

Foi realizado um plot de assistente sociais nos municipios com os seguintes intervalos: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100, 250, 300

Foi realizado um plot de ações de promoção e prevenção na saúde nos municipios com os seguintes intervalos: 1500, 3000, 5000, 10000, 50000, 100000, 200000, 5000000

Foi realizado um plot de ações complementares na saúde nos municipios com os seguintes intervalos: 1500, 3000, 5000, 10000, 50000, 100000, 250000

Foi realizado um plot de área de território nos municipios com os seguintes intervalos: 170000,500000, 750000, 1000000, 1550000

Foi realizado um plot de estimativa populacional nos municipios com os seguintes intervalos: 10000,50000,100000,200000,500000,1500000

Foi realizado um plot de IDH nos municipios com os seguintes intervalos: 0, 3.5, 5.5, 7, 8, 10

Foi realizado um plot de PIB nos municipios com os seguintes intervalos: 170000, 300000, 500000, 750000, 1000000, 1550000

Os intervalos foram feitos para facilitar a visualização, por ser 399 cidades outros tipos de gráfico pode confundir a quem for ver a imagem. Porém o intervalo do indice de IDH foi feito em relação de como o indice é calculado e caracterizaado, sendo de 0,350 – 0,554 (baixo), 0,555 – 0,699 (médio), 0,700 – 0,799 (alto) e 0,800 – 1,000 (muito alto).

Irei selecionar um tipo de doença mental categorizando elas como baixa, média e alta e rodar os algoritmos de machine learning para verificar se o algoritmo encontra um padrão de ações de promoção e prevenção em saúde e a quantidade de profissionais disponiveis que possa ser usado para classificar de maneira automatizada, se a cidade terá uma baixa, média ou alta saúde mental. Com esses dados poderei criar uma proposta de intervenção seja do governo ou para empresas privadas, para melhorar a saúde mental da população.
