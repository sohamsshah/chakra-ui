# Change Log

## 1.2.3

### Patch Changes

- [#5234](https://github.com/chakra-ui/chakra-ui/pull/5234)
  [`bc2613a9a`](https://github.com/chakra-ui/chakra-ui/commit/bc2613a9ab8273c844ed071947164f0a82ad9ea4)
  Thanks [@nxtman123](https://github.com/nxtman123)! - `useBreakpointValue`
  returns the correct value on first tick, if `matchMedia` is available

## 1.2.2

### Patch Changes

- [#5135](https://github.com/chakra-ui/chakra-ui/pull/5135)
  [`53e2df4f9`](https://github.com/chakra-ui/chakra-ui/commit/53e2df4f9cbe7fc2fad69d1ee49a1e788811467a)
  Thanks [@primos63](https://github.com/primos63)! - Improved performance and
  behavior of `useMediaQuery` hook.

## 1.2.1

### Patch Changes

- [#5074](https://github.com/chakra-ui/chakra-ui/pull/5074)
  [`042994eb0`](https://github.com/chakra-ui/chakra-ui/commit/042994eb0866e4f49cc286f64f54962f613a4423)
  Thanks [@cschroeter](https://github.com/cschroeter)! - Fix issue where
  `useColorModePreference` returned incorrect values due to array destructuring.

* [#5075](https://github.com/chakra-ui/chakra-ui/pull/5075)
  [`b28142946`](https://github.com/chakra-ui/chakra-ui/commit/b281429462a099b7fd7f9352e837cd28d1a2da0e)
  Thanks [@cschroeter](https://github.com/cschroeter)! - Update babel config to
  transpile soruces for older browsers. This fixes issues with CRA and
  Storybook.
* Updated dependencies
  [[`b28142946`](https://github.com/chakra-ui/chakra-ui/commit/b281429462a099b7fd7f9352e837cd28d1a2da0e)]:
  - @chakra-ui/react-env@1.1.1
  - @chakra-ui/utils@1.9.1

## 1.2.0

### Minor Changes

- [#4991](https://github.com/chakra-ui/chakra-ui/pull/4991)
  [`6095eaf9a`](https://github.com/chakra-ui/chakra-ui/commit/6095eaf9ac64a7e4d9f934bcb530bae2a92111a6)
  Thanks [@segunadebayo](https://github.com/segunadebayo)! - Update build system
  we use from a custom babel cli setup to
  [preconstruct](https://preconstruct.tools/).

  The previous build system transpiles the code in `src` directory to `dist/esm`
  and `dist/cjs` keeping the same file structure. The new build system merges
  all files in `src` and transpiles to a single `esm` and `cjs` file.

  **Potential Breaking Change:** The side effect of this is that, if you
  imported any function, component or hook using the **undocumented** approach
  like
  `import { useOutsideClick } from "@chakra-ui/hooks/dist/use-outside-click"`,
  you'll notice that the this doesn't work anymore.

  Here's how to resolve it:

  ```jsx live=false
  // Won't work 🎇
  import { useOutsideClick } from "@chakra-ui/hooks/dist/use-outside-click"

  // Works ✅
  import { useOutsideClick } from "@chakra-ui/hooks"
  ```

  If this affected your project, we recommend that you import hooks, functions
  or components the way it's shown in the documentation. This will help keep
  your project future-proof.

### Patch Changes

- Updated dependencies
  [[`6095eaf9a`](https://github.com/chakra-ui/chakra-ui/commit/6095eaf9ac64a7e4d9f934bcb530bae2a92111a6)]:
  - @chakra-ui/react-env@1.1.0
  - @chakra-ui/utils@1.9.0

## 1.1.5

### Patch Changes

- [`97bad87c7`](https://github.com/chakra-ui/chakra-ui/commit/97bad87c7b8b4ff31f705a9d55b392385d921a33)
  [#4807](https://github.com/chakra-ui/chakra-ui/pull/4807) Thanks
  [@primos63](https://github.com/primos63)! - Corrected eslint errors.

* [`f2df9cfc1`](https://github.com/chakra-ui/chakra-ui/commit/f2df9cfc1c3c2ef3f3b74ec2849079fd726cd84c)
  [#4807](https://github.com/chakra-ui/chakra-ui/pull/4807) Thanks
  [@primos63](https://github.com/primos63)! - Fix an issue where the
  `useMediaQuery` was not updating the array of booleans correctly when resizing
  the viewport.

  It also removes deprecated calls `addListener` and `removeListener` in favor
  of the recommended `addEventListener` and `removeEventListener` calls.

## 1.1.4

### Patch Changes

- Updated dependencies
  [[`cd0893c56`](https://github.com/chakra-ui/chakra-ui/commit/cd0893c561d8c72b69db7c03d10adae752468a4f)]:
  - @chakra-ui/utils@1.8.4
  - @chakra-ui/react-env@1.0.8

## 1.1.3

### Patch Changes

- Updated dependencies
  [[`c06d242c6`](https://github.com/chakra-ui/chakra-ui/commit/c06d242c672a10f93fab4dc2321143beae2db669),
  [`5b4d8ef24`](https://github.com/chakra-ui/chakra-ui/commit/5b4d8ef24017dab1d69aeb5016b53366bdb3bcfd)]:
  - @chakra-ui/utils@1.8.3
  - @chakra-ui/react-env@1.0.7

## 1.1.2

### Patch Changes

- Updated dependencies
  [[`4c1071969`](https://github.com/chakra-ui/chakra-ui/commit/4c1071969a9b41a952b374f9990ac0bb89d24fa0),
  [`43f66097b`](https://github.com/chakra-ui/chakra-ui/commit/43f66097b39f1c37a4627dd6ca8a85555f35b95c)]:
  - @chakra-ui/utils@1.8.2
  - @chakra-ui/react-env@1.0.6

## 1.1.1

### Patch Changes

- Updated dependencies
  [[`4a1e4d93b`](https://github.com/chakra-ui/chakra-ui/commit/4a1e4d93b0a07df7266d40bb66039385b158d3d1)]:
  - @chakra-ui/utils@1.8.1
  - @chakra-ui/react-env@1.0.5

## 1.1.0

### Minor Changes

- [`31ec6466c`](https://github.com/chakra-ui/chakra-ui/commit/31ec6466c2ddc7fffb8e8dfa0f7f241f189f96eb)
  [#4029](https://github.com/chakra-ui/chakra-ui/pull/4029) Thanks
  [@jesstelford](https://github.com/jesstelford)! - `useBreakpointValue()` now
  supports receiving a `defaultBreakpoint` as the second argument to support
  SSR/SSG.

## 1.0.14

### Patch Changes

- [`760607680`](https://github.com/chakra-ui/chakra-ui/commit/76060768093b056a8d645b981da12f147bb7cf0f)
  [#4038](https://github.com/chakra-ui/chakra-ui/pull/4038) Thanks
  [@cschroeter](https://github.com/cschroeter)! - fix(media-query): fix an issue
  with useBreakpointValue

## 1.0.13

### Patch Changes

- Updated dependencies
  [[`d0f50a46e`](https://github.com/chakra-ui/chakra-ui/commit/d0f50a46ea6c2bcf06d8cad8b9b3994fd934be01),
  [`b479ff22e`](https://github.com/chakra-ui/chakra-ui/commit/b479ff22ea10c1a1393224c37c36aa6ceabc4aab),
  [`07d15eab4`](https://github.com/chakra-ui/chakra-ui/commit/07d15eab480724f8fee1a09b7cecdf1e968d9ddd)]:
  - @chakra-ui/utils@1.8.0

## 1.0.12

### Patch Changes

- Updated dependencies
  [[`e9ac4cc76`](https://github.com/chakra-ui/chakra-ui/commit/e9ac4cc7629cd79efc753b4e3353bacdad46cd7d)]:
  - @chakra-ui/utils@1.7.0

## 1.0.11

### Patch Changes

- Updated dependencies
  [[`0974e547c`](https://github.com/chakra-ui/chakra-ui/commit/0974e547c29e4efc1ba4d1eb1507d0dad7d7a77a),
  [`59ea894a7`](https://github.com/chakra-ui/chakra-ui/commit/59ea894a7e03d16cd7a1b89d00816eafa9fab65d)]:
  - @chakra-ui/utils@1.6.0

## 1.0.10

### Patch Changes

- Updated dependencies
  [[`8b5eb9654`](https://github.com/chakra-ui/chakra-ui/commit/8b5eb9654affe562795d38a19f732f84732a949d)]:
  - @chakra-ui/utils@1.5.2

## 1.0.9

### Patch Changes

- Updated dependencies
  [[`1a04a41bd`](https://github.com/chakra-ui/chakra-ui/commit/1a04a41bd2285069011a738fff422ba1a6fcce94),
  [`e481ba491`](https://github.com/chakra-ui/chakra-ui/commit/e481ba4914a7f163d93d4c22e2e457f1afb08721)]:
  - @chakra-ui/utils@1.5.1

## 1.0.8

### Patch Changes

- Updated dependencies
  [[`a58b724e9`](https://github.com/chakra-ui/chakra-ui/commit/a58b724e9c8656044f866b658f378662f2a44b46),
  [`b724a9dd9`](https://github.com/chakra-ui/chakra-ui/commit/b724a9dd9429d02c0b2c7f7deac66d3553100bdc)]:
  - @chakra-ui/utils@1.5.0

## 1.0.7

### Patch Changes

- Updated dependencies
  [[`e748219f3`](https://github.com/chakra-ui/chakra-ui/commit/e748219f300f0c51b0eb304fce38b014d7bcbc86),
  [`91ef14839`](https://github.com/chakra-ui/chakra-ui/commit/91ef148397187010804eb8f30307d2ec94c32c5b)]:
  - @chakra-ui/utils@1.4.0

## 1.0.6

### Patch Changes

- Updated dependencies
  [[`87cc23e14`](https://github.com/chakra-ui/chakra-ui/commit/87cc23e14814e02cbbfc9737c2356cef682ddd5d)]:
  - @chakra-ui/utils@1.3.0

## 1.0.5

### Patch Changes

- Updated dependencies
  [[`ff4a36bca`](https://github.com/chakra-ui/chakra-ui/commit/ff4a36bca11cc177830f6f1da13700acd1e3a087),
  [`483687237`](https://github.com/chakra-ui/chakra-ui/commit/483687237f2c4fed05dc6a79693f307c601c1285),
  [`61962345c`](https://github.com/chakra-ui/chakra-ui/commit/61962345c5b1c862445c16c586e304b28c376c9a)]:
  - @chakra-ui/utils@1.2.0

## 1.0.4

### Patch Changes

- Updated dependencies
  [[`8b87406c`](https://github.com/chakra-ui/chakra-ui/commit/8b87406c3132586be3393117eef80d47ec82fc54)]:
  - @chakra-ui/utils@1.1.0

## 1.0.3

### Patch Changes

- [`1286da79`](https://github.com/chakra-ui/chakra-ui/commit/1286da7977db7bd8f19e2abd03b73990737b1379)
  [#2992](https://github.com/chakra-ui/chakra-ui/pull/2992) Thanks
  [@ljosberinn](https://github.com/ljosberinn)! - fix(media-query): fixes
  useBreakpoinValue infinite loop due to bug in createMediaQueries

## 1.0.2

### Patch Changes

- Updated dependencies
  [[`e73878ee`](https://github.com/chakra-ui/chakra-ui/commit/e73878ee686c11d3f94ad6ac61b19ae9508d75a5)]:
  - @chakra-ui/utils@1.0.2

## 1.0.1

### Patch Changes

- [`a1ff404b`](https://github.com/chakra-ui/chakra-ui/commit/a1ff404b12a898ab97af024391a06c34da5bc69a)
  [#2540](https://github.com/chakra-ui/chakra-ui/pull/2540) Thanks
  [@stellarhoof](https://github.com/stellarhoof)! - Fix match media on
  useBreakpoint when no default value is provided

- Updated dependencies
  [[`5c482483`](https://github.com/chakra-ui/chakra-ui/commit/5c482483ce24fc798540c9792a15e06772eae213)]:
  - @chakra-ui/utils@1.0.1

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0 (2020-11-13)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-rc.8 (2020-10-29)

### Bug Fixes

- **toast:** allow custom render in update
  ([eb8bff9](https://github.com/chakra-ui/chakra-ui/commit/eb8bff911e6ec9de0165ab1e8f5ca10d5e022459)),
  closes [#2362](https://github.com/chakra-ui/chakra-ui/issues/2362)

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-rc.7 (2020-10-25)

**Note:** Version bump only for package @chakra-ui/media-query

# 1.0.0-rc.6 (2020-10-25)

**Note:** Version bump only for package @chakra-ui/media-query

# 1.0.0-rc.5 (2020-09-27)

**Note:** Version bump only for package @chakra-ui/media-query

# 1.0.0-rc.4 (2020-09-25)

**Note:** Version bump only for package @chakra-ui/media-query

# 1.0.0-rc.3 (2020-08-30)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-rc.2 (2020-08-09)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [1.0.0-rc.1](https://github.com/chakra-ui/chakra-ui/compare/@chakra-ui/media-query@1.0.0-rc.0...@chakra-ui/media-query@1.0.0-rc.1) (2020-08-06)

### Bug Fixes

- **media-query:** create media queries using breakpoint name keys only
  ([1f1413f](https://github.com/chakra-ui/chakra-ui/commit/1f1413f297c08d819e56b5649258c18472f9177a))

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [1.0.0-rc.0](https://github.com/chakra-ui/chakra-ui/compare/@chakra-ui/media-query@1.0.0-next.7...@chakra-ui/media-query@1.0.0-rc.0) (2020-07-26)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [1.0.0-next.7](https://github.com/chakra-ui/chakra-ui/compare/@chakra-ui/media-query@1.0.0-next.6...@chakra-ui/media-query@1.0.0-next.7) (2020-07-26)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [1.0.0-next.6](https://github.com/chakra-ui/chakra-ui/compare/@chakra-ui/media-query@1.0.0-next.5...@chakra-ui/media-query@1.0.0-next.6) (2020-07-15)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# [1.0.0-next.5](https://github.com/chakra-ui/chakra-ui/compare/@chakra-ui/media-query@1.0.0-next.4...@chakra-ui/media-query@1.0.0-next.5) (2020-07-15)

**Note:** Version bump only for package @chakra-ui/media-query

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-next.4 (2020-07-01)

### Bug Fixes

- [#891](https://github.com/chakra-ui/chakra-ui/issues/891)
  ([e107acc](https://github.com/chakra-ui/chakra-ui/commit/e107acc8487898a965b0d695c1da71f46fc56d5e))
- ts issue with sx prop
  ([d3b1340](https://github.com/chakra-ui/chakra-ui/commit/d3b1340cb255937927b4d4c56ce218141570b951))

### Features

- **media-query:** add breakpoint value, animation, and color mode utils
  ([9487655](https://github.com/chakra-ui/chakra-ui/commit/9487655f315656b7bf58fe81e4b6ce90d546caf0))

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-next.3 (2020-06-28)

### Bug Fixes

- [#891](https://github.com/chakra-ui/chakra-ui/issues/891)
  ([e107acc](https://github.com/chakra-ui/chakra-ui/commit/e107acc8487898a965b0d695c1da71f46fc56d5e))
- ts issue with sx prop
  ([d3b1340](https://github.com/chakra-ui/chakra-ui/commit/d3b1340cb255937927b4d4c56ce218141570b951))

# Change Log

All notable changes to this project will be documented in this file. See
[Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 1.0.0-next.2 (2020-06-21)

### Bug Fixes

- [#891](https://github.com/chakra-ui/chakra-ui/issues/891)
  ([e107acc](https://github.com/chakra-ui/chakra-ui/commit/e107acc8487898a965b0d695c1da71f46fc56d5e))
