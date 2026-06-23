# Airline CheckIn App

## Overview

This project is a comprehensive airline check-in application built using React and bootstrapped with Vite, ensuring a fast and efficient development environment. It leverages TypeScript for robust type-checking, ESLint and Stylelint for maintaining code quality and consistent styling, Prettier for automatic code formatting, Storybook for isolated UI component development, and Cypress for end-to-end testing.

The application follows the Atomic Design Principle, which structures UI components into atoms, molecules, organisms, templates, and pages, promoting reusability and maintainability. SCSS is used for styling, providing powerful features like variables, nesting, and mixins to write clean and manageable CSS.

# Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Development Server](#running-the-development-server)
- [Configuration](#configuration)
  - [ESLint](#eslint)
  - [Stylelint](#stylelint)
  - [Prettier](#prettier)
  - [TypeScript](#typescript)
  - [Storybook](#storybook)
  - [Cypress](#cypress)
- [Directory Structure](#directory-structure)
- [Design & Style Configuration](#design--style-configuration)
- [Open Source Modules or Libraries](#open-source-modules-or-libraries)
- [Additional Information for Extended Development](#additional-information-for-extended-development)

## Getting Started

### Prerequisites

Ensure you have the following installed:

- **Node.js** (v20.11.1 or higher)
- **Yarn** (v1.22.22 or higher) [Recommended] or **npm** (v10.2.4 or higher)

To get started with our project, you need to ensure that Node.js, Yarn, and npm are installed on your system. Follow the steps below:

#### 1. Install Node.js (v20.11.1 or higher)

**Check if Node.js is already installed:**

```sh
node -v
```

If not installed, follow these steps:

#### Download Node.js:

Visit the Node.js download page.

1. Download the LTS version (recommended for most users) or the Current version if you need the latest features.
   Install Node.js:

2. Run the installer and follow the on-screen instructions.
   Ensure the installer includes npm (Node Package Manager), which comes bundled with Node.js.
   Verify Installation:

```sh
node -v
npm -v
```

#### 2. Install Yarn (v1.22.22 or higher)

#### Check if Yarn is already installed:

```sh
yarn -v
```

#### If not installed, follow these steps:

1. Using npm (recommended):

```sh
npm install --global yarn
```

2. Using Homebrew (macOS):

```sh
brew install yarn
yarn -v
```

#### Check if npm is already installed:

```sh
npm -v
```

If npm is not installed, then add the below command:

```sh
brew install npm
```

#### Note: npm comes bundled with Node.js, but if you need to update or install a specific version:

Update npm:

```sh
npm install -g npm@latest
```

### Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/Jaima07/Airline-CheckIn-App.git
cd MeldCX_Development
yarn install
```

### Node Version Compatibility

If you face any difficulties regarding node version issues, ensure your Node.js version matches the specified requirements before proceeding.

### Running the Development Server

Before running the server, please follow the steps below:

1. Create a `.env.local` file.

2. Copy the data from `.env.example` into `.env.local`.

```
yarn dev
```

### Configuration

#### ESLint

ESLint is configured to enforce coding standards and catch errors. Configuration is in `.eslintrc.json`.

#### Stylelint

Stylelint is configured to enforce consistent styling rules. Configuration is in `.stylelintrc.json`.

#### Prettier

Prettier is configured to format code. Configuration is in `.prettierrc`.

#### TypeScript

TypeScript is used for type checking. Configuration is in `tsconfig.json`.

#### Storybook

Storybook is used for developing UI components in isolation. Configuration is in `.storybook` directory.

#### Running Storybook

To run Storybook, execute the following command:

```bash
yarn storybook
```

#### Cypress

Cypress is used for end-to-end testing. Configuration is in `cypress` directory.

#### Running End-to-End Tests

To execute end-to-end tests, run the following command:

```bash
yarn cypress:open
```

After running the command, a browser will open with two options. Please follow these steps:

1. Select **End to End Testing**.
2. Choose your required browser, **Chrome (recommended)**.
3. Click on **Start E2E Testing in Chrome**.

A new page will open in the Chrome browser. From there, you can choose the pages you want to run or check for end-to-end testing.

### Directory Structure

```
|__ cypress # Cypress tests
├── public/ # Public files
├── src/ # Source code
│ ├── assets/
│ ├── components/
│ ├── styles/
│ ├── contexts/
│ ├── hooks/
│ └── pages/
│ ├── styles
│ └── templates/
│ └── utils/
│ ├── App.tsx
│ └── main.tsx
|___ .env.example
|__  .env.preview
├── .storybook # Storybook configuration
├── .eslintrc.json # ESLint configuration
├── .stylelintrc.json # Stylelint configuration
├── .prettierrc # Prettier configuration
├── tsconfig.json # TypeScript configuration
├── vite.config.ts # Vite configuration
├── package.json # Package dependencies and scripts
└── README.md # Project documentation

```

Here, .env.preview file is utilized for a stage in the deployment process that closely mirrors the production environment.

In our project, each component—whether it is an atom, molecule, or organism—is structured with four specific files

```
components/(atoms or molecules or organisms)/
  ├── index.cy.tsx      #Contains Cypress component tests if available
  ├── Index.module.scss #Contains SCSS styles specific to the component
  ├── Index.stories.tsx #Contains Storybook stories for the component
  └── index.tsx         #Contains the component's implementation
```

### Design & Style Configuration

In this project, we’ve adopted a module-based SCSS methodology. Also known as modular SCSS or modular CSS, this approach structures SCSS files to enhance reusability, maintainability, and separation of concerns.

We’ve organized our styles into a dedicated folder within src/styles. This folder contains all the necessary mixins, variables, and other styling tools. Here is the file structure:

```
src/styles
  ├── animation.scss
  ├── base.scss
  ├── mixin.scss
  ├── tools.scss
  ├── variables
  │   ├── color.scss
  │   ├── constant.scss
  │   └── fonts.scss
  └── fonts

```

The styles defined in index.module.scss are scoped to the React component, preventing global style conflicts. Below is an example of how to use these styles within a React component.
In our project, we follow the atomic design principle, which organizes components into atoms, molecules, and organisms.

#### Naming Conventions

#### Atoms

- **Prefix:** `a_`
- **Naming Convention:** Camel Case
- **Example:** `a_text`

#### Molecules

- **Prefix:** `m_`
- **Naming Convention:** Camel Case
- **Example:** `m_boxItem`

#### Organisms

- **Prefix:** `o_`
- **Naming Convention:** Camel Case
- **Example:** `o_boxItemList`

#### Element Naming Convention

**Element Naming:**

Format: `prefix_componentName__element`

Example for Organism: `o_boxItemList__content`

#### Importing and Using Styles in Components

For each component, styles are imported from their respective SCSS module files, ensuring encapsulation and preventing global style conflicts.

**Import Styles:**

```javascript
import styles from "./index.module.scss";
```

### Open Source Modules or Libraries

#### Moment.js for Timezone Handling

In our project, we leverage Moment.js for robust timezone management.  
[Visit Moment Timezone NPM page](https://www.npmjs.com/package/moment-timezone)

##### React Router DOM

The `react-router-dom` package contains bindings for using React Router in web applications.  
[Visit react-router-dom](https://www.npmjs.com/package/react-router-dom)

##### Cypress

Fast, easy, and reliable testing for anything that runs in a browser.  
[Visit Cypress](https://www.cypress.io/)

##### Storybook

Storybook is a standalone tool that runs alongside your app, allowing you to develop UI components in isolation.  
[Visit Storybook](https://storybook.js.org/)

##### ESLint

A pluggable linting utility for JavaScript and TypeScript.  
[Visit ESLint](https://eslint.org/)

##### Stylelint

A mighty, modern CSS linter and fixer that helps you avoid errors and enforce conventions in your styles.  
[Visit Stylelint](https://stylelint.io/)

##### Prettier

An opinionated code formatter that ensures consistent code style across your project.  
[Visit Prettier](https://prettier.io/)

##### TypeScript

TypeScript extends JavaScript by adding types, which help catch errors and provide better tooling for large-scale JavaScript applications.  
[Visit TypeScript](https://www.typescriptlang.org/)

##### Cross-env

A utility that allows you to use environment variables across different operating systems.  
[Visit Cross-env](https://github.com/kentcdodds/cross-env)

##### SASS

A mature, stable, and powerful CSS extension language.  
[Visit SASS](https://sass-lang.com/)

### Additional information for extend development

#### Steps needs to follow when, we're doing component testing

To properly configure Cypress for testing React components with TypeScript, follow these steps:

1. install the necessary Cypress plugins:

```sh
  yarn add @cypress/react --dev
```

2. Create Cypress Support File
   Create or update cypress/support/component.ts to add the mount command:

```sh
import { mount } from '@cypress/react18';

Cypress.Commands.add('mount', mount);

```

3. add bellow settings in tsconfig.ts

```sh
{
  "compilerOptions":{
     "types": ["cypress", "node"]
  },
   "include": ["src", "cypress"]
}
```
