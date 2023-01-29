# Naiome-Alves-Pereira
Trabalho Individual 1

https://pubmed.ncbi.nlm.nih.gov/33290246/
https://pubmed.ncbi.nlm.nih.gov/36127910/

  Um tema que vem sendo muito discutido no Brasil e no mundo, é a saúde mental. Após a pandemia do Covid 19 esse problema se tornou cada vez mais recorrentes e muitos estudos andam abordando as consequências ocasionado por problemas mentais na vida do indivíduo como sua vida profissional, social, amorosa e etc. Os estudos utilizados para me auxiliar a compreender melhor o problema foram: Mental Health and Burnout Syndrome Among Postgraduate Students in Medical and Multidisciplinary Residencies During the COVID-19 Pandemic in Brazil: Protocol for a Prospective Cohort Study, publicado em janeiro de 2021; e o artigo Occupational stress and common mental disorders: how do coping strategies work?, publicado em junho de 2022, ambos foram publicados pelo site PubMed.gov e estão disponiveis pela National Library of Medicine.

  O contexto escolhido para a analise de dados foi um estado que fica no sul do Brasil. O Paraná é um estado que possui 399 municipíos e é a 4º maior econômia do país. Com os dados disponibilizados pelo governo federal iremos analisar se a diferença entre esses municipios e se é possivel medir a saúde mental de uma determinada população e se ações de promoção a saúde que é um conjunto de politicas, programas e plano de saúde pública que visa melhorar o bem estar e a qualidade de vida da população, podendo ser realizadas por individuos, coletivamente ou por organizações.

  O objetivo desse trabalho busca descobrir se quanto mais ações de promoção a saúde maior será a saúde mental da população?

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


Pré-processamento (limpeza, missings, outliers, feature engineering, formatação (números e texto), etc.

O processo do desenvolvimento desse trabalho se deu da seguinte forma:
  Foi utilizado dados no Tabnet - SUS (Quantidade de Assistentes Sociais, Psicólogos, Psiquiatra, Ações de Promoções e Prevenções a Saúde e Ações Complementares de atenção a saúde, além da quantidade de atendimentos realizados nos anos de 2017, 2018, 2019, 2020 e 2021)  e do IBGE (Área Territorial, Estimativa da População, Índice de Desenvolvimento Humano e Produto Interno Bruto).
  Foi realizado a limpeza dos arquivos csv, eliminando cabeçalhos e rodapés e combinando mais de um banco de dados, houve tratamento de caracteres não numerais, a codificação para latin-1.
  Na parte de pré-processamento foi criado 4 Data Frames e cada um referente a uma tabela, sendo: 
DF1 - Tabela referente a ocupações de niveis superior. Foi utilizada apenas as colunas referentes as profissões de assistente social, psicólogo e psiquiatra
DF2 - Tabela referente a copiladoss de dados da saúde de 2021. Foi utilizado os dados apresentados em ações de promoção e prevenção em saúde e
       ações complementares de atenção a saude
DF3 -
DF4 -
Como a minha tabela possuía todos os municipios selecionei apenas os do estado do Paraná (Os municípios do Paraná começam com o número 41, pois é 4º região e o 1º estado); como também escolhi na tabela de profissionais disponibilizadas pelo governo os profissionais de assistência social, psicólogos e psiquiatras pois são os profissionais que lidam com saúde mental.

Análise Exploratória 

Proposta de estratégia analítica (como planeja resolver o problema de pesquisa com os dados coletados)
