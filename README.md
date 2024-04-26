# Siga as instruções para finalizar o projeto dessa aula. 
Nessa aula nós construímos a  **seção escola**  da nossa página. Vamos checar o passo a passo?

## Analisando o protótipo

Observe a seção abaixo do cabeçalho no seu protótipo para se basear na criação de cores e textos no código. No exemplo do vídeo, a seção deverá ficar assim:

![alt text: A imagem mostra um site com cabeçalho com a logo da alurastart no lado esquerdo no canto superior sendo que a palavra "alura" escrita na cor branca e a palavra "start" nas cores vermelho, amarelo, azul, roxo e verde. Do outro lado, mas ainda no canto superior, existem duas palavras: escola e estudante, ambas na cor branca. A cor de fundo do cabeçalho é um tom de azul escuro. Mais embaixo, a cor de fundo começa com o mesmo tom de azul escuro e até ao final da página para um azul mais claro com contraste mais forte. No meio dessa transição de cores azul existe um texto em branco explicando algumas informações sobre a escola. Os textos estão no lado direito um texto embaixo do outro e uma imagem  de uma professora escrevendo no quadro mais para o lado esquerdo. Esta seção está destacada por um retângulo vermelho.](https://cdn3.gnarususercontent.com.br/3594+-+P%C3%A1gina+web%3A+utilizando+HTML+e+CSS+para+construir+um+site+criativo/img/aula04_FCF-01.png)

Para conseguir esse resultado, é necessário  **unir os elementos**  a seguir: parágrafos, imagem e textos.

Sendo assim, abaixo do  `header`, adicione a tag  `section`  de classe  `"escola"`  para criar uma nova seção:

```html
<header class="cabecalho">
    <img class="cabecalho-imagem" src="alurastart logo.png" alt="logo da alura start">
    <ul class="cabecalho-lista">
        <li class="cabecalho-lista-item">Escola</li>
        <li class="cabecalho-lista-item">Estudante</li>
    </ul>
</header>

<section class="escola">
    
</section>

```

Dentro dela, adicione a tag  `div`  de classe  `"escola-div-conteudo"`, que indicará uma  **divisão**  dentro da seção:

```html
<section class="escola">
    <div class="escola-div-conteudo">
    
    </div>
</section>

```

Agora, dentro da  `div`  criada, adicione um título  `h2`  de classe  `"escola-titulo"`  com o texto  **"Sobre a nova escola"**.

```html
<section class="escola">
    <div class="escola-div-conteudo">
        <h2 class="escola-titulo">Sobre a escola</h2>
    </div>
</section>

```

Em seguida,  **copie o texto do protótipo**  e cole ele dentro de duas tags  `p`  de classes  `"escola-texto-um"`  e  `"escola-texto-dois"`:

```html
<section class="escola">
    <div class="escola-div-conteudo">
        <h2 class="escola-titulo">Sobre a Escola</h2>
        <p class="escola-texto-um">A Escola Alura foi fundada em 2010 e tem como objetivo ensinar Pensamento Computacional, através do ensino de  Programação.</p>
        <p class="escola-texto-dois">A turma mais estudiosa e famosa é a Segunda Série A. Nós somos super unidos e a turma favorita por todos os professores e professoras que nos ajudam!</p>
    </div>
</section>

```

> Cada tag  `p`  equivale a  **1 linha**, por isso quebramos o texto em duas tags.

Pronto! Todos os textos foram adicionados à página.

![alt text: Captura de tela do projeto no navegador contendo o título 'Sobre a escola" e o texto: "A escola Alura foi fundada em 2010 com o objetivo de ensinar Pensamento Computacional através da Programação. A turma mais famosa é a Segunda Série A. Uma turma diversa e engajada, as vezes, um pouco bagunceira, mas que entrega excelentes resultados!"](https://cdn3.gnarususercontent.com.br/3594+-+P%C3%A1gina+web%3A+utilizando+HTML+e+CSS+para+construir+um+site+criativo/img/aula04_FCF-02.png)

## Adicionando a imagem

Podemos adicionar uma imagem já existente ou da internet. No exemplo do vídeo, pegamos uma imagem do site  [Storyset](https://storyset.com/).

> Nunca se esqueça de checar se a imagem é 100% grátis, de domínio público ou possui direitos autorais, ok?

Após baixar a sua imagem adicione no HTML, dentro da  `section`, uma tag  `img`  de classe  `"escola-imagem"`, identificando seu  **caminho**  e  **texto alternativo**:

```html
<section class="escola">
    <div class="escola-div-conteudo">
        <h2 class="escola-titulo">Sobre a Escola</h2>
        <p class="escola-texto-um">A Escola Alura foi fundada em 2010 e tem como objetivo ensinar Pensamento Computacional, através do ensino de  Programação.</p>
        <p class="escola-texto-dois">A turma mais estudiosa e famosa é a Segunda Série A. Nós somos super unidos e a turma favorita por todos os professores e professoras que nos ajudam!</p>
    </div>
    <img class="escola-imagem" src="Formula-bro.png" alt="Professora no quadro">
</section>

```

Em seguida no CSS, crie um seletor (`.`) para a classe  `escola-imagem`, determinando uma  **largura**  `width`  de  `25%`:

```css
.escola-imagem{
    width: 25%;
}

```

Pronto, nossa imagem já foi adicionada e está no tamanho ideal!

## Adicionando cores

Para criar um gradiente no plano de fundo, no CSS crie um seletor (`.`) para a classe  `escola`, adicionando nele a propriedade  `background-image`  de valor  `linear-gradiente()`:

```css
.escola{
    background-image: linear-gradient();
}

```

Dentro do  `linear-gradient()`, adicione a  **cor inicial**  (`#424E61`) e a  **cor final**  (`#4EBFE9`), separando-as por vírgulas:

```css
.escola{
    background-image: linear-gradient(#424E61, #4EBFE9);
}

```

Você também pode adicionar a propriedade  `color`  de valor  `white`  para determinar a  **cor do texto**:

```css
.escola{
    background-image: linear-gradient(#424E61, #4EBFE9);
    color: white;
}

```

Insira um  `display`  de valor  `flex`  para alinhar os itens de forma flexível:

```css
.escola{
    background-image: linear-gradient(#424E61, #4EBFE9);
    color: white;
    display: flex;
}

```

Observe como está ficando nossa seção!

![alt text: A imagem mostra a seção "escola" do projeto", a cor de fundo começa com o mesmo tom de azul escuro e até ao final da página para um azul mais claro com contraste mais forte. No meio dessa transição de cores azul existe um texto em branco explicando algumas informações sobre a escola. Os textos estão no lado direito um texto embaixo do outro e uma imagem  de uma professora escrevendo no quadro mais para o lado esquerdo](https://cdn3.gnarususercontent.com.br/3594+-+P%C3%A1gina+web%3A+utilizando+HTML+e+CSS+para+construir+um+site+criativo/img/aula04_FCF-03.png)

## Alinhando os conteúdos

Vamos alinhar os conteúdos na página!

Crie um seletor (`.`) para a classe  `escola-div-conteudo`  e adicione uma largura  `width`  de valor  `35%`:

```css
.escola-div-conteudo{
    width: 35%;
}

```

Crie também um seletor (`.`) para a classe  `escola-titulo`, adicionando nele um espaçamento  `padding`  de valores  `24px 0`:

```css
.escola-titulo{
    padding: 24px 0;
}

```

Agora no seletor da classe  `escola`, adicione a propriedade  `justify-content`  de valor  `center`, para alinhar todos os itens ao centro da tela:

```css
.escola{
    background-image: linear-gradient(#424E61, #4EBFE9);
    color: white;
    display: flex;
    justify-content: center;
}

```

Adicione também a propriedade  `align-items`  de valor  `center`:

```css
.escola{
    background-image: linear-gradient(#424E61,#16CFF8);
    color:white;
    display: flex;
    justify-content: center;
    align-items: center;
}

```

Por fim, insira um espaçamento  `padding`  de valores  `24px 0`:

```css
.escola{
    background-image: linear-gradient(#424E61,#16CFF8);
    color:white;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 24px 0;
}

```

Nosso site estará cada vez mais parecido com nosso protótipo, como você pode observar na imagem abaixo:

![alt text: Entrega parcial do site desenvolvido.A imagem mostra um site com cabeçalho com a logo da alurastart no lado esquerdo no canto superior sendo que a palavra "alura" escrita na cor branca e a palavra "start" nas cores vermelho, amarelo, azul, roxo e verde. Do outro lado, mas ainda no canto superior, existem duas palavras: escola e estudante, ambas na cor branca. A cor de fundo do cabeçalho é um tom de azul escuro. Mais embaixo, a cor de fundo começa com o mesmo tom de azul escuro e até ao final da página para um azul mais claro com contraste mais forte. No meio dessa transição de cores azul existe um texto em branco explicando algumas informações sobre a escola. Os textos estão no lado direito um texto embaixo do outro e uma imagem  de uma professora escrevendo no quadro mais para o lado esquerdo](https://cdn3.gnarususercontent.com.br/2881-html-css-start/01/aula11-figura08.png)

Aproveite este momento para explorar sua criatividade, utilizando cores, imagens e fontes da sua preferência!

## Código final

Ao final da aula, seu código HTML deve ficar da seguinte forma:

```xml
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header class="cabecalho">
        <img class="cabecalho-imagem" src="alurastart logo.png" alt="logo da alura start">
        <ul class="cabecalho-lista">
            <li class="cabecalho-lista-item">Escola</li>
            <li class="cabecalho-lista-item">Estudante</li>
        </ul>
    </header>


    <section class="escola">
        <div class="escola-div-conteudo">
            <h2 class="escola-titulo">Sobre a Escola</h2>
            <p class="escola-texto-um">A Escola Alura foi fundada em 2010 e tem como objetivo ensinar Pensamento Computacional, através do ensino de  Programação.</p>
            <p class="escola-texto-dois">A turma mais estudiosa e famosa é a Segunda Série A. Nós somos super unidos e a turma favorita por todos os professores e professoras que nos ajudam!</p>
        </div>
        <img class="escola-imagem" src="Formula-bro.png" alt="Professora no quadro">
    </section>
</body>

</html>

```

Já o CSS ficará assim:

```css
* {
    margin: 0;
    padding: 0;
}

.cabecalho {
    background-color: #424E61;
    color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding: 24px 0;
}

.cabecalho-imagem{
    width: 15%;
}

.cabecalho-lista-item{
    display: inline-block;
    margin: 0 16px;
    font-size: 20px;
}

.escola-imagem{
    width: 25%;
}

.escola{
    background-image: linear-gradient(#424E61,#16CFF8);
    color:white;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 24px 0;
}

.escola-div-conteudo{
    width: 35%;
}
.escola-titulo{
    padding: 24px 0;
}
```
