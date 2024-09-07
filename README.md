# POC 01

# O que é Flexbox

O Flexbox é um módulo de layout que oferece uma maneira mais eficiente de organizar, alinhar e distribuir espaço entre os itens dentro de um contêiner. Ele foi projetado para ser flexível, permitindo que os itens se ajustem automaticamente, seja expandindo para preencher o espaço disponível ou encolhendo para evitar transbordamentos, mesmo quando o tamanho dos itens é desconhecido ou dinâmico.
A principal vantagem do Flexbox é a sua capacidade de adaptar os itens do contêiner para ocupar o espaço disponível de forma otimizada, considerando diferentes dispositivos e tamanhos de tela. Diferente dos layouts tradicionais, como o layout em bloco (vertical) e o layout em linha (horizontal), o Flexbox é agnóstico à direção, o que significa que ele pode organizar os itens em qualquer direção, tornando-o ideal para componentes de uma aplicação e layouts de pequena escala, onde é necessário lidar com mudanças de orientação, redimensionamento e outras dinâmicas.

# Noções básicas e termologia

O Flexbox é um módulo abrangente que consiste em várias propriedades, não se limitando a apenas uma. Algumas dessas propriedades são aplicadas diretamente ao contêiner (o elemento pai, conhecido como flex container), enquanto outras são definidas nos elementos filhos, chamados de flex items.
Enquanto o layout tradicional utiliza as direções block e inline, o layout Flex é orientado pelas direções "flex flow". O diagrama da especificação a seguir ilustra a ideia central do layout Flex, mostrando como ele organiza e distribui os elementos dentro do contêiner de maneira flexível e adaptável.
 
# Os ítens serão dispostos no leiaute seguindo ou o eixo principal ou o transversal.

•	Eixo principal: o eixo principal de um flex container é o eixo primário e ao longo dele são inseridos os flex items. Cuidado: O eixo principal não é necessariamente horizontal; vai depender da propriedade flex-direction (veja abaixo).
•	main-start | main-end: os flex items são inseridos dentro do container começando pelo lado start, indo em direção ao lado end.
•	Tamanho principal: A largura ou altura de um flex item, dependendo da direção do container, é o tamanho principal do ítem. A propriedade de tamanho principal de um flex item pode ser tanto width quanto height, dependendo de qual delas estiver na direção principal.
•	Eixo transversal: O eixo perpendicular ao eixo principal é chamado de eixo transversal. Sua direção depende da direção do eixo principal.
•	cross-start | cross-end: Linhas flex são preenchidas com ítens e adicionadas ao container, começando pelo lado cross start do flex container em direção ao lado cross end.
•	cross size: A largura ou altura de um flex item, dependendo do que estiver na dimensão transversal, é o cross size do íten. A propriedade cross size pode ser tanto a largura quanto a altura do ítem, o que estiver na transversal.
