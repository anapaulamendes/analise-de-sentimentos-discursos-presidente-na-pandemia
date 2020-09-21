# Análise de sentimentos dos discursos do presidente Bolsonaro durante a pandemia do covid-19.

Este trabalho utiliza Processamento de Linguagem Natural (PLN) e tem por objetivo a análise de sentimentos dos discursos do presidente Bolsonaro durante a pandemia de covid-19.

A pandemia de covid-19 teve seu início oficial em 26 de fevereiro de 2020. Em 20 de setembro de 2020 foram confirmados 4.544.629 casos, destes 136.895 mortes, aproximadamente 3.01% de mortes com relação ao total de casos. Apesar deste número parecer pequeno, de acordo com dados do [Ministério da Saúde](https://saude.gov.br/), a covid-19 no Brasil até abril de 2020, matou mais do que a H1N1, dengue e sarampo em todo o ano de 2019. (WIKIPÉDIA, 2020)

## Corpus

A criação do *corpus* foi feita com os discursos disponíveis no site do [Planalto](https://www.gov.br/planalto/pt-br), na página ["Últimos Discursos"](https://www.gov.br/planalto/pt-br/acompanhe-o-planalto/discursos?b_start:int=0). A raspagem colhe os discursos realizados entre o intervalo de datas: 26/02/2020 a 20/09/2020.

A ferramenta escolhida para a raspagem foi o Selenium, pois páginas governamentais geralmente possuem código com JavaScript para dificultar a raspagem, portanto, esta foi a escolha para evitar este problema durante a raspagem para a criação do corpus.

Foi escrito um *script* para a raspagem, este está disponível na pasta e arquivo `raspagem-dos-discursos/raspa-discursos.ipynb`.

## Análise do Corpus

Para a análise do corpus foram feitas medidas básicas como: contagem de palavras mais frequentes, plotagem de palavras mais frequentes, ocorrência de determinadas palavras com relação ao contexto da pandemia, dispersão de palavras no contexto da pandemia ao longo dos discursos, riqueza léxica dos discursos, *collocations*, frequência de pronomes.

Esta análise está disponível na pasta e arquivo `analise/analise-do-corpus.ipynb`.

## Análise de Sentimentos

Esta análise está disponível na pasta e arquivo `analise/analise-de-sentimentos.ipynb`.

## Requisitos

 - [Python 3](https://www.python.org/downloads/)
 - [Jupyter Notebook](https://jupyter.org/install)
 - [Biblioteca NLTK](https://www.nltk.org/install.html)
 - [Selenium](https://selenium-python.readthedocs.io/installation.html)
 - [Chrome Driver](https://sites.google.com/a/chromium.org/chromedriver/downloads)

## Referências

WIKIPÉDIA. Desenvolvido pela Wikimedia Foundation. Apresenta conteúdo enciclopédico. Disponível em: <[https://pt.wikipedia.org/wiki/Pandemia_de_COVID-19_no_Brasil](https://pt.wikipedia.org/wiki/Pandemia_de_COVID-19_no_Brasil")>. Acesso em: 20 Set 2020.