#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Daniel Sonda
## Artigo de revisão de CSS3
#### Funcionalidade: transition
##### O que é?
As transições em CSS3 permitem alterar os valores das propriedades de modo suave, especificando o tempo de duração desta transição. Para criar o efeito de transição, é necessário informar a propriedade CSS que se deseja alterar e o tempo de duração que o efeito terá. É imprescindível informar o tempo de duração, pois, caso omitido, o valor default é 0, fazendo com que a transição não seja realizada. É possível informar mais de uma propriedade, cada uma com a respectiva duração do efeito, a curva de velocidade a ser aplicada no efeito (transition-timing-function) e um atraso no início do efeito  (transition-delay). O efeito será iniciado quando a propriedade especificada sofrer alguma alteração, geralmente quando o usuário passar o mouse sobre o elemento.
##### Onde usar:
Em propriedades do tipo *animatable*, que são propriedades que podem mudar gradualmente de um valor para outro, como tamanho, números, percentual e cores.
##### Como usar:
```css
/* Standard syntax */
seletor {
  transition-property: none|all|property|initial|inherit;
  transition-duration: time|initial|inherit;
  transition-timing-function: ease|linear|ease-in|ease-out|ease-in-out|cubic-bezier()|initial|inherit;
  transition-delay: time|initial|inherit;
}
/* Short syntax */
seletor {
  transition: property duration timing-function delay|initial|inherit;
}
```
##### Exemplo de uso
O exemplo abaixo exibe um elemento *div* vermelho de 100 x 100 px, adicionando um efeito de transição nas propriedades *with* e *height* com duração de 2 e 4 segundos, respectivamente.
```css
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s, height 4s linear 1s;
}
```
O efeito seria iniciado quando a propridade fosse alterada ao passar o mouse sobre o elemento, conforme o exemplo abaixo:
```css
div:hover {
  width: 300px;
  height: 300px;
}
```

#### Funcionalidade: transform
##### O que é?
As transformações em CSS3 permitem alterar a posição, girar, torcer/inclinar e aumentar ou diminuir os elementos, permitindo assim mudar sua forma, tamanho e posição, suportando 2D e 3D.
##### Onde usar:
Em qualquer elemento do tipo *transformable*, cujo layout é controlado pelo *CSS box model*.
##### Como usar:
As transformações 2D são:
```css
/* translate: move o elemento no eixo X (à direita) e Y (abaixo) em pixels */
seletor {
  transform: translate(x,y);
}
/* rotate: gira o elemento em X graus em sentido horário (positivo) ou anti-horário (negativo) */
seletor {
  transform: rotate(angle);
}
/* scale: aumenta ou diminui o tamanho original do elemento no número de vezes informado para a largura e 
altura */
seletor {
  transform: scale(x,y);
}
/* skewX: torce ou inclina o elemento no eixo X, conforme o ângulo informado */
seletor {
  transform: skewX(angle);
}
/* skewY: torce ou inclina o elemento no eixo Y, conforme o ângulo informado */
seletor {
  transform: skewY(angle);
}
/* skew: torce ou inclina o elemento no eixo X e Y, conforme os ângulos informados */
seletor {
  transform: skew(x-angle,y-angle);
}
/* matrix: combina todos os métodos anteriores em um só, passando 6 parâmetros representando uma matriz que 
será utilizada para transformar o elemento */
seletor {
  transform: matrix(n,n,n,n,n,n);
}
```
As transformações 3D são:
```css
/* rotateX: gira o elemento no eixo X, conforme o ângulo informado */
seletor {
  transform: rotateX(angle);
}
/* rotateY: gira o elemento no eixo Y, conforme o ângulo informado */
seletor {
  transform: rotateY(angle);
}
/* rotateZ: gira o elemento no eixo Z, conforme o ângulo informado */
seletor {
  transform: rotateZ(angle);
}
```
##### Exemplo de uso
O exemplo abaixo combina as duas funcionalidades vistas até agora, exibindo um elemento *div* vermelho de 100 x 100 px, adicionando um efeito de transição nas propriedades *with* e *height* com duração de 2 segundos e uma transformação com duração de 2 segundos.
```css
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s, height 2s, transform 2s;
}
```
O efeito inicia ao passar o mouse sobre o elemento, conforme o exemplo abaixo, aumentando, girando e inclinando a imagem:
```css
div:hover {
  width: 300px;
  height: 300px;
  transform: rotate(180deg) skewX(-5deg);
}
```

#### Funcionalidade: animation
##### O que é?
Permite aplicar animações a maior parte dos elementos HTML sem utilizar JavaScript ou Flash, alterando quantas propriedades e quantas vezes quiser. Basicamente, você especifica o valores inicial, intermediários e final da propriedade (via *keyframes*), além da duração do efeito, atraso no início (delay), quantas vezes será executado, a direção (reversa ou alternada) e a curva de velocidade do efeito (Ex: mais rápida no início e mais lenta no final).
##### Onde usar:
Em propriedades do tipo animatable, que são propriedades que podem mudar gradualmente de um valor para outro, como tamanho, números, percentual e cores.
##### Como usar:
```css
/* código de animação (de..para) */
@keyframes animationname  {
  from {css-styles;}
  to {css-styles;}
}
/* código de animação (escala de percentuais) */
@keyframes animationname  {
  0% {css-styles;}
  ...
  100% {css-styles;}
}
/* aplicação da animação ao elemento */
seletor {
  animation-name: animationname;
}
```
##### Exemplo de uso
O keyframes define uma animação progressiva, alterando a cor e posição do elemento, fazendo com que ele se mova na tela contornando um quadrado imaginário, no sentido horário. Após, um elemento *div* recebe a animação com as respectivas opções.
```css
@keyframes animacao {
  0%   {background-color: red; left:0px; top:0px;}
  25%  {background-color: yellow; left:200px; top:0px;}
  50%  {background-color: blue; left:200px; top:200px;}
  75%  {background-color: green; left:0px; top:200px;}
  100% {background-color: red; left:0px; top:0px;}
}

div {
  width: 100px;
  height: 100px;
  background-color: red;
  position: relative;
  animation-name: animacao;
  animation-duration: 5s;
  animation-timing-function: ease;
  animation-delay: 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

#### Funcionalidade: multi-column
##### O que é?
Permite formatar um elemento para exibir texto em múltiplas colunas, como em um jornal. É possível definir:

 - `column-count` - quantidade de colunas.
 - `column-gap` - espaço entre as colunas, em pixels.
 - `column-rule-style` - estilo da linha divisória entre as colunas.
 - `column-rule-width` - largura da linha divisória entre as colunas.
 - `column-rule-color` - cor da linha divisória entre as colunas.
 - `column-rule` - todas as opções da linha divisória numa propriedade apenas.
 - `column-span` - a quantidade de colunas que o texto irá ocupar (geralmente o título).
 - `column-width` - sugere uma largura para as colunas.

##### Onde usar:
Em elementos que exibam texto.
##### Como usar:
```css
seletor {
  column-count: number|auto|initial|inherit;
  column-gap: length|normal|initial|inherit;
  column-rule-style: none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit;
  column-rule-width: medium|thin|thick|length|initial|inherit;
  column-rule-color: color|initial|inherit;
  column-rule: column-rule-width column-rule-style column-rule-color|initial|inherit;
  column-span: 1|all|initial|inherit;
  column-width: auto|length|initial|inherit;
}
```
##### Exemplo de uso
Elemento *div* irá exibir o texto em duas colunas, sendo que o título ocupará apenas a primeira coluna.
```css
.colunas {
  column-count: 2;
  column-gap: 50px;
  column-rule: 1px solid black;
}

h2 {
  column-span: 1;
}

<div class="colunas">
  <h2>Título</h2>
  Texto do div que será exibido em duas colunas. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. 
</div>
```

#### Funcionalidade: resize
##### O que é?
Permite ao usuário redimensionar um elemento HTML.
##### Onde usar:
Qualquer elemento.
##### Como usar:
```css
seletor {
  resize: none|both|horizontal|vertical|initial|inherit;
}
```
##### Exemplo de uso
Permite ao usuário aumentar ou reduzir a altura do elemento *div*.
```css
div {
  resize: vertical;
}
```

#### Funcionalidade: flexbox
##### O que é?
É um modo de layout novo no CSS3, que garante que os elementos se comportem de maneira previsível quando for necessário suportar diversas resoluções de tela e dispositivos. O flexbox é um container, cujos itens podem se posicionar em diversas direções e ajustar as dimensões para se adaptarem ao espaço disponível, ao longo de uma linha.
Propriedades do container flexbox:

- `display` - define o tipo do container.
- `direction` - define do container na página.
- `flex-direction` - define a direção da disposição dos itens dentro do container.
- `justify-content` - define o alinhamento horizontal dos itens dentro do container.
- `align-items` - define o alinhamento vertical dos itens dentro do container.
- `flex-wrap` - define se os itens irão automaticamente quebrar a linha na estrutura.
- `align-content` - define o alinhamento do conteúdo dentro do container (linhas).

Propriedades dos itens do container flexbox:

- `order` - define a ordem do item.
- `margin` - define a margem do item.
- `align-self` -  define o alinhamento vertical do item, sobrepondo a propriedade `align-items` do container.
- `flex` - define a proporção do item dentro do container.
##### Onde usar:
Definição da estrutura de uma página.
##### Como usar:
```css
/* container flexbox */
seletor {
  display: flex|inline-flex|<outros>;
  direction: ltr|rtl|initial|inherit;
  flex-direction: row|row-reverse|column|column-reverse|initial|inherit;
  justify-content: flex-start|flex-end|center|space-between|space-around|initial|inherit;
  align-items: stretch|center|flex-start|flex-end|baseline|initial|inherit;
  flex-wrap: nowrap|wrap|wrap-reverse|initial|inherit;
  align-content: stretch|center|flex-start|flex-end|space-between|space-around|initial|inherit;
}

/* item de container flexbox */
seletor {
  order: number|initial|inherit;
  margin: length|auto|initial|inherit;
  align-self: auto|stretch|center|flex-start|flex-end|baseline|initial|inherit;
  flex: flex-grow flex-shrink flex-basis|auto|initial|inherit;
}
```
##### Exemplo de uso
Exibe um container com três itens dispostos em coluna e centralizados verticalmente, com margem automática entre os mesmos.
```css
.flex-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 400px;
  height: 400px;
  background-color: lightgrey;
}

.flex-item {
  background-color: cornflowerblue;
  width: 100px;
  height: 100px;
  margin: auto;
}

<div class="flex-container">
  <div class="flex-item">flex item 1</div>
  <div class="flex-item">flex item 2</div>
  <div class="flex-item">flex item 3</div>  
</div>
```

#### Funcionalidade: media queries
##### O que é?
A instrução `@media` foi introduzida no CSS2 para identificar o tipo de mídia (tela de computador, impressora, dispositivos mobibe, TV) e a aplicar estilos diferentes para cada um. No CSS3, em vez de verificar o tipo do dispositivo, é possível consultar as características e capacidades do mesmo, como por exemplo a largura e altura da janela, largura e altura da tela, orientação (retrato ou paisagem) e a resolução.
##### Onde usar:
Numa página para dispositivos móveis, para ajustar o layout conforme a orientação da tela.
##### Como usar:
```css
/* mediatype = all|print|screen|speech */
@media not|only mediatype and (expressions) {
    CSS-Code;
}
```
##### Exemplo de uso
O exemplo abaixo exibe um menu alinhado à esquerda caso a janela tenha mais que 480 pixels de largura. Caso contrário, o menu ficará no topo, ocupando toda a largura disponível.
```css
#leftsidebar {float: none;width: auto;}

.menuitem {
  background:lightblue;
  border-radius:4px;
  list-style-type:none;
  margin:4px;
  padding:2px;
}

@media screen and (min-width: 480px) {
    #leftsidebar {width:200px;float:left;}
}

<div id="leftsidebar">
  <ul id="menulist">
    <li class="menuitem">Menu-item 1</li>
    <li class="menuitem">Menu-item 2</li>
    <li class="menuitem">Menu-item 3</li>
 </ul>
</div>
```

#### Funcionalidade: backgrounds
##### O que é?
Conjunto de propriedades para configurar o fundo de um elemento, sendo possível adicionar múltiplas imagens:

- `background-image` - imagem ou imagens a serem exibidas.
- `background-position` - posição da imagem no fundo.
- `background-repeat` - define se a imagem será repetida até preencher o espaço.
- `background-size`- tamanho da imagem a ser exibida.
- `background-origin` - define a origem da posição da imagem.
- `background-clip` - define a área de desenho da imagem.

##### Onde usar:
Em qualquer elemento que seja deseja exibir uma imagem de fundo.
##### Como usar:
```css
seletor {
  background-image: url|none|initial|inherit;
  background-size: auto|length|cover|contain|initial|inherit;
  background-origin: padding-box|border-box|content-box|initial|inherit;
  background-clip: border-box|padding-box|content-box|initial|inherit;     
}
```
##### Exemplo de uso
A imagem cobrirá toda a janela do browser, centralizada e mantendo a proporção original, sem barras de rolagem.
```css
html {
  background: url(img_flower.jpg) no-repeat center center fixed;
  background-size: cover;
}
```

#### Funcionalidade: border images
##### O que é?
Utilizar uma imagem como borda de um elemento, definindo como a imagem será cortada e se as seções do meio da borda deverão esticar a imagem ou repeti-la. A imagem sempre será cortada em nove pedaços: quatro cantos, quatro  lados e um centro.
##### Onde usar:
Em qualquer elemento que suporte a propriedade `border`.
##### Como usar:
```css
seletor {
  border: border-width border-style border-color|initial|inherit;
  border-image: source slice width outset repeat|initial|inherit;
}
```
##### Exemplo de uso
A imagem será cortada em pedaços de 30 pixels, que serão ajustados automaticamente para preencher toda a extensão da borda do elemento.
```css
#borderimg { 
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 round;
}
```

#### Funcionalidade: 10
##### O que é?
Texto.
##### Onde usar:
Texto.
##### Como usar:
```css
seletor {
  ?
}
```
##### Exemplo de uso
Texto.
```css
div {
  ?
}
```

### Referências:
[http://www.w3schools.com/css/default.asp](http://www.w3schools.com/css/default.asp)

[http://www.w3schools.com/cssref/](http://www.w3schools.com/cssref/)

[http://www.w3.org/TR/css3-transitions/](http://www.w3.org/TR/css3-transitions/)
