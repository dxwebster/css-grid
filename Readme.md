<h1>Desvendando o CSS-GRID</h1>

<h2>Alinhamento de Itens</h2>
<p>Aqui estamos utilizando um grid com 3 linhas em 3 colunas, onde cada todos os item são alinhados juntos, nesse caso, ao centro de sua respectiva célula. Pra isso utilizamos o justify-items, onde o <b>align-items</b> refere-se ao alinhamento <b>vertical</b> e o <b>justify-items</b> ao alinhamento <b>horizontal</b>.</p>
<p>Podemos usar 4 valores: start, end, center, stretch</p>
      
```css
.container{
    display: grid;
    grid-template: 1fr 1fr 1fr / 1fr 1fr 1fr ;
    align-items: center;
    justify-items: center;
}
```
<img src="readme/01.png"/>

<h2>Alinhamento Self</h2>
<p>Aqui temos um grid também com 3 linhas e 3 colunas, mas podemos trabalhar individualmente no alinhamento de itens. Basta setar o 'align/justify-self' no elemento filho do container que eu quero alinhar. No exemplo abaixo, os items em verde estão recebendo a classe 'center' que contém os alinhamnetos ao centro. </p>

```css
.container{
    display: grid;
    grid-template: 1fr 1fr 1fr/1fr 1fr 1fr;
}

.center {
    align-self: center;
    justify-self: center;
    background-color: green;
}

```
<img src="readme/02.png"/>

<h2>Alinhamento de Content</h2>
<p>Aqui temos um grid também com 3 linhas e 3 colunas, mas podemos trabalhar no alinhamento do próprio grid, utilizando o 'justify/align-content'.</p>

<p>O uso dessas propriedades são raras, pois só é aplicado caso o grid seja menor que a area definida. (Por exemplo, quando usamos em px o tamanho do grid, poderemos terminar com um grid pequeno, para o tamanho da area do grid)</p>

<p>Podemos usar 7 valores: start, end, strech, space-between, space-around, space-evenly.</p>

```css
.container{
    display: grid;
    grid-template: 10px 10px 10px / 10px 10px 10px;
    align-content: center;
    justify-content: center;
}
 ```

<img src="readme/03.png"/>


<section>
<h2>Alinhamento por Template</h2>
<p>Por meio do grid-template-areas podemos alinhar os elementos onde quisermos dentro de um container.</p>

```css
.container{
    display: grid;
    grid-template: 20vh 30vh 10vh/3fr 1fr;

    grid-template-areas:
    "header header"
    "main aside"
    "footer footer";
}
```

<p>E para cada item eu defino, o nome com o 'grid-area'</p>

```css
header  {background: yellow; grid-area: header}
main    {background: blue; grid-area: main}
aside   {background: green; grid-area: aside}
footer  {background: red; grid-area: footer}
```

<img src="readme/04.png"/>


