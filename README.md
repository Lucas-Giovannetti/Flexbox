# POC 01

## O que é Flexbox

O Flexbox é um módulo de layout que oferece uma maneira mais eficiente de organizar, alinhar e distribuir espaço entre os itens dentro de um contêiner. Ele foi projetado para ser flexível, permitindo que os itens se ajustem automaticamente, seja expandindo para preencher o espaço disponível ou encolhendo para evitar transbordamentos, mesmo quando o tamanho dos itens é desconhecido ou dinâmico.
A principal vantagem do Flexbox é a sua capacidade de adaptar os itens do contêiner para ocupar o espaço disponível de forma otimizada, considerando diferentes dispositivos e tamanhos de tela. Diferente dos layouts tradicionais, como o layout em bloco (vertical) e o layout em linha (horizontal), o Flexbox é agnóstico à direção, o que significa que ele pode organizar os itens em qualquer direção, tornando-o ideal para componentes de uma aplicação e layouts de pequena escala, onde é necessário lidar com mudanças de orientação, redimensionamento e outras dinâmicas.

## Noções básicas e termologia

O Flexbox é um módulo abrangente que consiste em várias propriedades, não se limitando a apenas uma. Algumas dessas propriedades são aplicadas diretamente ao contêiner (o elemento pai, conhecido como flex container), enquanto outras são definidas nos elementos filhos, chamados de flex items.
Enquanto o layout tradicional utiliza as direções block e inline, o layout Flex é orientado pelas direções "flex flow". O diagrama da especificação a seguir ilustra a ideia central do layout Flex, mostrando como ele organiza e distribui os elementos dentro do contêiner de maneira flexível e adaptável.

## Os ítens serão dispostos no leiaute seguindo ou o eixo principal ou o transversal.
![image](https://github.com/user-attachments/assets/efd04d56-0efa-49c9-9877-a754f03545b4)
*	Eixo principal: o eixo principal de um flex container é o eixo primário e ao longo dele são inseridos os flex items. Cuidado: O eixo principal não é necessariamente horizontal; vai depender da propriedade flex-direction (veja abaixo).
*	main-start | main-end: os flex items são inseridos dentro do container começando pelo lado start, indo em direção ao lado end.
*	Tamanho principal: A largura ou altura de um flex item, dependendo da direção do container, é o tamanho principal do ítem. A propriedade de tamanho principal de um flex item pode ser tanto width quanto height, dependendo de qual delas estiver na direção principal.
*	Eixo transversal: O eixo perpendicular ao eixo principal é chamado de eixo transversal. Sua direção depende da direção do eixo principal.
*	cross-start | cross-end: Linhas flex são preenchidas com ítens e adicionadas ao container, começando pelo lado cross start do flex container em direção ao lado cross end.
*	cross size: A largura ou altura de um flex item, dependendo do que estiver na dimensão transversal, é o cross size do íten. A propriedade cross size pode ser tanto a largura quanto a altura do ítem, o que estiver na transversal.

## ELEMENTOS PAIS
### display:
Define o flex conteiner; em linha ou em bloco dependendo dos valores passados. Colacando os elementos filhos em um contexto flex.
### justify-content:
Esta propriedade define o alinhamento dos ítens ao longo do eixo principal. Ajuda a distribuir o espaço livre que sobrar no container tanto se todos os flex items em uma linha são inflexíveis, ou são flexíveis mas já atingiram seu tamanho máximo. Também exerce algum controle sobre o alinhamento de ítens quando eles ultrapassam o limite da linha.
* flex-start (padrão): os ítens são alinhados junto à borda de início (start) de acordo com qual for a flex-direction do container.
* flex-end: os ítens são alinhados junto à borda final (end) de acordo com qual for a flex-direction do container.
* center: os ítens são centralizados na linha.
* space-between: os ítens são distribuídos de forma igual ao longo da linha; o primeiro ítem junto à borda inicial da linha, o último junto à borda final da linha.
* space-around: os ítens são distribuídos na linha com o mesmo espaçamento entre eles. Note que, visualmente, o espaço pode não ser igual, uma vez que todos os ítens tem a mesma quantidade de espaço dos dois lados: o primeiro item vai ter somente uma unidade de espaço junto à borda do container, mas duas unidades de espaço entre ele e o próximo ítem, pois o próximo ítem também tem seu próprio espaçamento que está sendo aplicado.
### flex-direction:
Estabelece o eixo principal, definindo assim a direção em que os flex items são alinhados no flex container. O Flexbox é (com exceção de um wrapping opcional) um conceito de leiaute de uma só direção. Pense nos flex items inicialmente posicionais ou em linhas horizontais ou em colunas verticais.
* row (padrão): esquerda para a direita em ltr (left to right), direita para a esquerda em rtl (right to left)
* row-reverse: direita para a esquerda em ltr, esquerda para a direita em rtl
* column: mesmo que row, mas de cima para baixo
* column-reverse: mesmo que row-reverse mas de baixo para cima
### flex-wrap:
Por padrão, os flex items vão todos tentar se encaixar em uma só linha. Com esta propriedade você pode modificar esse comportamento e permitir que os ítens quebrem para uma linha seguinte conforme for necessário.
* nowrap (padrão): todos os flex items ficarão em uma só linha
* wrap: os flex items vão quebrar em múltiplas linhas, de cima para baixo
* wrap-reverse: os flex items vão quebrar em múltiplas linhas de baixo para cima
### flex-flow:
A propriedade flex-flow é uma propriedade shorthand (uma mesma declaração inclui vários valores relacionados a mais de uma propriedade) que inclui flex-direction e flex-wrap. Determina quais serão os eixos pricipal e transversal do container. O valor padrão é row nowrap.
### align-items:
* stretch (padrão): estica os ítens para preencher o container, respeitando o min-width/max-width).
* flex-start/ start / self-start: ítens são posicionados no início do eixo transversal. A diferença entre eles é sutil e diz respeito às regras de flex-direction ou writing-mode.
* center: ítens são centralizados no eixo transversal.
* baseline: ítens são alinhados de acordo com suas baselines.
### align-content:
Organiza as linhas dentro de um flex container quando há espaço extra no eixo transversal, similar ao modo como justify-content alinha ítens individuais dentro do eixo principal. Esta propriedade não tem efeito quando há somente uma linha de flex items no container.
* flex-start / start: ítens alinhados com o início do container. O valor (com maior suporte dos navegadores) flex-start se guia pela flex-direction, enquanto start se guia pela direção do writing-mode.
* flex-end / end: ítens alinhados com o final do container. O valor (com maior suporte dos navegadores) flex-end se guia pela flex-direction, enquanto end se guia pela direção do writing-mode.
* center: ítens centralizados no container.
* space-between: ítens distribuídos igualmente; a primeira linha junto ao início do container e a última linha junto ao final do container.
* space-around: ítens distribuídos igualmente com o mesmo espaçamento entre cada linha.
* space-evenly: ítens distribuídos igualmente com o mesmo espaçamento entre eles.
* stretch (padrão): ítens em cada linha esticam para ocupar o espaço remanescente entre elas.

## ELEMENTOS FILHOS
### flex:
Esta é a propriedade shorthand para flex-grow, flex-shrink e flex-basis, combinadas. O segundo e terceiro parâmetros (flex-shrink e flex-basis) são opcionais. O padrão é 0 1 auto, mas se você definir com apenas um número, é equivalente a 0 1.
### order:
Determina a ordem em que os elementos aparecerão.
Por padrão os flex items são dispostos na tela na ordem do código. Mas a propriedade order controla a ordem em que aparecerão no container.
### align-self:
Permite que o alinhamento padrão (ou o que estiver definido por align-items) seja sobrescrito para ítens individuais. Veja a propriedade align-items para entender quais são os possíveis valores.
