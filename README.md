# Nestjs project name

Nestjs project Description.

## Requirements

Before starting, make sure you have at least those components on your workstation:

| Name                          | Version |
|:------------------------------|:--------|
| [NodeJS](https://nodejs.org/) | 19+     |
| MySQL                         | ANY     |

---

## Configuration

1. Create a `.env` file
    - Copy [.env.sample](.env.sample) file to `.env`.
   ```shell
   cp .env.example .env
   ```
    - Edit [.env](.env) file.
   ```shell
   nano .env
   ```
2. Edit env config
    - Edit the file in the [config](src/config) folder.
    - `default`, `development`, `production`, `test`

---

## Installation

```shell
npm ci
```

When synchronize database from existing entities:

```shell
npm run entity:sync
```

When import entities from an existing database:

```shell
npm run entity:load
```

If you use multiple databases in `entity:load`, [modify them.](bin/entity.ts#L45)

---

### Development

```shell
npm run start:dev
# https://docs.nestjs.com/recipes/repl
npm run start:repl
```

Run [http://localhost:3000](http://localhost:3000)

---

### Test

```shell
npm test # exclude e2e
npm run test:e2e
```

---

### Production

1. Build:
   ```shell
   npm run lint
   npm run build
   ```
2. Run:
   ```shell
   # Define environment variable yourself.
   # NODE_ENV=production PORT=8000 NO_COLOR=true node dist/app
   node dist/app
   # OR
   npm start
   ```

---

## Copyright and license
Licensed under the **MIT License** [LICENSE](LICENSE) license.

Copyright © 2023 [Dafa](https://github.com/Dafa-Co) <a href="https://www.dafa.sa/" target="blank">
<img src="https://static.wixstatic.com/media/8b2439_37f48f90ad054b39b4ae46a70af9bebb~mv2.png/v1/fill/w_115,h_69,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Dafe-logo-01.png" width="48" alt="Dafa Logo" border="0" />
</a>

<!-- Remove the lines bellow before go live -->

---

##### For developers:
###### - Project structure documentation: [STRUCTURE.md](STRUCTURE.md).
###### - Naming cheatsheet: [NAMING.md](NAMING.md).
###### - JS Clean code: [ryanmcdermott/clean-code-javascript#readme](https://github.com/ryanmcdermott/clean-code-javascript#readme).
