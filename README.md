# Turborepo template [![test](https://github.com/mayank1513/esbuild-plugin-removetestid/actions/workflows/test.yml/badge.svg)](https://github.com/mayank1513/esbuild-plugin-removetestid/actions/workflows/test.yml) [![codecov](https://codecov.io/gh/mayank1513/esbuild-plugin-removetestid/graph/badge.svg?token=8LX1NLNVRV)](https://codecov.io/gh/mayank1513/esbuild-plugin-removetestid) [![Version](https://img.shields.io/npm/v/esbuild-plugin-removetestid.svg?colorB=green)](https://www.npmjs.com/package/esbuild-plugin-removetestid) [![Downloads](https://img.jsdelivr.com/img.shields.io/npm/dt/esbuild-plugin-removetestid.svg)](https://www.npmjs.com/package/esbuild-plugin-removetestid) [![Unit Tests](https://github.com/mayank1513/esbuild-plugin-removetestid/actions/workflows/test.yml/badge.svg)](https://github.com/mayank1513/esbuild-plugin-removetestid/actions/workflows/test.yml) ![npm bundle size](https://img.shields.io/bundlephobia/minzip/esbuild-plugin-removetestid)

- ✅ Fully Treeshakable (`import from esbuild-plugin-removetestid/client/component`)
- ✅ Full TypeScript Support
- ✅ Unleash the full power of React18 Server components
- ✅ Works with all build systems/tools/frameworks for React18

## Install

```bash
$ pnpm add esbuild-plugin-removetestid
# or
$ npm install esbuild-plugin-removetestid
# or
$ yarn add esbuild-plugin-removetestid
```

> A quick tip: Delete all stale branches `git branch --merged main | grep -v '^[ *]*main$' | xargs git branch -d`



## What's different from scaffolding turbo-repo by `create-turbo`

The default scafold from `create-turbo` just gives some stubs for sharing packages across projects/apps within current monorepo.

This template is targeted for sharing packages across organizations/repos publically or privately.

Following features make it really cool and useful

- Unit tests with `vitest`
- Build setup with `tsup` and `esbuild-react18-useclient` Supports React Server components out of the box
- **Automatic file generation**
  - just run `yarn turbo gen` and follow the propts to auto generate your new component with test file and dependency linking
  - follow best practices automatically
- As a small extra gift Fork Me component is already added in UI
- github actions/workflows to auto publish your package when version changes

## Checklist


- [ ] Review and merge `setup-repo` branch to main
  - We have created a new branch called `setup-repo`. This will automatically rename packages and update workflows, directories etc. with your repo's name
  - [ ] Create PR from `setup-repo` to `main`
  - [ ] Review changes and merge
- [ ] **Imp** - update publish workflow - replace `fork-me` with `esbuild-plugin-removetestid` in `.github/workflows/publish.yml` file.
- [ ] **Imp** - update test workflow - replace `fork-me` with `esbuild-plugin-removetestid` in `.github/workflows/test.yml` file
- [ ] Set up `CodeCov`
  - If you merged changes from `setup-repo` branch, we have already updated the badges, however, codecov needs a token
  - [ ] Visit codecov and setup your repo
  - [ ] Update codecov badge in README
  - [ ] Create repository secrets for `CODECOV_TOKEN`
- [ ] Add `NPM_AUTH_TOKEN` to repository secrets to automate publishing package
  - [ ] login to your `npm` account and create automation token
  - [ ] Create a new repository secrets `NPM_AUTH_TOKEN`
- [ ] Update description in `packages/esbuild-plugin-removetestid/package.json`
- [ ] Create your library and update examples
- [ ] Update README
- [ ] Push your changes/Create PR and see your library being automatically tested and published
- [ ] Optionally deploy your example(s) to Vercel.
- [ ] You are most welcome to star this template, contribute, and/or sponsor the terbo-repo-template project / me

## What's inside?

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

### Apps and Packages

This Turborepo includes the following packages/apps:

- `nextjs`: a [Next.js](https://nextjs.org/) app
- `docs`: another [Next.js](https://nextjs.org/) app
- `ui`: a React component library shared by both `nextjs` and `docs` examples
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo

Each package/example is 100% [TypeScript](https://www.typescriptlang.org/).

### Build

To build all apps and packages, run the following command:

```
cd my-turborepo
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```
cd my-turborepo
pnpm dev
```

### Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```
npx turbo link
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turbo.build/repo/docs/core-concepts/monorepos/running-tasks)
- [Caching](https://turbo.build/repo/docs/core-concepts/caching)
- [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching)
- [Filtering](https://turbo.build/repo/docs/core-concepts/monorepos/filtering)
- [Configuration Options](https://turbo.build/repo/docs/reference/configuration)
- [CLI Usage](https://turbo.build/repo/docs/reference/command-line-reference)

### 🤩 Don't forger to start this repo!

Want handson course for getting started with Turborepo? Check out [React and Next.js with TypeScript](https://www.udemy.com/course/react-and-next-js-with-typescript/?referralCode=7202184A1E57C3DCA8B2)

![Repo Stats](https://repobeats.axiom.co/api/embed/2ef1a24385037998386148afe5a98ded6006f410.svg "Repobeats analytics image")

## License

Licensed as MIT open source.

<hr />

<p align="center" style="text-align:center">with 💖 by <a href="https://mayank-chaudhari.vercel.app" target="_blank">Mayank Kumar Chaudhari</a></p>
