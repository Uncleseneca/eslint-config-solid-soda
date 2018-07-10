# eslint-config-solid-soda

This package provides Solid Soda's base JS .eslintrc as an extensible shared config. It's based on Airbnb's [eslint-config-airbnb-base](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb-base) config.

## Usage

We export two ESLint configurations for your usage.

### eslint-config-solid-soda

Our default export contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

If you use yarn, run `npm info "eslint-config-solid-soda@latest" peerDependencies` to list the peer dependencies and versions, then run `yarn add --dev <dependency>@<version>` for each listed peer dependency. See below for npm instructions.

1.  Install the correct versions of each package, which are listed by the command:

```sh
npm info "eslint-config-solid-soda@latest" peerDependencies
```

If using **npm 5+**, use this shortcut

```sh
npx install-peerdeps --dev eslint-config-solid-soda
```

If using **npm < 5**, Linux/OSX users can run

```sh
(
  export PKG=eslint-config-solid-soda;
  npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

Which produces and runs a command like:

```sh
  npm install --save-dev eslint-config-solid-soda eslint@^#.#.# eslint-plugin-import@^#.#.#
```

If using **npm < 5**, Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

```sh
npm install -g install-peerdeps
install-peerdeps --dev eslint-config-solid-soda
```

The cli will produce and run a command like:

```sh
npm install --save-dev eslint-config-solid-soda eslint@^#.#.# eslint-plugin-import@^#.#.#
```

2.  Add `"extends": "solid-soda"` to your .eslintrc.

### eslint-config-solid-soda/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

1.  Install the correct versions of each package, which are listed by the command:

```sh
npm info "eslint-config-solid-soda@latest" peerDependencies
```

Linux/OSX users can run

```sh
(
  export PKG=eslint-config-solid-soda;
  npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
)
```

Which produces and runs a command like:

```sh
npm install --save-dev eslint-config-solid-soda eslint@^3.0.1 eslint-plugin-import@^1.10.3
```

2.  Add `"extends": "solid-soda/legacy"` to your .eslintrc

### eslint-config-solid-soda/whitespace

This entry point only warns on whitespace rules and sets all other rules to warnings.

## Improving this config

Consider adding test cases if you're making complicated rules changes, like anything involving regexes. Perhaps in a distant future, we could use literate programming to structure our README as test cases for our .eslintrc?

You can run tests with `npm test`.

You can make sure this module lints with itself using `npm run lint`.
