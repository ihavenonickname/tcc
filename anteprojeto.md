# Protótipo de geração de caricaturas com redes adversárias generativas

## Resumo

A criatividade pode ser definida como a habilidade de criar algo que antes não existia, ou de conectar conceitos que antes não estavam conectados. Um sistema informatizado de criatividade computacional auxilia seres humanos em tarefas que exigem habilidades inovativas, servindo não apenas como uma ferramenta, mas sim como um colaborador na criação de trabalhos criativos. Dentro da área de criatividade computacional, o uso de redes adversárias generativas alcançou sucesso na sintetização de rostos humanos ultrarrealistas. No contexto de geração de rostos sintéticos, uma sub-área da criatividade computacional é a geração automática de caricaturas. A caricatura de um rosto humano é a representação desse rosto em que suas características são alteradas de modo a se diferenciar o máximo possível do rosto humano comum. Com base nesse contexto, este trabalho tem como objetivo desenvolver e validar um protótipo gerador de caricaturas baseado em redes adversárias generativas.

Palavras-chave: Criatividade computacional, caricaturas, redes adversárias generativas

## Motivação

Criatividade computacional é uma área de pesquisa multidisciplinar que combina ciência da computação, psicologia, interação humano-computador e engenharia de software (Kantosalo, 2019). De acordo com Colton e outros (2009), o estudo da criatividade computacional permite entender a criatividade humana, bem como criar programas que serão usados por pessoas criativas, de modo que o programa atue como um colaborador ao invés de uma mera ferramenta.

A criatividade pode ser definida como a habilidade de criar algo que não existia antes, ou de conectar de forma inovadora conceitos já existentes (Carnovalini e Rodá, 2020). Segundo Issa e outros (2019), um sistema de criatividade computacional pode ser usado por seres humanos para aumentar suas habilidades de inovação em domínios artísticos como música, poesia e comédia, notando que o sistema deve seguir o mesmo padrão utilizado por humanos para produzir materiais.

Uma caricatura é uma representação de uma pessoa ou objeto em que as suas características mais marcantes são intencionalmente exageradas. Artistas que desenham caricaturas capturam as características faciais mais importantes da pessoa representada, tais como formato dos olhos e estilo do cabelo, e então exageram essas características para se desviar do rosto humano comum (Shi e outros, 2019). De acordo com experimentos de Rhodes e outros (1987), humanos identificam rostos familiares muito mais rapidamente em desenhos caricatos do que em desenhos realistas.

Conforme Sadimon e outros (2010), sistemas informatizados geradores de caricatura tentam converter o processo de desenhar caricaturas num algoritmo que será executado pelo computador, que por sua vez pode ser usado para assistir o usuário na criação de caricaturas, seja esse usuário um artista habilidoso ou um iniciante sem habilidade. Ainda conforme os mesmos autores, há bastante espaço para evolução dos sistemas nessa área.

De acordo com Creswell e outros (2018), redes adversárias generativas (GANs) provêem uma forma de aprender representações complexas sem depender de dados com anotações extensivas. As GANs alcançam esse feito derivando sinais de retropropagação num processo competitivo envolvendo um par de redes neurais. Ainda de acordo com os mesmos autores, as representações aprendidas pelas GANs podem ser usadas numa variedade de aplicações, tais como sintetização de imagem, edição semântica de imagem, transferência de estilo e super-resolução de imagem.

Zhang e outros (2021) usaram GANs para mapear as características faciais em fotos de rostos humanos e gerar retratos artificiais alterando a expressão facial presente na imagem original. Os autores notam que o sucesso de GANs na área de geração de imagens sintéticas os inspirou a aplicar essa técnica na pesquisa em questão. O objetivo da pesquisa foi alcançado com sucesso.

Li e outros (2021) utilizaram GANs para gerar caricaturas em três dimensões. O estudo alcançou seu objetivo, mas os autores notam que há espaço para melhorias, especialmente porque as deformidades apresentadas pela GAN não exibem muita variedade. Os autores entendem que isso se deve à falta de anotações no dataset utilizado durante a etapa de transferência de geometria. Outro problema observado foi a diminuição da resolução da imagem original.

Chen e outros (2020) utilizaram GANs para alterar a expressão facial de caricaturas em imagens de duas e três dimensões. Os resultados obtidos foram muito satisfatórios, com as imagens geradas mantendo a qualidade da imagem original e preservando a identidade da caricatura.

No cenário apresentado, considerando a importância da geração automática de caricaturas e o grande desafio técnico que tal projeto exibe, este trabalho tem como objetivo utilizar GANs para criar um protótipo informatizado gerador de caricaturas a partir de fotografias. Para tanto, dará continuidade ao TCC da estudante Suelem Kleinkauf do curso de Sistemas de Informações, defendido em 2021. Esta conseguiu treinar um dataset para alterar imagens de faces, porém, sem os destaques necessários nas características faciais para delinear as caricaturas.

## Objetivos

### Objetivo geral

Desenvolver um protótipo gerador de caricaturas a partir de fotos com o uso de redes GAN.

### Objetivos específicos

* Estudar redes GAN no contexto de classificação e sintetização de imagens
* Realizar experimentos com algoritmos que usam GANs e suas variações
* Desenvolver o protótipo
* Validar o protótipo

## Metodologia

A metodologia Design Science Research (DSR) foi escolhida para conduzir este trabalho. Segundo Çagdasß e Stubkjær (2010), DSR é um processo rigoroso para projetar artefatos a fim de resolver problemas observados, avaliar esses artefatos e comunicar os resultados. De acordo com Lacerda e outros (2013), o DSR é formado por um conjunto de técnicas analíticas que permitem o desenvolvimento de pesquisas em diversas áreas, cujo objetivo é estudar, pesquisar e investigar o artificial e seu comportamento.

Essa metodologia será aplicada neste trabalho dividida em 5 etapas principais conforme descritas por Junior e outros (2017), apresentadas a seguir junto de sua descrição:

1. **Identificação do problema e contexto:** Pesquisa sobre técnicas e métodos de inteligência artificial utilizados no contexto da geração e modificação de imagens e caricaturas
1. **Definição dos artefatos para a solução:** Escolha da linguagem de programação, das bibliotecas e do dataset que serão utilizados no desenvolvimento do protótipo
1. **Projeto e desenvolvimento:** Desenvolvimento do protótipo de geração de caricaturas baseado em imagem
1. **Avaliação:** Geração de caricaturas pelo protótipo desenvolvido e avaliação dessas caricaturas por profissionais da área do desenho
1. **Comunicação:** Apresentação do trabalho de conclusão

## Cronograma

### Trabalho de conclusão I

| Etapa                                                   | Abril | Maio | Junho |
|:-------------------------------------------------------:|:-----:|:----:|:-----:|
| Revisar literatura sobre inteligência artificial e GANs | x     | x    |       |
| Definir técnicas e dataset para desenvolvimento         |       | x    | x     |
| Preparar ambiente de desenvolvimento                    |       |      | x     |
| Escrita do TC 1                                         | x     | x    | x     |
| Entrega do TC 1                                         |       |      | x     |

### Trabalho de conclusão II

| Etapa                   | Agosto | Setembro | Outubro | Novembro |
|:-----------------------:|:------:|:--------:|:-------:|:--------:|
| Desenvolver o protótipo | x      | x        | x       |          |
| Validar o protótipo     |        |          | x       |          |
| Escrita do TC 2         | x      | x        | x       | x        |
| Entrega do TC 2         |        |          |         | x        |
| Banca do TC 2           |        |          |         | x        |
| Publicação do artigo    |        |          | x       |          |

## Bibliografia

Em ordem de citação no texto:

* KANTOSALO, Anna. Human-Computer Co-Creativity: Designing, Evaluating and Modelling Computational Collaborators for Poetry Writing. Dissertação de doutorado - Faculdade de ciências da Universidade de Helsinki, 2019.
* COLTON, Simon et al. Computational Creativity: Coming of Age. Association for the Advancement of Artificial Intelligence, 2009.
* CARNOVALINI, Filippo; RODÁ, Antonio. Computational Creativity and Music Generation Systems: An Introduction to the State of the Art. Revista Frontiers in Artificial Intelligence, 2020.
* ISSA, Lana et al. Computational Creativity: The Design of a Creative Computer Program. nternational Conference on Information and Communication Systems, 2019.
* SHI, Yichun et al. WarpGAN: Automatic Caricature Generation. Computer Vision Foundation, 2019.
* RHODES, Gillian et al. Identification and Ratings of Caricatures: Implications for Mental Representations of Faces. Revista Cognitive Psychology, 1987.
* SADIMON, Suriati Bte et al. Computer Generated Caricature: A Survey. International Conference on Cyberworlds, 2010.
* CRESWELL, Antonia et al. Generative Adversarial Networks. IEEE Signal Processing Magazine, 2018.
* ZHANG, Kaihao et al. Disentangled Feature Networks for Facial Portrait and Caricature Generation. IEEE Transactions on Multimedia, 2021.
* LI, Song et al. Deep 3D caricature face generation with identity and structure consistency. Revista Neurocomputing, 2021.
* CHEN, Keyu et al. Modeling Caricature Expressions by 3D Blendshape and Dynamic Texture. ACM International Conference on Multimedia, 2020.
* KLEINKAUF, Suelem. Protótipo de Geração de Caricaturas Baseada em Fotos. Trabalho de Conclusão de Curso (Monografia) - Curso de Sistemas de Informação, Universidade FEEVALE, 2021.
* ÇAGDASSS, Volkan; STUBKJÆR, Erik. Design research for cadastral systems. Computers, Environment and Urban Systems, 2010.
* LACERDA, Daniel Pacheco et al. Design Science Research: método de pesquisa para a engenharia de produção. Revista Gestão & Produção, 2013.
* JÚNIOR, Vanderlei Freitas et al. Design Science Research Methodology As Methodological Strategy for Technological Research. Revista Espacios, 2017.

Em ordem alfabética pelo nome do autor:

* ÇAGDASSS, Volkan; STUBKJÆR, Erik. Design research for cadastral systems. Computers, Environment and Urban Systems, 2010.
* CARNOVALINI, Filippo; RODÁ, Antonio. Computational Creativity and Music Generation Systems: An Introduction to the State of the Art. Revista Frontiers in Artificial Intelligence, 2020.
* CHEN, Keyu et al. Modeling Caricature Expressions by 3D Blendshape and Dynamic Texture. ACM International Conference on Multimedia, 2020.
* COLTON, Simon et al. Computational Creativity: Coming of Age. Association for the Advancement of Artificial Intelligence, 2009.
* CRESWELL, Antonia et al. Generative Adversarial Networks. IEEE Signal Processing Magazine, 2018.
* ISSA, Lana et al. Computational Creativity: The Design of a Creative Computer Program. International Conference on Information and Communication Systems, 2019.
* JÚNIOR, Vanderlei Freitas et al. Design Science Research Methodology As Methodological Strategy for Technological Research. Revista Espacios, 2017.
* KANTOSALO, Anna. Human-Computer Co-Creativity: Designing, Evaluating and Modelling Computational Collaborators for Poetry Writing. Dissertação de doutorado - Faculdade de ciências da Universidade de Helsinki, 2019.
* KLEINKAUF, Suelem. Protótipo de Geração de Caricaturas Baseada em Fotos. Trabalho de Conclusão de Curso (Monografia) - Curso de Sistemas de Informação, Universidade FEEVALE, 2021.
* LACERDA, Daniel Pacheco et al. Design Science Research: método de pesquisa para a engenharia de produção. Revista Gestão & Produção, 2013.
* LI, Song et al. Deep 3D caricature face generation with identity and structure consistency. Revista Neurocomputing, 2021.
* RHODES, Gillian et al. Identification and Ratings of Caricatures: Implications for Mental Representations of Faces. Revista Cognitive Psychology, 1987.
* SADIMON, Suriati Bte et al. Computer Generated Caricature: A Survey. International Conference on Cyberworlds, 2010.
* SHI, Yichun et al. WarpGAN: Automatic Caricature Generation. Computer Vision Foundation, 2019.
* ZHANG, Kaihao et al. Disentangled Feature Networks for Facial Portrait and Caricature Generation. IEEE Transactions on Multimedia, 2021.
