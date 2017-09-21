# Vue Project Roadmap

## Core

### 2.5

- Planned release: early October 2017
- [TypeScript improvements](https://medium.com/the-vue-point/upcoming-typescript-changes-in-vue-2-5-e9bd7e2ecf08)
- Various improvements to be announced on release

### 3.0

- Planned release: early 2018
- Will be targeting evergreen browsers only
- Reactivity system will be rewritten with Proxies with various improvements
- No major breaking changes; will be maintained in parallel to 2.x with feature parity

## Active Initiatives

### vue-test-utils

- **Goal:** provide an official library and guide for unit testing Vue components.
- **Lead:** @eddyerburgh
- [Design thread](https://github.com/vuejs/vue-test-utils/issues/1)

### `vue-cli` 3.0 redesign

- **Goal:** upgrade `vue-cli` to address project upgrade issues and provide even smoother DX.
- **Lead:** @yyx990803, @egoist
- [Design thread](https://github.com/vuejs/vue-cli/issues/589)

### eslint-plugin-vue

- **Goal:** provide an official eslint plugin with capability of linting single file components (including template syntax errors)
- **Lead:** @michalsnik, @mysticatea
- [Discussions](https://github.com/vuejs/eslint-plugin-vue/issues)

### Bundler-agnostic Single-File Component Compiler

- **Goal:** extract single-file component compilation logic from `vue-loader` into a bundle-agnostic package so that it can be reused in all tooling in the ecosystem.
- **Lead:** @znck, @eddyerburgh
- [Design thead](https://github.com/vuejs/vue-component-compiler/issues/28)

### Style Guide

- **Goal:** offer code style recommendations for teams seeking consistency.
- **Lead:** @chrisvfritz
- [WIP branch](https://github.com/vuejs/vuejs.org/tree/style-guide)

### Cookbook

- **Goal:** offer solutions to commonly encountered scenarios
- **Lead:** @chrisvfritz
- Planned to be started November 2017
