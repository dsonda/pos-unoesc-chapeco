## Atomic Design
Daniel Sonda (Unoesc Chapecó)</br>
{dsonda@gmail.com}
#####Resumo:
A necessidade de prototipar interfaces com design responsivo, considerando a diversidade atual de dispositivos, demanda um esforço muito grande de designers e desenvolvedores. Em vez de utilizar ferramentas como o Photoshop para a criação dos layouts, esta nova metodologia sugere o uso de componentes modulares vivos, funcionais e reutilizáveis. 
#####1) O que é?
O Atomic Design ou Design Atômico, em português, é uma criação do webdesigner Brad Frost, que se baseou nas aulas de química para explicar como os componentes de uma página interagem. Segundo ele, as páginas são sistemas formados por elementos simples que, quando integrados, podem criar sistemas complexos, mas organizados, da mesma forma que átomos se ligam para criar moléculas e organismos na natureza. 
#####2) Como funciona
O Atomic Design estabelece os seguintes conceitos ou etapas pelos quais você deverá passar:
######Átomos
Assim como na natureza, são os menores elementos, que neste caso são as tags HTML: labels, inputs, botões, parágrafos. Sozinhos eles são abstratos e não fazem muito sentido, mas são utilizados para construir componentes maiores e mais complexos.
######Moléculas
Juntando um ou mais átomos, cria-se uma molécula, que faz com que os átomos funcionem com um objetivo único, criando um componente mais concreto. Por exemplo, um label, uma caixa de texto e um botão podem formar um componente de pesquisa.
######Organismos
A junção de diferentes moléculas cria um organismo, que numa página resulta em uma seção distinta. Por exemplo, um logotipo, menu, campos de pesquisa e de login, podem criar o cabeçalho de uma página. Organismos podem ser criados pensando num padrão modular e reutilizável.
######Templates
Nesta etapa diversos organismos são acoplados para se criar um modelo vivo, ou seja, o esqueleto de uma página HTML funcional, mas de baixa fidelidade (wireframes). Neste momento, já é possível validar o layout com o cliente, pois foi produzido algo concreto, do ponto de vista dele.
######Pages
Adicionando-se conteúdo a um template, tem-se uma página, com cores, tipografia, imagens e vídeos, facilitando a validação do template e identificação de ajustes necessários, culminando no produto final.
#####3) Para que usar
Facilitar a criação de layouts através do uso modular e progressivo de componentes dinâmicos, aumentando a rapidez e produtividade dos designer e desenvolvedores, pela facilidade de experimentação, alterando a combinação dos elementos para criação de novas estruturas.
No lugar de apresentar para o cliente modelos estáticos, é possível criar desde o início um protótipo responsivo, que poderá ser testado e evoluído diretamente nos dispositivos que irão executá-lo.
#####4) Onde usar?
No desenvol vimento de sistemas responsivos que necessitem de uma de interface com o usuário padronizada e bem definida. Sites estáticos, onde a reutilização de componentes não se faz tão necessário, podem não se beneficiar muito desta metodologia. 
#####5) Exemplos:
######Átomos
```html
<input type="submit" value="Submit">
```
######Moléculas
```html
<form>
  Pesquise no site: <input type="text" name="busca">
  <input type="submit" value="Pesquisar">
</form>
```
######Organismos
![Organismo](http://bradfrost.com/wp-content/uploads/2013/06/organism2.jpg)
######Templates
![Template](http://bradfrost.com/wp-content/uploads/2013/06/template1.jpg)
######Pages
![Página](http://bradfrost.com/wp-content/uploads/2013/06/page1.jpg)
#####6) Referências
[http://tableless.com.br/o-que-e-design-atomic/](http://tableless.com.br/o-que-e-design-atomic/)</br>
[http://pt.slideshare.net/bradfrostweb/atomic-design](http://pt.slideshare.net/bradfrostweb/atomic-design)</br>
[http://bradfrost.com/blog/post/atomic-web-design/](http://bradfrost.com/blog/post/atomic-web-design/)</br>
[http://nomadev.com.br/atomic-design-por-que-usar/](http://nomadev.com.br/atomic-design-por-que-usar/)</br>
[http://nomadev.com.br/atomic-design-com-angularjs/](http://nomadev.com.br/atomic-design-com-angularjs/)</br>
