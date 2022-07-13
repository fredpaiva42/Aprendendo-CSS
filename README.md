# Aprendendo CSS

Podemos adicionar estilo a um elemento, especifiando-o dentro do `<style>` e definindo uma propriedade para ele.
```CSS
element {
    property: value;
}
```
Para centralizar um texto podemos usar o *seletor de tipo* para o elemento que estamos querendo estilizar e definindo a propriedade `text-align` com o valor **center**.
```CSS
h1 {
    text-align: center;
}
```
Quando temos muitos tipos de seletores com o mesmo estilo, podemos adicionar o mesmo grupo de estilo a muitos elementos, criando uma lista de seletores. Cada seletor é separado por vírgula.
```CSS
h1, h2, p {
    text-align: center;
}
```
Estilizar os elementos dentro da tag `<style>` no nosso arquivo **HTML** funciona, porém não é a melhores da práticas, isso quando se tem muitos estilos torna o arquivo gigante e também não facilita a leitura. Por isso, o importante é que criemos um **arquivo CSS separado** apenas para a estilização e vinculá-lo ao nosso **HTML**.

Com o arquivo **CSS** criado, é preciso linká-lo ao nosso **HTML**. Para fazer isso precisamos adicionar a tag `<link>` no `<head>`, adicionando o atributo `rel` com o valor **stylesheet** e o atributo `href` com o valor do caminho ou nome do arquivo **CSS**.

É importante que a estilização da página fique semelhante em qualquer disposito, então para isso precisamos adicionar outra tag `<meta>` no nosso `<head>` com um atributo especial chamado **content**.
```HTML
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
```
Quando quisermos alterar a cor do corpo da página, basta usar o *seletor* `body` e adicionar a propriedade `background-color` e nome da cor que queremos.
```CSS
body {
    background-color: brown;
}
```
O elemento `<div>` é usado principalmente para fins de layout de design.

Para ajustar a largura dos elementos na página, devemos usar a propriedade `width`. o valor do width pode ser especificada em pixels (`px`) ou em porcentagem (`%`), com a porcentagem o elemento que está sendo estilizado vai ter a largura daquela porcentagem baseada no seu elemento pai.

Comentários em CSS:
```CSS
/* Assim que se faz comentários em CSS */
```

Uma maneira de centralizar um elemento horizontalmente é definindo as propriedades `margin-left` e `margin-right` com o valor **auto**.

**Seletor de classe** é definido por um nome com um ponto na frente:
```css
.class-name {
    styles
}
```

Para adicionar uma imagem de fundo na página podemos usar a propiedade `background-image`:
```CSS
body{
background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg)
}
```
Elementos `article` comumente contêm vários elementos que possuem informações relacionada.

Elementos `p` são elementos *em nível de bloco*, então eles ocupam toda a largura do seu elemento pai. Para mudar essa característica, podemos adicionar a propriedade `display` com valor **inline-block** e assim estilizando os elementos `p`, eles vão se comportar mais como elementos em linha. 

Os elementos com a propriedade **inline-block** só ocupam a largura do seu conteúdo. Então para distribuí-los é preciso que o elementos tenham seu **width** ajustado.

Para mexer no espaçamento interno de um elemento, nós podemos usar a propriedade `padding`.
```CSS
.menu{
    width: 80%;
    background-color: burlywood;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
}
```

Para evitar que em telas muito amplas os elementos fiquem muito distantes um do outro, podems fazer uso da propriedade `max-width`.

É possível alterar o estilo de fonte com `font-family`, para que o texto fique diferente do estilo de fonte padrão do navegador. Cada navegador tem algumas fontes comuns já disponíveis. É bom adicionar um valor de **fallback** para a `font-family` adicionando outro nome de fonte separado por uma vírgula. Os fallbacks são usados em instâncias onde a fonte inicial não é encontrada ou não está disponível.
```CSS
h1 {
    font-family: Heveltica, Impact; /*Nesse caso a Impact é o nosso fallback*/
}
```

Conseguimos alterar o estilo das fontes com a propriedade `font-style`, nela temos os valores como **bold**, **italic** e etc.

A tipografia dos elementos do cabeçalho (por exemplo, `h1`, `h2`) é definida por valores padrão dos navegadores. Porém podem ser alteradas com a propriedade `font-size`.

Com o elemento `<hr>` podemos dividir as seções de conteúdo diferente com uma linha. As propriedades padrões farão com que o `<hr>` apareça como uma linha cinza claro fina. 

Você muda as propriedade de um link quando o link tenha sido visitado de fato usando um *pseudosseletor*:
```CSS
a:visited {
    color: gray;
}
```

Você muda as propriedades de um link quando o mouse passa sobre ele usando um *pseudosseletor*:
```CSS
a:hover {
    color: brown;
}
``` 

Você muda as propriedades de um link quando o link tiver sido clicado de fato usando um *pseudosseletor*:
```CSS
a:active {
    color: white;
}
```
