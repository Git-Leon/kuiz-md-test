# kuiz.md

:dart: Live demo at [https://kuiz-md.firebaseapp.com](https://kuiz-md.firebaseapp.com)

You can use the kuiz NPM module to generate your own kuiz from Markdown you provide.

```bash
npm install kuiz-md
```

Or, if you use yarn:
```bash
yarn add kuiz-md
```

## Usage

Provide:

- your markdown text
- a callback triggered when an user sends the kuiz
- a HTML element to render the kuiz into

```javascript
const app = require('kuiz-md');

const markdown = '# your *Markdown* text _here_';
const yourCallback = (data) => {
  alert('User ' + data.email + ' had grade ' + data.grade);
};
const elementIdToRenderInto = "my-kuiz"

app.init(markdown, yourCallback, elementIdToRenderInto);
```

## Special notation

There is a special notation for handling the Kuiz possible responses:

**Multiple possible answers**

The user must validate all possible answers, identifed with a "x" inside the parenthesis:
```
random text

( ) answer not valid
(x) answer valid
(x) answer valid
( ) answer not valid
```

Other answer types: WIP

## Development

To launch a local webserver, run
```bash
cd landing
npm install
npm install babel-preset-es2015
npm install --save-dev css-loader style-loader
npm install node-sass@4.14.0
npm start
```

## Deployment

```bash
npm run deploy
```
