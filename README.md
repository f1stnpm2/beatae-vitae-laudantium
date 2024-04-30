<h1 align="center">Welcome to @f1stnpm2/beatae-vitae-laudantium 👋</h1>
<p align="center">
  <img src="https://img.shields.io/npm/v/@f1stnpm2/beatae-vitae-laudantium.svg?orange=blue" />
  <a href="https://www.npmjs.com/package/@f1stnpm2/beatae-vitae-laudantium">
    <img alt="downloads" src="https://img.shields.io/npm/dm/@f1stnpm2/beatae-vitae-laudantium.svg?color=blue" target="_blank" />
  </a>
  <a href="https://github.com/syukronarie/@f1stnpm2/beatae-vitae-laudantium/blob/main/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-yellow.svg" target="_blank" />
  </a>
  <a href="https://codecov.io/gh/syukronarie/@f1stnpm2/beatae-vitae-laudantium">
    <img src="https://codecov.io/gh/syukronarie/@f1stnpm2/beatae-vitae-laudantium/branch/main/graph/badge.svg" />
  </a>
  <a href="https://snyk.io/test/npm/@f1stnpm2/beatae-vitae-laudantium">
    <img alt="snyk.io" src="https://snyk.io/test/npm/@f1stnpm2/beatae-vitae-laudantium/badge.svg" target="_blank" /> 
  </a>
</p>

## ✨ What is @f1stnpm2/beatae-vitae-laudantium?

`@f1stnpm2/beatae-vitae-laudantium` is library to convert json raw (`array`) into xlsx file

## ⚡️ Installation

using npm

```zsh
npm install @f1stnpm2/beatae-vitae-laudantium
```

using yarn

```zsh
yarn add @f1stnpm2/beatae-vitae-laudantium
```

using pnpm

```zsh
pnpm add @f1stnpm2/beatae-vitae-laudantium
```

## 🚀 Usage

Use to save as file:

```js
const @f1stnpm2/beatae-vitae-laudantium = require('@f1stnpm2/beatae-vitae-laudantium');
const fs = require('fs');

const json = [
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
];

const buffer = @f1stnpm2/beatae-vitae-laudantium(json);

fs.writeFileSync('example.xlsx', buffer, 'binary');
```

Or use as express middleware. It adds a convenience `xlsx` method to the response object to immediately output an excel as download.

```js
const express = require('express');
const @f1stnpm2/beatae-vitae-laudantium = require('@f1stnpm2/beatae-vitae-laudantium');
const app = express();
const PORT = 3000;

const data = [
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
  {
    name: 'John',
    age: 27,
    job: 'Software Engineer',
  },
];

app.use(@f1stnpm2/beatae-vitae-laudantium.middleware);
app.get('/', function (req, res) {
  res.xlsx('example.xlsx', data);
});

app.listen(PORT, function (err) {
  if (err) console.log(err);
  console.log('Server listening on PORT', PORT);
});
```

## 🤝 Contributing

Anyone can contribute with [issues](https://github.com/syukronarie/@f1stnpm2/beatae-vitae-laudantium/issues) and [PRs](https://github.com/syukronarie/@f1stnpm2/beatae-vitae-laudantium/pulls). If you're submitting a pull request, always create a new branch to work your changes, and try squashing commits down if possible. Always test any new code and make sure `npm test` passes and `npm run test:cover` for code coverage is adequate before opening a PR.

## Author

👤 **Arie Syukron**

- Github: [@syukronarie](https://github.com/syukronarie)

## Show your support

Please ⭐️ this repository if this project helped you!

<a href="https://www.patreon.com/syukronarie">
  <img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## 📝 License

Copyright © 2022 [Arie Syukron](https://github.com/syukronarie).<br />
This project is [MIT](https://github.com/syukronarie/@f1stnpm2/beatae-vitae-laudantium/blob/main/LICENSE) licensed.

happy coding!
