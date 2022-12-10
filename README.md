# Vite TypeScript NPM Package

Scaffold TypeScript npm packages using this template to bootstrap your next library.

Versions of this template:
- [Vite TypeScript library npm package](https://github.com/jasonsturges/vite-typescript-npm-package)
- [Vite JavaScript library npm package](https://github.com/jasonsturges/vite-npm-package)
- [Rollup JavaScript library npm package](https://github.com/jasonsturges/npm-package-boilerplate)
- [Rollup TypeScript library npm package](https://github.com/jasonsturges/typescript-npm-package)


## Getting Started

Begin via any of the following:

- Press the "*Use this template*" button

- Use [degit](https://github.com/Rich-Harris/degit) to execute: 

    ```
    degit github:jasonsturges/vite-typescript-npm-package
    ```
    
- Use [GitHub CLI](https://cli.github.com/) to execute: 

    ```
    gh repo create <name> --template="https://github.com/jasonsturges/vite-typescript-npm-package"
    ```
    
- Simply `git clone`, delete the existing .git folder, and then:

    ```
    git init
    git add -A
    git commit -m "Initial commit"
    ````

Remember to use `npm search <term>` to avoid naming conflicts in the NPM Registery for your new package name.


## Usage

The following tasks are available for `npm run`:

- `start`: Run Vite in host mode for a local development environment (not included in production build)
- `watch`: Run Vite in watch mode to detect changes to files during development
- `build`: Run Vite to build a production release distributable


## Development

Vite features a host mode to enables development with real time HMR updates directly from the library via the `start` script.

To test your library from within an app:

- **From your library**: run `npm link` or `yarn link` command to register the package
- **From your app**: run `npm link "mylib"` or `yarn link "mylib"` command to use the library inside your app during development


## Development Cleanup

Once development completes, `unlink` both your library and test app projects.

- **From your app**: run `npm link "mylib"` or `yarn link "mylib"` command to use the library inside your app during development
- **From your library**: run `npm unlink` or `yarn unlink` command to register the package


## Release Publishing

Update your `package.json` to next version number, and remember to tag a release.

Once ready to submit your package to the NPM Registry, execute the following tasks via `npm` (or `yarn`):

- `npm run clean` &mdash; Assure a clean build
- `npm run build` &mdash; Build the package
- `npm run build:types` &mdash; Build API Extractor d.ts declaration

Assure the proper npm login:

```
npm login
```

Submit your package to the registry:

```
npm publish --access public
```
