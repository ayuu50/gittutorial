LIRA: Radiologist Workstation Frontend

The LIRA Radiologist Workstation is a dedicated frontend application built for efficient viewing, diagnosis, and management of medical imaging data. It provides the core user interface for image retrieval, viewer functionality, and reporting.

🚀 Technology Stack

This application is built for performance and scalability using a modern development stack:

Component

Technology

Description

Framework

React

Component-based UI development.

Language

TypeScript

Strong typing for safer, more robust code.

Build Tool

Vite

Fast development server and optimized production builds.

Styling

Tailwind CSS

Utility-first CSS framework for rapid, responsive UI development.

✨ What's New & Key Updates

Recent development has centered on pipeline stability, core application logic, and preparing the codebase for long-term health.

Commit Detail

File(s) Affected

Date

CI/CD Stabilization

lira_jenkinsfile, lira_prod_jenkinsfile

Added explicit configuration to build from the main branch across both staging and production pipelines.

Viewer Logic

src

Implemented an empty body structural change (likely for new feature scaffolding).

Auth Update

package.json, pnpm-lock.yaml

Implemented critical updates related to the authentication system (auth changes).

Routes & Fetching

index.html

Changed core application routes and optimized data fetching processes for better performance.

Security & Build

tailwind.config.js

Updated configuration related to the MFA backend integration.

Installation

This project utilizes npm and package-lock.json.

# Install all project dependencies
$ npm install


Available Scripts

This project uses standard Vite scripts for development and testing:

Command

Description

$ npm run dev

Starts the development server with HMR (Hot Module Replacement).

$ npm run build

Compiles the TypeScript and bundles the application for production deployment.

$ npm run test

Executes the test suite (likely configured via Cypress/Jest).

$ npm run lint

Runs ESLint to enforce code quality and styling rules.

⚙️ Configuration Notes

Expanding ESLint Configuration

If developing production features, it is required to upgrade the ESLint configuration to enable type-aware lint rules for maximum safety.

Steps Required:

Update parserOptions in your main ESLint config file (.eslintrc.cjs) to include project paths:

parserOptions: {
  ecmaVersion: 'latest',
  sourceType: 'module',
  project: ['./tsconfig.json', './tsconfig.node.json'],
  tsconfigRootDir: __dirname,
}


Replace Extension: Change plugin:@typescript-eslint/recommended to either plugin:@typescript-eslint/recommended-type-checked or the stricter plugin:@typescript-eslint/strict-type-checked.

Add React Plugins: Install and include eslint-plugin-react and add plugin:react/recommended & plugin:react/jsx-runtime to the extends list.

🤝 Contributing

Before starting work, please ensure your branch is up-to-date with main. All new features and fixes must include relevant test coverage.
