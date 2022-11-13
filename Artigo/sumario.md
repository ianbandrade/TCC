# Identificação da estrutura de Github Wikis a partir de aprendizagem de máquina

1. Gabriel Moreira Chaves
2. Ian Bittencourt Andrade Jacinto

- Jose Laerte Pires Xavier Junior
- Marco Rodrigo Costa
- Hugo Bastos de Paula

## Introdução

1. A área da Engenharia de Software tratada neste trabalho é a Gestão do Conhecimento em Engenharia de Software;
2. O problema que este trabalho busca resolver nessa área é a ausência de trabalhos que avaliam a utilização de aprendizagem de máquina para determinar o conteúdo das páginas dos GitHub Wikis;
3. Resolver este problema é relevante porque com a classificação, será possível identificar a estrutura dos GitHub Wikis com intenção de facilitar aos usuários e proprietários de repositórios a descoberta de informações relevantes, buscando promover uma visão geral sobre as estruturas que estão sendo abordadas nas construções dos GitHub Wikis, de modo a captar a presença de consistências e padrões aplicados a essas estruturas;
4. O objetivo geral deste estudo é avaliar a utilização de aprendizagem de máquina para determinar a estrutura de conteúdo dos GitHub Wikis;
5. Os *três* objetivos específicos deste trabalho são: 1) classificar uma base de dados de nomes de páginas de GitHub Wikis por tipo de conteúdo; 2) treinar modelos de aprendizagem de máquina para classificação dessas páginas em função de seus conteúdos; 3) realizar a avaliação dos modelos de aprendizagem de máquina.

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

1. O tipo de pesquisa adotado neste trabalho é um estudo de caso, caracterizando-se como uma pesquisa descritiva. O estudo de caso é realizado com a intenção de coletar dados qualitativos a partir do conteúdo dos GitHub Wikis;
2. Os materiais utilizados neste trabalho são os dados coletados a partir da GitHub API REST e dos repositórios de GitHub Wiki. Os dados são analisados e manipulados com a utilização da linguagem de programação Python assim como o treinamento e avaliação dos modelos de aprendizado de máquina;
3. Os métodos empregados neste trabalho são: 1) Coletar os repositórios pela API REST do GitHub; 2) Filtrar pelos repositórios que possuem o campo `has_wiki` positivo; 3) Tentar clonar os repositórios com o campo `has_wiki` positivo; 4) Extrair os nomes de páginas dos repositórios clonados; 5) Filtrar pelos repositórios com quantidade de estrelas maior ou igual a 4.500; 6) Filtrar os repositórios com até 7 páginas; 7) Filtrar por páginas que possuam nome com caracteres em inglês; 8) Filtrar por páginas que possuam pelo menos 1Mb de tamanho; 9) Filtrar por páginas que possuam seu conteúdo em inglês; 10) Aplicar as abstrações; 11) Gerar a base de dados para classificação. A partir da coleta, os dados são classificados de forma manual pelos autores. Para o treinamento, são definidas 6 fases: 1) Utilizar as colunas _abstracted_ (colunas com os nomes das páginas abstraídas) e _classification_ (classificações realizadas pelos autores); 2) Remover classificações referentes à categoria `Other`; 3) Aplicar a técnica de extração de features tf-idf com ngramas de 1 a 3 palavras; 4) Separar as classificações em base de treinamento e teste; 5) Treinar os modelos de aprendizado de máquina; 6) Analisar os resultados obtidos do aprendizado (_recall_, _precision_ e F1 _score_).    
