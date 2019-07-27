# Photography Day!! (Don't forget to do the check-in)

## Summary OLA MARILENE

##TAINHA E VINHO(?)

#We did the check-in =D!

## Summary

1. Introduction to Frontend
  - HTML Boilerplate, Tags and <!DOCTYPE html>
  - Three Ways to Insert CSS
    - Inline Styles
    - Internal Style Sheet
    - External Style Sheet
  - Vanilla JavaScript
2. Revisiting GraphQL Clients
3. Extra

## Introduction to Frontend

- HTML [Boilerplate](https://en.wikipedia.org/wiki/Boilerplate_code), [Tags](https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element) and [<!DOCTYPE html>](http://gabsferreira.com/pra-que-serve-a-tag-doctype-em-arquivos-html/)

**index.html**
```
<!DOCTYPE html> <!-- This is an HTML comment, try CTRL + / on your text editor -->
<html>
  <head>
    <title>Simple Webpage</title>
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
    <span>Let's learn about <a href="https://pipefy.com/lean">Lean</a></span>
    <input type="text" />
    <div>
      <div>
        <div>
          <div>
            Divs everywhere
          </div>
        </div>
      <div>
    <div>
  </body>
</html>
```

- Three Ways to Insert [CSS](https://developer.mozilla.org/pt-BR/docs/Web/CSS)

> Inline Styles

**index.html**
```
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Webpage</title>
  </head>
  
  <body>
    <p>I play Pokémon <span style="color: red;">Red</span>.
  </body>
</html>
```

> Internal Style Sheet

**index.html**
```
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Webpage</title>
    <style>
      body {
        font-family: "Comic Sans MS";
        background-color: #BBB;
      }
    </style>
  </head>
  
  <body>
    <h1>This is a very well designed web page</h1>
  </body>
</html>
```

> External Style Sheet

**styles.css**
```
.shiny {
  background-color: yellow;
}

.dark {
  background-color: #555;
}

.sm-square {
  height: 50px;
  width: 50px;
}

.lg-square {
  height: 150px;
  width: 150px;
}
```

**index.html**

```
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Webpage</title>
    <link> rel="stylesheet" href="./styles.css" /> 
  </head>
  
  <body>
    <div class="shiny sm-square"></div>
    <br />
    <div class="lg-square dark"></div>
  </body>
</html>
```

- [Vanilla JavaScript](http://vanilla-js.com)

**index.html**

```
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Webpage</title>
    <script>
      console.log('script started');

      function switchBackgroundColor() {
        var background = document.querySelector('body');

        if (background.style.backgroundColor == 'white') {
          background.style.backgroundColor = 'black';
        } else {
          background.style.backgroundColor = 'white';
        }
      }

      function load() {
        console.log('DOM loaded');

        var myButton = document.querySelector('button');
        myButton.addEventListener('click', switchBackgroundColor, false);
      }

      document.addEventListener('DOMContentLoaded', load, false);
    </script>
  </head>
  
  <body>
    <button>Click Me!</button>
  </body>
</html>
```

## Revisiting GraphQL Clients

**index.html?**
```
fetch('/graphql', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Accept': 'application/json',
  },
  body: JSON.stringify({query: "{ hello }"})
})
  .then(r => r.json())
  .then(data => console.log('data returned:', data));
```

## Extra

`$ npm install -g create-react-app`
`$ create-react-app todos`
