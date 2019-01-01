**This repo has been archived. Please refer to the [Roadmap Project Board](https://github.com/vuejs/vue/projects/6) for the latest roadmap.**

# Vue Project Roadmap

> This document outlines work that is currently being worked on and things we plan to work on next. The general answer to "when will X be done?" is "when it's ready," as we believe at this particular stage in Vue's lifecycle, it's more important to ensure shipping stable and solid code rather than rushing out new features. That said, we do value feedback from the community to help us better understand user needs and adjust priorities.

## Core

### 2.6

* [GitHub Project](https://github.com/vuejs/vue/projects/4)
* Various improvements regarding error handling, functional components, SSR

### 2.x-next

* Will be targeting evergreen browsers only in order to leverage native ES2015 features
* Reactivity system will be rewritten with Proxies with various improvements
* No major breaking changes; will be maintained in parallel to 2.x with feature parity

*Note: this means there will be two releases for each new minor version of Vue: 2.x which supports IE and 2.x-next which does not. This also means we are not dropping IE support.*

### 3.x

- [Announcement blog post](https://medium.com/the-vue-point/plans-for-the-next-iteration-of-vue-js-777ffea6fabf)
- [Updates Slides (Nov 2018)](https://docs.google.com/presentation/d/1yhPGyhQrJcpJI2ZFvBme3pGKaGNiLi709c37svivv0o/edit?usp=sharing)
- Will be using TypeScript. For internal implementation only. Does NOT affect ES users, but should improve TS integration for TS users.
- Decouple internals into separate packages (monorepo) each with its own defined API contracts.
  - Individual packages are smaller in scope and more friendly for contributions
  - Opens up custom renderer API for rendering to non-web targets, e.g. NativeScript, Weex, WeChat.
  - Possibility to swap the observer / scheduler with different underlying implementations. E.g. ES5 observer for IE11 compatibility, alternative scheduler to leverage `requestIdleCallback` for time-slicing.
- High level API remains as close to 2.x as possible. Breaking changes only made where necessary, and will be communicated through the RFC process.

### Vuex 4.x

- Simplify usage
  - Getting rid of `mapXXX` helpers via scoped-slot based store consumer component
  - Getting rid of the need for separating actions and mutations
- Better TypeScript inference (may require API redesign)
- Accompanying DevTools update

- **Actionable: kickoff public design thread**

### Backlog

* Built-in class-based API when class properties and decorators reach stage 4
* Leveraging Web Assembly when it gains better DOM access capabilities

## Governance

### RFC process

We plan to drop feature requests from core repo's (`vuejs/vue`)'s issue list soon. New proposals for landing features into core must go through a standard RFC process which helps the contributor to better outline the considerations and tradeoffs involved in adding a new feature.

After 2.6, all non-trivial additions or changes to the core API will go through the RFC process as well, even if it comes from core team members.

- **Actionable: setup RFC repo and guidelines**

## Release Management

### Release Schedule

In the past we've been trying to group-up new features to be released together in a new minor release so that each minor feels more "feature-packed". But over time we've found that such a release schedule is less predictable and can often delay features that are ready from being landed in a timely fashion.

After 2.6 we will switch to a time-based release schedule for minor releases. The new release scheme

- **Major**: will be announced at least 6 months before release. All breaking changes will be communicated before through the RFC process. Accompanying upgrade guide and tooling will be shipped along with the release.

- **Minor**: every 3 months, as long as there are new features.

- **Patch**: as often as necessary.

- **Actionable: release schedule visualization page on vuejs.org**

### Release channels and LTS

- Every major will go through alpha / beta / RC stages as needed.

- Every minor will go through a 3 week beta / 1 week RC process.

- A weekly unstable release (edge) to be automatically cut from latest commit with passing CI build on `dev` branch.

- The current active major will always be active maintained.

- Every time a new major is released, the last minor in the previous major automatically becomes LTS for 18 months, receiving bug fixes and security patches. Then it becomes maintenance mode (security patches only) for another 18 months before entering end of life.

- **Actionable: edge build automatic release system**

### [Regression Testing](https://github.com/vuejs/regression-testing)

We plan to invest time in developing a more robust regression testing system to ensure we don't accidentally break production apps in patch and minor releases. The system will run integration tests on major libraries / frameworks in the ecosystem and other non-trivial codebases to ensure stability.

- **Actionable: regression testing system**

## Tooling

### [vue-cli 3.0](https://github.com/vuejs/vue-cli)

* **Status:** stable
* **Goal:** upgrade `vue-cli` to address project upgrade issues and provide even smoother DX.
* [Docs](https://cli.vuejs.org)

### [vue-test-utils](https://github.com/vuejs/vue-test-utils)

* **Status:** beta
* **Goal:** provide an official library and guide for unit testing Vue components.
* **Lead:** [@eddyerburgh](https://github.com/eddyerburgh)
* [Docs](https://vue-test-utils.vuejs.org/)

### [DevTools 5.0](https://github.com/vuejs/vue-devtools)

- **Status:** beta
- **Goal:** new features like Routing, Performance benchmarks and much more.
- **Lead:** [@Akryum](https://github.com/Akryum)

## Upcoming Events

### Vue.js Amsterdam 2019

* Planned date: Feb 14-15. 2019
* Location: Amsterdam, Netherlands
* [Website](https://www.vuejs.amsterdam)

### VueConf US 2019

* Planned date: Mar 25-27. 2019
* Location: Tampa, Florida, USA
* [Website](http://us.vuejs.org/)

### Vue Fes Japan 2019

* Planned in: Autumn
* Location: Japan

