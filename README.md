# Análise de sentimentos dos discursos do presidente Bolsonaro durante a pandemia do covid-19.

Este trabalho utiliza Processamento de Linguagem Natural (PLN) e tem por objetivo a análise de sentimentos dos discursos do presidente Bolsonaro durante a pandemia de covid-19.

A pandemia de covid-19 teve seu início oficial em 26 de fevereiro de 2020. Em 20 de setembro de 2020 foram confirmados 4.544.629 casos, destes 136.895 mortes, aproximadamente 3.01% de mortes com relação ao total de casos. Apesar deste número parecer pequeno, de acordo com dados do [Ministério da Saúde](https://saude.gov.br/), a covid-19 no Brasil até abril de 2020, matou mais do que a H1N1, dengue e sarampo em todo o ano de 2019. (WIKIPÉDIA, 2020)

## Criação do Corpus de Discursos

A criação do *corpus* foi feita com os discursos disponíveis no site do [Planalto](https://www.gov.br/planalto/pt-br), na página ["Últimos Discursos"](https://www.gov.br/planalto/pt-br/acompanhe-o-planalto/discursos?b_start:int=0). A raspagem colhe os discursos realizados entre o intervalo de datas: 26/02/2020 a 23/09/2020.

A ferramenta escolhida para a raspagem foi o Selenium, pois páginas governamentais geralmente possuem código com JavaScript para dificultar a raspagem, portanto, esta foi a escolha para evitar este problema durante a raspagem para a criação do corpus.

Foi escrito um *script* para a raspagem, este está disponível na pasta e arquivo `raspagem-dos-discursos/raspa-discursos.ipynb`.

## Análise do Corpus de Discursos

Para a análise do corpus foram feitas medidas básicas como: contagem de palavras mais frequentes, plotagem de palavras mais frequentes, ocorrência de determinadas palavras com relação ao contexto da pandemia, dispersão de palavras no contexto da pandemia ao longo dos discursos, riqueza léxica dos discursos, *collocations*, frequência de pronomes.

Esta análise está disponível na pasta e arquivo `analise/analise-do-corpus.ipynb`.

## Análise de Sentimentos

As análises estão disponíveis na pasta `analise`. Foram realizadas 4 análises com 4 corpus diferentes:

 - [Corpus ReLi](https://www.linguateca.pt/Repositorio/ReLi/)
 - [WordNetAffectBR](https://www.inf.pucrs.br/linatural/wordpress/recursos-e-ferramentas/wordnetaffectbr/)
 - [OpLexicon](https://www.inf.pucrs.br/linatural/wordpress/recursos-e-ferramentas/oplexicon/)
 - [SentiLex-PT](https://b2share.eudat.eu/records/93ab120efdaa4662baec6adee8e7585f)

As análises com os corpus ReLi e WordNetAffectBR tiveram bons resultados, porém nas análises com os corpus OpLexicon e SentiLex-PT não foi possível completar devido ao pouco poder de processamento. Estes 2 últimos são enormes, muito bons para esta análise, porém exigem mais processamento.

## Requisitos

 - [Python 3](https://www.python.org/downloads/)
 - [Jupyter Notebook](https://jupyter.org/install)
 - [NLTK](https://www.nltk.org/install.html)
 - [Selenium](https://selenium-python.readthedocs.io/installation.html)
 - [Chrome Driver](https://sites.google.com/a/chromium.org/chromedriver/downloads)
 - [TextBlob](https://textblob.readthedocs.io/en/dev/index.html)
 - [Pandas](https://pandas.pydata.org/)
 - [Numpy](https://numpy.org/)
 - [Matplotlib](https://matplotlib.org/)
 - [Scikit-learn](https://scikit-learn.org/stable/)
 - [Wordcloud](https://pypi.org/project/wordcloud/)

## Referências
-   Freitas, C.; Motta, E.; Milidiú, R.; Cesar, J. Vampiro que brilha... rá! Desafios na anotação de opinião em um corpus de resenhas de livros. In: XI Encontro de Linguística de Corpus (ELC 2012), São Paulo, Brasil, 2012.
- Mário J. Silva, Paula Carvalho and Luís Sarmento. "Building a Sentiment Lexicon for Social Judgement Mining". In Lecture Notes in Computer Science (LNCS) / Lecture Notes in Artificial Intelligence (LNAI), International Conference on Computational Processing of Portuguese (PROPOR), 17-20 April, 2012, Coimbra.
- PASQUALOTTI, Paulo Roberto. WordNet Affect BR – uma base de expressões de emoção em Português. Novas Edições Acadêmicas. 2015
- S. Loria, textblob Documentation, (2018) 1–73.
- Souza, M.; Vieira, R. Sentiment Analysis on Twitter Data for Portuguese Language. 10th International Conference Computational Processing of the Portuguese Language, 2012.
- WIKIPÉDIA. Desenvolvido pela Wikimedia Foundation. Apresenta conteúdo enciclopédico. Disponível em: <[https://pt.wikipedia.org/wiki/Pandemia_de_COVID-19_no_Brasil](https://pt.wikipedia.org/wiki/Pandemia_de_COVID-19_no_Brasil")>. Acesso em: 20 Set 2020.