# Assessing Mock Classes: An Empirical Study

G. Pereira and A. Hora, "Assessing Mock Classes: An Empirical Study," 2020 IEEE International Conference on Software Maintenance and Evolution (ICSME), 2020, pp. 453-463. DOI: [10.1109/ICSME46990.2020.00050](https://doi.org/10.1109/ICSME46990.2020.00050)

## 1. Fichamento de Conteúdo

No âmbito da Engenharia de Software, há uma etapa de realização de atividades de testes. Vários _softwares_ desenvolvidos para funcionarem em sua plenitude possuem diversas comunicações com outros sistemas (_web services_, banco de dados, etc).
Havendo a necessidade de se comunicarem para a realização dos testes, uma técnica para emular essas dependências são utilizadas (_mock_). O artigo se propõe a realizar um experimento empírico a partir de perspectivas quantitativas e qualitativas, para analisar classes _mock_. Como metodologia, realizaram análises de 12 projetos de _software open source_. Três questões de pesquisa foram realizadas: (1) Qual o conteúdo das classes _mock_; (2) Como as classes _mock_ são projetadas; (3) Como as classes _mock_ são usadas pelos desenvolvedores. Os autores como resultados relatam: (1) classes _mock_ são frequentemente criadas para emular objetos de domínio, dependências externas e serviços da Web; (2) classes _mock_ geralmente fazem parte de uma hierarquia, são principalmente públicas e não diferem das classes regulares em relação ao número de métodos; (3) classes simuladas são amplamente consumidas por projetos de clientes para dar suporte a testes, principalmente para emular serviços da web.

## 2. Fichamento Bibliográfico

- _"Domain object"_ são regras de negócio de um sistema (página 1).
- _"Mock objects"_ são objetos que simulam o comportamento de objetos reais de forma controlada (página 1).
- _"Mocking frameworks"_ são ferramentas que auxiliam estruturas de teste de unidade isolando as dependências, mas não substituem as estruturas de teste de unidade (página 1).


## 3. Fichamento de Citações

- _"In practice, there are two solutions to adopt mock objects.The emulated dependency can be dynamically created withthe support of mocking frameworks or manually handcoded in mock classes."_
- _"As briefly described in the introduction, mock objectscan be either (1) dynamically created with the supportof mocking frameworks or (2) manually hand-coded inmock classe."_
- _"Mock classes are often created to emulate domain objects, external dependencies, and web services."_
- _"Mock classes are often part of a hierarchy, are mostly public, and are not different from regular classes regarding number of methods."_
- _"Mock classes are largely consumed by client projects to support testing, particularly to emulate web services."_
