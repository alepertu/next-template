Custom Next.js 13 Typescript project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). Includes TailwindCSS for styles, Jest for testing. Prettier, ESLint, Husky and Github Actions pre configured.

Deps managed by Yarn@Berry, no installs required.

## Getting Started

Fork and get going. Run the development server:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

Edit src/app/page.tsx to change the initial page.

## Configuration

Search for !FIXME comments and customize the template.

## File and folder structure

- /.github/workflows - Contains files regarding Github Actions.
  - create-branch.yml - Action that automates branch creation when an Issue is opened. Triggers on Issue.
  - lint.yml - Action that performs various tasks over the src folder: it runs ESLint, type checks, formats with Prettier and runs tests with Jest. Triggers on push to main.
  - release-please.yml - Action that integrates Google's [release-please](https://github.com/googleapis/release-please) to the workflow, automating releases, changelog, etc.
- /.husky - Contains Husky commit hooks
  - /\_ - Husky base files
  - commit-msg - Runs [commitlint](https://github.com/conventional-changelog/commitlint) on each commit, this enforces the [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/) format.
  - pre-commit - Runs [lint-staged](https://github.com/okonet/lint-staged) on each commit, linting staged files.
- /.next - Next.js build folder.
- /.swc/plugins/v4 - Next.js compiler cache.
- /.vscode - Visual Code Studio configurations.
  - extensions.json - Lists recomended VSCode extensions for this workspace.
  - settings.json - Settings stored for this workspace.
- /.yarn - Files used by Yarn Berry
  - /cache - Saves compressed versions of all the proyects deps. Equivalent to node_modules folder.
  - /releases - Contains the Yarn release used in this project.
  - /sdks - Contains the editor SDKs used with Yarn.
  - /unplugged - Holds machine-specific build artifacts.
  - install-state.gz - Yarn optimization file.
- /public - Holds project static files. Accessible by Next.js anywhere from the base URL (/).
  - /static - Holds project static assets (images, fonts, etc.).
  - favicon.ico - The site's favicon.
- /src - Next.js main project folder.
  - /\_\_tests\_\_ - Contains Jest .test.tsx files.
  - /app - Holds pages and routes. Folders are used to define routes. Files are used to create UI that is shown for the route segment.
    - /api - Route to handle API endpoints.
    - layout.tsx - Holds the topmost \<html\> and \<body\> tags.
    - page.tsx - Site's main page.
  - /components - Holds the project components, standarized by Atomic Design.
    - /atoms - Smallest component that makes sense (e.g. login button).
    - /molecules - Functional group of atoms (e.g. login email input and label).
    - /organisms - Complex group of molecules and atoms (e.g. login form).
    - /templates - Organized structure of pages, composed by organisms (e.g. login page).
  - /styles - Holds the project styles.
    - globals.css - Styles applied to the entire project.
- .commitlintrc.json - Holds the configuration for commitlint.
- .eslintrc.json - Holds the configuration for ESLint.
- .gitattributes - Defines path attributes to be considered by Git.
- .gitignore - Holds the project's Git ignored files.
- .pnp.cjs - Yarn's main dependencies tree file.
- .pnp.loader.mjs - Yarn optimization file.
- .prettierignore - Holds files ignored by Prettier.
- .prettierrc.json - Holds the configuration for Prettier.
- .yarnrc.yml - Holds the configuration for Yarn.
- jest.config.js - Holds the configuration for Jest.
- next-env.d.ts - Next.js Typescript configuration.
- next.config.js - Holds the configuration for Next.js.
- package.json - Project's Manifest.
- postcss.config.js - Holds the configuration for postcss, used by TailwindCSS.
- README.md - This file.
- tailwind.config.js - Holds the configuration for TailwindCSS.
- yarn.lock - Yarn's lockfile.
