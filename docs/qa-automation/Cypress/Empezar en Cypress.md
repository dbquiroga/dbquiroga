---
sidebar_position: 2
---

## Qué es
Cypress es una herramienta Javascript de end-to-end testing que permite hacer testing en aplicaciones web como así también microservicios.
Podemos testear aplicaciones web, bases de datos SQL o mongoDB, testear postgress, etc, etc. 

:::note
** No ** permite testear aplicaciones nativas de Android u Ios.
:::

## Características
- Web testing
- Api Testing
- Múltiples browsers
- Ejecución oculta
- Interfaz propia
- Amigable
- Esperas automáticas (por default espera 4 segundos, se puede modificar)
- Open source

## Interacciones en el DOM

- ** click() **: es la acción de clickear en un elemento web
- ** type() **: es la acción de escribir texto en un input
- ** clear() **: elimina texto de un input
- ** check/uncheck() **: funciona con inputs tipo checkbox o radio button y permite seleccionar sus opciones
- ** select() **: permite seleccionar valores en una lista desplegable

## Metodos de Cypress
- ** visit('https://tu-url.com') **: Para ingresar a una pagina
- ** get('#user')** : Para obtener un elemento

:::note
Para que no se visualice la contraseña en la ejecucion, en los logs, se coloca lo siguiente:
```js
cy.get('#pass').type('123456!, {log:false})
```
:::

# Colocar referencia a cypress
Se coloca para que nos de info rapida de cypress. Es una ayuda para usar metodos y no sabemos como se utiliza, nos dice los parametros, ejemplos y referencia a la documentacion. 

```js
<reference types="cypress"/>
```

:::note
Todo dato sensible como contraseñas, lo ideal es que se escriban en ** variables de entorno ** y saacrlo del test en si.
:::

# Errores comunes en cypress
Cuando tenemos un elemento delante del que queremos interactuar cypress nos indicara un error, para solucionar este problema cypress en si ya sugiere que uses el comando ** force **. 

```js title="Ejemplo uso force"
cy.get("[value='Male']".check({force:true}));
```