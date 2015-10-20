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
  transition-property: [property];
  transition-duration: [time];
  transition-timing-function: [timing];
  transition-delay: [time];
}
/* Short syntax */
seletor {
  transition: [property] [time] [timing] [time];
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
/* translate: move o elemento no eixo X (à direita) e Y (abaixo) */
seletor {
  transform: translate([x-pixels],[y-pixels]);
}
/* rotate: gira o elemento em X graus em sentido horário (positivo) ou anti-horário (negativo) */
seletor {
  transform: rotate([degrees]);
}
/* scale: aumenta ou diminui o tamanho original do elemento no número de vezes informado para a largura e 
altura*/
seletor {
  transform: scale([*width],[*height]);
}
/* skewX: torce ou inclina o elemento no eixo X, conforme os graus informados */
seletor {
  transform: skewX([degrees]);
}
/* skewY: torce ou inclina o elemento no eixo Y, conforme os graus informados */
seletor {
  transform: skewY([degrees]);
}
/* skew: torce ou inclina o elemento no eixo X e Y, conforme os graus informados */
seletor {
  transform: skew([x-degrees],[y-degrees]);
}
/* matrix: combina todos os métodos anteriores em um só, passando 6 parâmetros representando uma matriz que 
será utilizada para transformar o elemento */
seletor {
  transform: matrix([p1],[p2],[p3],[p4],[p5],[p6]);
}
```
As transformações 3D são:
```css
/* rotateX: gira o elemento no eixo X, conforme os graus informados */
seletor {
  transform: rotateX([degrees]);
}
/* rotateY: gira o elemento no eixo Y, conforme os graus informados */
seletor {
  transform: rotateY([degrees]);
}
/* rotateZ: gira o elemento no eixo Z, conforme os graus informados */
seletor {
  transform: rotateZ([degrees]);
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

#### Funcionalidade: 3
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

#### Funcionalidade: 4
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

#### Funcionalidade: 5
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

#### Funcionalidade: 6
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

#### Funcionalidade: 6
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

#### Funcionalidade: 7
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

#### Funcionalidade: 8
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

#### Funcionalidade: 9
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

[http://www.w3.org/TR/css3-transitions/](http://www.w3.org/TR/css3-transitions/)
