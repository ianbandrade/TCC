# Análise sistemática do conteúdo dos GitHub Wikis dos repositórios open source mais populares

1. Gabriel Moreira Chaves
2. Ian Bittencourt Andrade

- Jose Laerte Pires Xavier Junior
- Marco Rodrigo Costa

## Introdução

1. A área da Engenharia de Software tratada neste trabalho é a Gerência de Conhecimento em Engenharia de Software;
2. O problema que este trabalho busca resolver nessa área é a a ausência de uma compreensão sistemática do conteúdo de um GitHub Wiki em projetos *open source*;
3. Resolver este problema é relevante porque com a compreensão sistemática, será possível identificar a finalidade e a relevância dos GitHub Wikis com intenção de facilitar aos usuários e proprietários de repositórios a descoberta de informações relevantes, buscando promover uma análise crítica sobre as estruturas que estão sendo abordadas nas construções dos GitHub Wikis, de modo a captar a presença de consistências e padrões aplicados às estruturas;
4. O objetivo geral deste trabalho é realizar uma análise sistemática do conteúdo presente nos GitHub Wikis dos repositórios *open source* mais populares da plataforma;
5. Os *três* objetivos específicos deste trabalho são: 1) propor algoritmos de classificação de conteúdo de GitHub Wikis; 2) identificar quais são as categorias mais recorrentes nos conteúdos dos GitHub Wikis; 3) identificar quais modelos de aprendizado de máquina utilizados melhor realiza as classificações dos conteúdos dos GitHub Wikis.

## Fundamentação Teórica

1. O conceito principal deste trabalho se relaciona ao GitHub Wiki. A sua definição neste trabalho segue conforme definido no trabalho "Collaborating in GitHub" pela autora Nicky Bleiel;
2. O conceito secundário deste trabalho se relaciona aos Wikis. A sua definição neste trabalho segue conforme definido no livro "The wiki way: Quick collaboration on the Web" pelos autores Bo Leuf e Ward Cunningham;
3. O conceito terciário deste trabalho se relaciona à Gestão de Conhecimento. A sua definição neste trabalho segue conforme definido no trabalho "Knowledge management in software engineering" pelos autores Loana Rus e Mikael Lindvall.

## Trabalhos Relacionados

1. O trabalho mais relacionado é o "Categorizing the content of github readme files", publicado no ano de 2019. Nosso trabalho se baseia na metodologia de classificação para a definição do conteúdo sistemático, adotando as 8 categorias propostas nas classificações e realização da validação a partir do F1 score, entretanto utilizando a aplicação desses conceitos em GitHub Wikis;
2. O segundo trabalho mais relacionado é o "An empirical study of release note production and usage in practice", publicado no ano de 2020. O processo de definição das categorias das informações documentadas nas notas de versão são baseadas na classificação de quais são as finalidades dos GitHub Wikis;
3. O terceiro trabalho mais relacionado é o "A topological analysis of communication channels for knowledge sharing in contemporary GitHub projects", publicado no ano de 2019. O processo de classificação utilizado traz uma base para o nosso trabalho, sendo possível entender como as categorias de conhecimento organizacional impactam nas finalidades dos GitHub Wikis;
4. O quarto trabalho mais relacionado é o "OntoCat: Automatically categorizing knowledge in API Documentation", publicado no ano de 2016. Este trabalho baseia em abordagens de aprendizado de máquina supervisionado que são o mesmo tipo de abordagem adotado no nosso trabalho;
5. O quinto trabalho mais relacionado é o "Augmenting API Documentation with Insights from Stack Overflow", publicado no ano de 2016. O trabalho realizou uma construção de um processo de classificação a partir de aprendizado de máquina, nosso trabalho também utiliza um processo de classificação a partir de aprendizado de máquina.

## Materiais e Métodos

1. O tipo de pesquisa adotado neste trabalho é pesquisa descritiva. A pesquisa descreve características e finalidades dos conteúdos dos GitHub Wikis.
2. Os materiais utilizados neste trabalho utiliza dados extraídos da GitHub API GraphQL v4, analisando e manipulando esses dados com a linguagem de programação Python.
3. Os métodos empregados neste trabalho são a extração de dados de API, classificação utilizando a técnica de Close Card Sorting e aprendizado de máquina supervisionado para o aprendizado de máquina utilizando algoritmos de classificação.
4. As métricas de avaliação são as pontuações de F1 Score.
5. As etapa de execução do trabalho são: extrair os dados da GitHub API GraphQL v4; classificar o conteúdo dos GitHub Wikis; treinar algoritmos de classificação; avaliar e comparar o desempenho dos algoritmos a partir dos valores de F1 score.
