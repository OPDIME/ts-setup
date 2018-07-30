# TS-Setup

---

This repository should be used as a simple,
pre-configured workflow to get started with
TypeScript development for Node.JS.

### Getting started

Getting started with this setup only requires two steps.
1. Clone the repository `git clone https://github.com/opdime/ts-setup`
2. Adjust `package.json` (package name, version, description, keywords, author, license, URLs)
3. Install the packages `npm -i`

### NPM Scripts

*  `npm test` Starts Jest.
*  `npm run test-watch` Starts Jest in watch mode.
*  `npm build` Runs the TypeScript compiler for the project.
*  `npm run build-watch` Runs the TypeScript compiler for the project in watch mode.
*  `npm start` Starts Nodemon for the __compiled__ code.

The `prepublish` script is defined, to run the `build` command before publishing,
so the most up-to-date code get published.

### Structure

Code written in this setup should be contained inside the `src/` folder.
As soon as you start building that code, it compiled code will be stored
in the `dist/` folder.

### Nodemon

Nodemon is configured to watch for changes inside the `dist/` folder.
So, at the moment, the nodemon and compiler instance have to be run separately.

### Compiling

This setup offers a TypeScript configuration which
is applicable for most use cases. The compilation target,
by default, is ES5.

### Linting

This setup also contains a `tslint.json`. The default configuration
is meant to be very strict and verbose. For example, the linter is
configured to forbid the annotation `string[]` and encourages the usage
of `Array<string>`. As stated before, this linter config is meant to
encourage verbose, explicit, and precise code. This should reduce
issues, caused by too compact code.