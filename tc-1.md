# Protótipo de geração de caricaturas com redes adversárias generativas

## Introdução

Criatividade computacional é uma área de pesquisa multidisciplinar que combina ciência da computação, psicologia, interação humano-computador e engenharia de software (Kantosalo, 2019). De acordo com Colton e outros (2009), o estudo da criatividade computacional permite entender a criatividade humana, bem como criar programas que serão usados por pessoas criativas, de modo que o programa atue como um colaborador ao invés de uma mera ferramenta.

A criatividade pode ser definida como a habilidade de criar algo que não existia antes, ou de conectar de forma inovadora conceitos já existentes (Carnovalini e Rodá, 2020). Segundo Issa e outros (2019), um sistema de criatividade computacional pode ser usado por seres humanos para aumentar suas habilidades de inovação em domínios artísticos como música, poesia e comédia, notando que o sistema deve seguir o mesmo padrão utilizado por humanos para produzir materiais.

Uma caricatura é uma representação de uma pessoa ou objeto em que as suas características mais marcantes são intencionalmente exageradas. Artistas que desenham caricaturas capturam as características faciais mais importantes da pessoa representada, tais como formato dos olhos e estilo do cabelo, e então exageram essas características para se desviar do rosto humano comum (Shi e outros, 2019). De acordo com experimentos de Rhodes e outros (1987), humanos identificam rostos familiares muito mais rapidamente em desenhos caricatos do que em desenhos realistas.

Conforme Sadimon e outros (2010), sistemas informatizados geradores de caricatura tentam converter o processo de desenhar caricaturas num algoritmo que será executado pelo computador, que por sua vez pode ser usado para assistir o usuário na criação de caricaturas, seja esse usuário um artista habilidoso ou um iniciante sem habilidade. Ainda conforme os mesmos autores, há bastante espaço para evolução dos sistemas nessa área.

De acordo com Creswell e outros (2018), redes adversárias generativas (GANs) provêem uma forma de aprender representações complexas sem depender de dados com anotações extensivas. As GANs alcançam esse feito derivando sinais de retropropagação num processo competitivo envolvendo um par de redes neurais. Ainda de acordo com os mesmos autores, as representações aprendidas pelas GANs podem ser usadas numa variedade de aplicações, tais como sintetização de imagem, edição semântica de imagem, transferência de estilo e super-resolução de imagem.

No cenário apresentado, considerando a importância da geração automática de caricaturas e o grande desafio técnico que tal projeto exibe, este trabalho tem como objetivo utilizar GANs para criar um protótipo informatizado gerador de caricaturas a partir de fotografias. Para tanto, dará continuidade ao TCC da estudante Suelem Kleinkauf do curso de Sistemas de Informações, defendido em 2021. Esta conseguiu treinar um dataset para alterar imagens de faces, porém, sem os destaques necessários nas características faciais para delinear as caricaturas. Na conclusão de seu TCC, Kleinkauf observa que houve dificuldades para controlar quais características faciais eram alteradas pela GAN. Os trabalhos aqui citados, como de Chen e outros (2020) e Zhang e outros (2021), indicam que as GANs apresentam melhores resultados quando combinadas com pré-treinamentos a fim de mapear previamente as características geométricas relevantes do rosto humano comum, para só então aplicar deformações nos dados de entrada.

## Redes neurais artificiais

Janiesch e outros (2021) fazem uma analogia sobre o que é aprendizado de máquina: Para explicar a uma criança o que é um carro de corrida, é mais fácil mostrar exemplos concretos do que formular regras explícitas sobre carros de corrida. Similarmente, o aprendizado de máquina é uma área da ciência da computação que visa ensinar conhecimentos complexos a uma máquina sem codificar estes conhecimentos explicitamente. Segundo os mesmos autores, dentre os vários algoritmos de aprendizado de máquina destacam-se as redes neurais artificiais devido a sua flexibilidade para adaptar-se a uma grande variedade de contextos diferentes.

Abiodun e outros (2018) afirmam que redes neurais artificiais são aplicações inspiradas no sistema nervoso do cérebro humano. De acordo com Khelleher (2019), redes neurais artificiais são redes (mais precisamente, dígrafos) de unidades de processamento chamadas de neurônios. Na sua concepção mais simples, os neurônios são organizados em camadas, sendo que cada neurônio é conectado a todos os neurônios da camada seguinte. A primeira camada é a camada de entrada, onde os dados entram na rede neural. A última camada é a camada de saída, de onde o resultado do processamento é exibido. As camadas intermediárias são chamadas de camadas escondidas, é nelas que o processamento propriamente dito acontece.

![Figura 1: Topologia de uma rede neural.](imagens/imagem-1.png "Fonte: Khelleher (2019)")

Os neurônios das camadas intermediárias tipicamente possuem 3 elementos:

* Uma função de ativação
* Um valor chamado bias
* Uma coleção de pesos

E implementam um processamento dividido em duas etapas:

1. Cada valor de entrada é multiplicado por um respectivo peso, e então são somados.
2. O valor bias é adicionado à soma anterior, que é então repassada à função de ativação.

O resultado da função de ativação é o valor de saída do neurônio, que é então repassado aos neurônios da próxima camada, e o processo se repete até chegar na camada de saída.

Matematicamente, um neurônio pode ser definido como:

$$
z = f(\left[\sum_{i=1}^{n} x_i \times w_i\right] + b)
$$

Onde:

* $x$ é um valor de entrada
* $w$ é o peso daquela entrada
* $b$ é o bias
* $z$ é o valor de saída

Ainda segundo Khelleher (2019), deep learning é uma sub-área da inteligência artificial focada em criar grandes modelos de redes neurais artificiais capazes de tomar decisões baseadas em dados, sendo particularmente aderente a contextos em que os dados são abundantes e complexos. De acordo com este autor, sistemas de deep learning são usado por toda a indústria tecnológica, sendo o reconhecimento facial um dos exemplos mais notáveis.

![Figura 2: Relacionamento entre inteligência artificial, aprendizado de máquina e deep learning.](imagens/imagem-2.png "Fonte: Khelleher (2019)")

Conforme Leijen e van Veen (2020), muitas arquiteturas de redes neurais artificiais foram criadas nos últimos anos, havendo um aumento em complexidade em cada uma delas, uma vez que há grande ênfase na aplicação desta tecnologia em diversos problemas do mundo real. Essas arquiteturas inovadoras expandem a concepção mais simples de redes neurais, algumas delas modificam o funcionamento interno dos neurônios, outras conectam os neurônios de maneiras diferentes e outras combinam duas ou mais redes neurais em um único sistema.

## Redes adversárias generativas

Segundo Leijen e van Veen (2020), redes adversárias generativas, ou GANs, consistem em duas redes neurais. Uma delas, chamada de geradora, gera dados sintéticos similares aos dados do dataset utilizado. A outra, chamada de discriminadora, é alimentada por dados reais e sintéticos e tenta descobrir quais dados são reais. O sucesso da rede discriminadora é usado como parâmetro para a rede geradora. Essa configuração incentiva a rede geradora a se especializar em gerar dados que parecem reais, bem como incentiva a rede discriminadora a analisar e diferenciar dados reais. Os autores notam que o processo de aprendizado nesta arquitetura é bastante complicado porque a GAN não convergirá se uma das duas redes for muito melhor que a outra.

Janiesch e outros (2021) notam que as GANs muito provavelmente vão revolucionar áreas em que conteúdos inovativos são continuamente criados, tais como composição artística e moda, e áreas em que um conteúdo deve ser transformado de uma representação para outra, tal como geração de imagens a partir de descrições textuais.

## Trabalhos correlatos

Zhang e outros (2021) usaram GANs para mapear as características faciais em fotos de rostos humanos e gerar retratos artificiais alterando a expressão facial presente na imagem original. Os autores notam que o sucesso de GANs na área de geração de imagens sintéticas os inspirou a aplicar essa técnica na pesquisa em questão. O objetivo da pesquisa foi alcançado com sucesso.

Li e outros (2021) utilizaram GANs para gerar caricaturas em três dimensões. O estudo alcançou seu objetivo, mas os autores notam que há espaço para melhorias, especialmente porque as deformidades apresentadas pela GAN não exibem muita variedade. Os autores entendem que isso se deve à falta de anotações no dataset utilizado durante a etapa de transferência de geometria. Outro problema observado foi a diminuição da resolução da imagem original.

Chen e outros (2020) utilizaram GANs para alterar a expressão facial de caricaturas em imagens de duas e três dimensões. Os resultados obtidos foram muito satisfatórios, com as imagens geradas mantendo a qualidade da imagem original e preservando a identidade da caricatura.
