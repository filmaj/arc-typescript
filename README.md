# arc-typescript

> Example [arc.codes](https://arc.codes) app using typescript

## Overview

This is an [arc](arc.codes) app whose functions are written using TypeScript.
This repo takes massive inspiration from Mike MacCana's excellent
[serverless-starter-kit](https://github.com/mikemaccana/serverless-starter-kit) repo.

This app's makeup is defined in the `app.arc` file. It contains a single HTTP
GET route to the root (`/`). The code for this is located under
`src/http/get-index` - same as in any standard [arc.codes](https://arc.codes) app.

Because we use TypeScript, a build step is necessary (debatable, but for
purposes of this example, let's assume that is true). The tooling and building
is all handled using `npm run` scripts. In short, we configure TypeScript to
compile all `*.ts` files located under `src/` into `.js` files under the `dist/`
directory. Finally, we tell arc to look for code under the `dist/` directory
(see the `app.arc` file's `@http` section for details).

For details on the build scripts, check out the `scripts`
section of the `package.json` file. For details on the TypeScript compilation
options, check out the `tsconfig.json`.

## Quickstart

Clone this repo, then:

    cd arc-typescript
    npm install
    npm start

Then, local up http://localhost:3333.
