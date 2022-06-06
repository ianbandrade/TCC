# Classificação do Conteúdo Textual do GitHub Wiki de Repositórios _Open Source_

1. Gabriel Moreira Chaves
2. Ian Bittencourt Andrade

- Jose Laerte Pires Xavier Junior
- Marco Rodrigo Costa

## Introdução

1. A área da Engenharia de Software tratada neste trabalho é a Gestão do Conhecimento em Engenharia de Software;
2. O problema que este trabalho busca resolver nessa área é aa ausência de trabalhos que classificam o conteúdo textual de um GitHub Wiki em repositórios _open source_;
3. Resolver este problema é relevante porque com a classificação, será possível identificar a finalidade e a relevância dos GitHub Wikis com intenção de facilitar aos usuários e proprietários de repositórios a descoberta de informações relevantes, buscando promover uma visão geral sobre as estruturas que estão sendo abordadas nas construções dos GitHub Wikis, de modo a captar a presença de consistências e padrões aplicados às estruturas;
4. O objetivo geral deste estudo é avaliar e classificar o conteúdo textual presente no GitHub Wiki em repositórios _open source_;
5. Os *três* objetivos específicos deste trabalho são: 1) propor modelos de classificação de conteúdo de GitHub Wikis; 2) identificar quais são as categorias mais recorrentes no conteúdo dos GitHub Wikis; 3) identificar quais modelos de aprendizado de máquina utilizados melhor realiza as classificações do conteúdo dos GitHub Wikis.

## Fundamentação Teórica

1. O conceito principal deste trabalho se relaciona ao GitHub Wiki. A sua definição neste trabalho segue conforme definido no trabalho "Collaborating in GitHub" pela autora Nicky Bleiel;
2. O conceito secundário deste trabalho se relaciona aos Wikis. A sua definição neste trabalho segue conforme definido no livro "The wiki way: Quick collaboration on the Web" pelos autores Bo Leuf e Ward Cunningham;
3. O conceito terciário deste trabalho se relaciona à Gestão de Conhecimento. A sua definição neste trabalho segue conforme definido no trabalho "Knowledge management in software engineering" pelos autores Loana Rus e Mikael Lindvall.

## Trabalhos Relacionados

1. O trabalho mais relacionado é o "Categorizing the Content of GitHub Readme Files", publicado no ano de 2019. O trabalho trata sobre a classificação de READMEs para a definição de seus conteúdos, será adotado as oito categorias propostas para as classificações e será realizada a validação dessas, a partir do F1 _score_;
2. O segundo trabalho mais relacionado é o "An Empirical Study of Release Note Production and Usage in Practice", publicado no ano de 2020. O processo de aprendizado de máquina usado para prever os problemas que devem ser listados nas notas de versão são considerados quando executado o treinamento dos modelos de aprendizado de máquina usados para a categorização do conteúdo textual de GitHub Wikis;
3. O terceiro trabalho mais relacionado é o "A Topological Analysis of Communication Channels for Knowledge Sharing in Contemporary GitHub Projects", publicado no ano de 2019. O processo de classificação utilizado no trabalho relacionado traz uma base para a presente pesquisa, de modo a colaborar na identificação de quais modelos de aprendizado de máquina utilizados melhor realiza as classificações do conteúdo dos GitHub Wikis;
4. O quarto trabalho mais relacionado é o "OntoCat: Automatically Categorizing Knowledge in API Documentation", publicado no ano de 2016. O presente trabalho classifica o conteúdo dos GitHub Wikis baseando-se nas abordagens de aprendizado de máquina supervisionado assim como é apresentado nesse trabalho relacionado;
5. O quinto trabalho mais relacionado é o "Augmenting API Documentation with Insights From Stack Overflow", publicado no ano de 2016. O presente trabalho irá basear-se nos mecanismos utilizados na construção do sistema SISE apresentado nesse trabalho relacionado para construir um processo que realizará a classificação do conteúdo textual dos GitHub Wikis selecionados.

## Materiais e Métodos

1. O tipo de pesquisa adotado neste trabalho é a pesquisa descritiva. A pesquisa descreve as categorias do conteúdo textual presente nos GitHub Wikis dos repositórios _open source_ a partir de dados qualitativos;
2. Os materiais utilizados neste trabalho são os dados coletados a partir da GitHub API GraphQL v4 e dos repositórios de GitHub Wiki. Os dados são analisados e manipulados com a utilização da linguagem de programação Python assim como o treinamento e avaliação dos modelos de aprendizado de máquina.
3. Os métodos empregados neste trabalho são: 1) extração de dados de API; 2) aprendizado de máquina supervisionado utilizando os algoritmos de classificação: _Support Vector Machines_, _Logistic Regression_, _Random Forest_, _k-Nearest Neighbors_ e _Multinomial Naive Bayes_; 3) _survey_ para a coleta de dados de entrada para os modelos de aprendizado de máquina.
4. As métricas de avaliação são as pontuações da métrica de desempenho F1 Score obtidas pelos modelos de aprendizado de máquina, uma média harmônica calculada com base na precisão e na revocação dos modelos.
5. As etapa de execução do trabalho são: 1) Extração dos dados da API do GitHub; 2) Extração dos dados dos repositórios; 3) Algoritmo do envio do _survey_; 4) Algoritmo da coleta da _survey_; 5) Classificação do conteúdo dos GitHub Wikis; 6) Análise e manipulação dos resultados das classificações; 7) Treinamento dos modelos de aprendizado de máquina; 8) Discussão e avaliação dos resultados.
