[![tsbb](https://user-images.githubusercontent.com/1680273/57388344-9229a700-71ea-11e9-8495-1d299aed7888.png)](https://github.com/jaywcjlove/tsbb)

<p align="center">
  <a href="https://github.com/jaywcjlove/tsbb/issues">
    <img src="https://img.shields.io/github/issues/jaywcjlove/tsbb.svg">
  </a>
  <a href="https://github.com/jaywcjlove/tsbb/network">
    <img src="https://img.shields.io/github/forks/jaywcjlove/tsbb.svg">
  </a>
  <a href="https://github.com/jaywcjlove/tsbb/stargazers">
    <img src="https://img.shields.io/github/stars/jaywcjlove/tsbb.svg">
  </a>
  <a href="https://github.com/jaywcjlove/tsbb/releases">
    <img src="https://img.shields.io/github/release/jaywcjlove/tsbb.svg">
  </a>
  <a href="https://www.npmjs.com/package/tsbb">
    <img src="https://img.shields.io/npm/v/tsbb.svg">
  </a>
</p>

TSBB is a zero-config CLI that helps you develop, test, and publish modern TypeScript [Node.js](https://nodejs.org/en/) project.

`TypeScript + Babel` = `TSBB`

## Quick Start

You will need `Node.js` installed on your system.

```bash
$ npx tsbb create my-project
$ cd my-project
$ npm run watch # Listen compile .ts files.
$ npm run build # compile .ts files.
$ npm start
```

or

```bash
$ npm install tsbb -g
```

## Command Help

### `tsbb`

```shell
▶ tsbb --help
Usage: tsbb [options]

Commands:
  tsbb create <project-name> [options]  Create a new project with TSBB
  tsbb build [options]                  Build your project once and exit.
  tsbb watch [options]                  Build your project once and exit.

Options:
  --version  Show version number                                       [boolean]
  --help     Show help                                                 [boolean]

Examples:

  $ tsdd build                Build your project once and exit.
  $ tsdd watch                Rebuilds on any change.
  $ tsdd watch --no-comments  Rebuilds on any change.

Copyright 2019
```

### `tsbb create`

```shell
▶ tsbb create --help
tsbb create <project-name> [options]

Create a new project with TSBB

Options:
  --version    Show version number                                     [boolean]
  --help, -h   Show help.                                              [boolean]
  --force, -f  force create.                          [boolean] [default: false]
  --example    Example from
               https://github.com/jaywcjlove/tsbb/tree/master/example
               example-path.                         [string] [default: "basic"]

Examples:
  $ tsbb create my-app                    Create my project.
  $ tsbb create my-app --example express  Create an Express example project.
```

### `tsbb build`

```shell
▶ tsbb build --help
tsbb build [options]

Build your project once and exit.

Options:
  --version          Show version number                               [boolean]
  --help, -h         Show help.                                        [boolean]
  --source-root, -s  The root from which all sources are relative.
                                                       [string] [default: "src"]
  --copy-files       When compiling a directory copy over non-compilable files.
                                                       [boolean] [default: true]
  --source-maps      Source Map options.
              [string] [choices: true, "inline", "both", "none"] [default: true]
  --output, -o       Output directory.                 [string] [default: "lib"]
  --comments         decide whether a given comment should be included in the
                     output code.                      [boolean] [default: true]

Examples:
  $ tsbb build                Build your project.
  $ tsbb build --no-comments  Build your project and remove the comments.
```

### `tsbb watch`

```bash
▶ tsbb watch --help
tsbb watch [options]

Build your project once and exit.

Options:
  --version          Show version number                               [boolean]
  --help, -h         Show help.                                        [boolean]
  --source-root, -s  The root from which all sources are relative.
                                                       [string] [default: "src"]
  --copy-files       When compiling a directory copy over non-compilable files.
                                                       [boolean] [default: true]
  --source-maps      Source Map options.
              [string] [choices: true, "inline", "both", "none"] [default: true]
  --output, -o       Output directory.                 [string] [default: "lib"]
  --comments         decide whether a given comment should be included in the
                     output code.                      [boolean] [default: true]
  --timer, -t        Compile interval.                   [number] [default: 300]

Examples:
  $ tsbb watch   Rebuilds on any change.
```

## Example

- [Basic](example/basic) - The [Node.js](https://nodejs.org/en/) base application example.
- [Koa](example/koa) - The [Koa](https://koajs.com/) base application example.
- [Express](example/express) - The [Express](https://expressjs.com/) base application example.

## License

MIT © [Kenny Wong](https://wangchujiang.com)