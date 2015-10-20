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
Em qualquer propriedade do tipo *animatable*, que são propriedades que podem mudar gradualmente de um valor para outro, como tamanho, números, percentual e cores.
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
### Referencia:
[http://www.w3schools.com/css/default.asp](http://www.w3schools.com/css/default.asp)
[http://www.w3.org/TR/css3-transitions/](http://www.w3.org/TR/css3-transitions/)
