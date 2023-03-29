---
sidebar_position: 7
---

### Líneas de comando

Estos comando se usan para facilitarnos como queremos correr los test de una forma mas sencilla desde la consola.

-  ** --e2e ** sirve para indicar que se va a ejecutar testing end to end
- ** -b ** nos permite ingresar el browser que vamos a utilizar
- ** --spec ** nos permite indicar directamente el test

En el package.json podemos poner los scripts que querramos guardar

```jsx= "Script para correr en chromium"
"scripts":{
    "test": "npx cypress open --e2e -b chromium"
},
```

Para correr el script que definas hay que colocar en consola (dentro de donde tengas el cypress)
```jsx
npm run nombre%de%tu%script
```

Mas info:[https://docs.cypress.io/guides/guides/command-line]


### Cypress config

En ** cypress.config.js ** se puede agregar:

- defaultCommandTimeout: 10000,
- watchForFileChanges: Sirve si queremos que al guardar los test se ejecuten inmediatamente.En false no se van a  ejecutar los test al guardar. 
- viewportHeigth: para configurar tamaño de pantalla. 
- viewporWith: para configurar tamaño de pantalla. 
- baseUrl : se configura la pagina base que se esta testeando. 

```jsx title="cypress.config.js"
module.exports = defineConfig({
  e2e: {
    setupNodeEvents(on, config) {
      // implement node event listeners here
    },
    defaultCommandTimeout: 10000, //10seg
    watchForFileChanges: false,
    'baseUrl': 'https://some-url'
  },
});
```

Mas info:[https://docs.cypress.io/guides/references/configuration]
