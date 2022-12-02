# P-gina-de-receitas
Desafio "Página de Receita" do Discover da Rocketseat.
Nesse desafio você deverá criar uma página web de uma receita com título, imagem, lista de ingredientes e modo de preparo. O desafio está dividido em duas partes, no primeiro momento você irá criar a estrutura HTML com as informações da receita e na segunda parte será o momento de adicionar os estilos à página com o CSS.
<img src="https://github.com/igorbeckt/P-gina-de-receitas/blob/master/assets/pronto.png?raw=true">
## Iniciando o projeto

Para iniciar o projeto devemos criar a estrutura HTML base. Você deve iniciar **criando a pasta** onde vai colocar os arquivos do projeto e dentro dela você já pode criar o arquivo **index.html** que é onde vamos escreve o HTML da página da receita.

Para criar a estrutura base do HTML no Visual Studio Code, você pode digitar `!` e `TAB` em seguida. Feito isso, você vai ficar com uma estrutura parecida com o código abaixo:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>

  </body>
</html>
```

## Construindo a estrutura HTML da página

Nessa seção você vai encontrar as instruções e dicas para resolver o desafio.

Então, bora codar! 👨‍💻👩‍💻

- A receita deve ter um **título**, para isso você pode usar uma das tags de heading (`h1`, `h2`, `h3`, `h4`, `h5`, `h6`).
    
    <aside>
    💡 Você deve escolher a tag que faz mais sentido como **título principal** da página.
    
    </aside>
    
- A receita deve ter uma **imagem** ilustrativa.
    - Adicione também uma **legenda** para a imagem.
    
    <aside>
    💡 Para adicionar uma legenda na imagem você pode usar as tags `figure` e `figcaption` como no exemplo abaixo:
    
    </aside>
    
    ```html
    <figure>
       <img src="https://unsplash.com/photos/dEUyLofZe5o" alt="Texto descritivo da imagem" />
       <figcaption>Adicionar aqui a legenda da imagem</figcaption>
    </figure>
    ```
    
    <aside>
    💡 Sites onde você pode encontrar imagens grátis para usar nos seus projetos: [Unsplash](https://unsplash.com/), [Pexels](https://www.pexels.com/pt-br/), [Pixabay](https://pixabay.com/pt/).
    
    </aside>
    
- Cada lista deve ter um **subtítulo** (`Ingredientes` e `Modo de preparo`) .
- Os ingredientes devem ser apresentados como uma **lista não ordenada** `<ul>`.
- O modo de preparo deve ser apresentado como uma **lista ordenada** `<ol>`.
- Deve ter uma seção `Informações adicionais` com um **parágrafo** com a **descrição da receita.**
- No final da receita deve ter um **rodapé** com seus créditos.

## Importando o arquivo styles.css

Agora você deve criar o arquivo **styles.css** que é onde vamos adicionar todo o CSS da página. Depois de criado, você deve importar o arquivo no HTML usando a tag `<link>` dentro da tag `<head>`.

```html
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="styles.css" /> 
  </head>

```

## Fazendo o reset do CSS

Por padrão o navegador pode adicionar alguns estilos, então para fazer o reset desses estilos podemos adicionar o código abaixo:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
 }
```

<aside>
❓ Se você ficou com dúvida sobre o trecho de código acima, no curso do Discover "Uma caixa dentro da outra" tem várias dicas que podem te ajudar.

[](https://app.rocketseat.com.br/node/uma-caixa-dentro-da-outra)

</aside>

## Cores e tipografia

### Cores:

As cores usada no exemplo são as seguintes:

- Background da página: `#EAEAEA`;
- Background da receita: `#FFFFFF`;
- Títulos e subtítulos: `#1B1B1B`;
- Footer e legenda da imagem: `#8F8F8F`;
- Outros textos: `#39393A`;

<aside>
❓ Para ver mais sobre como trabalhar com cores no CSS:

[](https://app.rocketseat.com.br/node/agora-sim-cores)

</aside>

### Tipografia:

A font usada foi a **Roboto** que pode ser encontrada no site do [Google Fonts](https://fonts.google.com/).

Para usar essa font adicione o código abaixo dentro da tag `<head>` do HTML.

Para esse desafio estamos usando um **font-weight** de 400 para os textos e 700 para os título e subtítulos.

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
   href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
   rel="stylesheet"
/>
```

No CSS basta adicionar a propriedade `font-family: 'Roboto', sans-serif;` ao body, assim a font será aplicada para todos os elementos da página.

```css
body {
  background: #eaeaea;
  font-family: 'Roboto', sans-serif;
}
```

Você pode usar os tamanhos de font abaixo como referência:

- Título: `28px`;
- Subtítulos: `20px`;
- Listas e parágrafo(s): `16px`;
- Footer e legenda da imagem: `12px`;

<aside>
💡 Para usar a unidade de medida `rem` no lugar de `px`, basta dividir o valor em px por 16.
**Exemplo:** 28 / 16 = 1.75rem

16 é o tamanho de fonte padrão usado pela maioria dos navegadores. Se modificar o tamanho da font pelo elemento root ou html você deve dividir pelo valor alterado.
Lembrando também que deve ser usado **ponto** e não vírgula. 

[](https://app.rocketseat.com.br/node/nem-tudo-sao-pixels/lesson/distancias-absolutas-e-relativas)

</aside>

<aside>
❓ Para ver mais sobre como trabalhar com textos nos CSS:

[](https://app.rocketseat.com.br/node/app-bonito-ate-nos-textos)

</aside>

## Adicionando outros estilos a lista de ingredientes e modo de preparo

No exemplo acima foi usado a propriedade `line-height` nas listas de ingredientes e modo de preparo. O valor usado foi de 26px.

<aside>
❓ Nessa aula você pode ver mais sobre a propriedade `line-height`:

[](https://app.rocketseat.com.br/node/app-bonito-ate-nos-textos/group/mais-estilos-para-os-textos/lesson/line-height-e-text-transform)

</aside>

<aside>
💡 Para mudar o posicionamento dos boolets das listas, você pode usar a propriedade `list-style-position`.
Os valores aceitos são: inside | outside
Documentação: [https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position)

</aside>

## Como alinhar elementos ao centro da página?

Existem diversas opções para alinhar elementos ao centro da página, algumas formas simples que podemos usar em alguns casos como o desse desafio, são:

- Para **alinhar textos** e muitas vezes alguns outros elementos podemos usar  a propriedade `text-align: center;` , essa propriedade também aceita os valores start | end | left | right | center | justify | match-parent, então já fica aí a dica de como alinhar a legenda da imagem a direita (right). 😉
    
    <aside>
    ❓ Nessa aula você pode ver mais sobre a propriedade `text-align`:
    
    [](https://app.rocketseat.com.br/node/app-bonito-ate-nos-textos/group/mais-estilos-para-os-textos/lesson/text-align)
    
    </aside>
    
- Para alinhar outros tipos de elementos você pode tentar usar a propriedade `margin: 0 auto;`, por exemplo. Você pode adicionar qualquer valor de top e bottom, o importante é deixar como `auto`os valores de left e right. Também é importante lembrar que o width do elemento deve ser menor do que o da página para que seja possível visualizar o alinhamento ao centro.
    - Exemplo:
        
        ```css
        .recipe-container {
          background: white;
          width: 70%;
          margin: 40px auto;
          padding: 30px;
          border-radius: 10px;
        }
        ```
        
    
    Em alguns outro desafios iremos ver outras formas de alinhar elementos como CSS Flexbox e CSS Grid, por exemplo.
    

## Estilizando a imagem

A imagem do layout acima tem uma largura(width) de 100% e altura(height) de 250px. Você pode usar essas medida para ajustar o tamanho da imagem.

<aside>
💡 Caso a imagem fique distorcida, você pode usar a propriedade `object-fit` e testar/escolher o valor(value) que melhor ajusta a imagem.
Os valores aceitos são: fill | contain | cover | none | scale-down
Documentação: [https://developer.mozilla.org/pt-BR/docs/Web/CSS/object-fit](https://developer.mozilla.org/pt-BR/docs/Web/CSS/object-fit)

</aside>

Para deixar as bordas arredondadas basta adicionar a propriedade `border-radius`, no layout do desafio todos os border-radius desse desafio são de 10px. Lembrando que você pode usar [essa dica](https://www.notion.so/2-Adicionando-os-estilos-com-CSS-f0797e51911e453eabdc99634a0356a0) para converter px para rem, se preferir.

- Exemplo:
    
    HTML
    
    ```html
    <figure class="recipe-image">
        <img
           src="https://images.unsplash.com/photo-1562376552-0d160a2f238d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=925&q=80"
           alt="Foto Waffle"
         />
         <figcaption>Receita de waffle clássico</figcaption>
    </figure>
    ```
    
    CSS
    
    ```css
    .recipe-image {
      text-align: right;
      font-size: 12px;
      color: #8f8f8f;
    }
    
    .recipe-image img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 5px;
    }
    ```
    

## E quanto aos espaçamentos?

Nesse primeiro momento você pode analisar a imagem e adicionar valores de margin e ou padding aproximados. Isso vai te treinar a analisar o layout e definir qual elemento fica melhor para adicionar essas propriedades. Não precisa se preocupar com valores exatos por enquanto. Em próximos desafios você vai poder praticar outras formas de analisar o layout de um projeto.
