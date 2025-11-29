# LIRA v2 Frontend Application

LIRA v2 is the next generation of our medical data management frontend, built on a robust and modern stack for efficiency and scalability. It provides a responsive and interactive user interface for accessing and managing medical data.

## 🚀 Technology Stack

This application is built upon the following core technologies:

| Component | Technology | Description | 
 | ----- | ----- | ----- | 
| **Frontend Framework** | React | Component-based UI development. | 
| **Language** | TypeScript | Strong typing for safer, more robust code. | 
| **Build Tool** | Vite | Leveraging HMR and Fast Refresh for optimal performance. | 
| **Styling** | Tailwind CSS | Utility-first CSS framework (configured via `tailwind.config.js`). | 

## Installation

This project uses `pnpm` as the package manager.

```bash
# Install all project dependencies
$ pnpm install
# Alternative shorthand (often faster)
$ pnpm i
````

## Available Scripts

| Command | Description |
| ----- | ----- |
| `$ pnpm dev` | Starts the development server with Hot Module Replacement (HMR). |
| `$ pnpm build` | Compiles the TypeScript and bundles the assets for production deployment (output is typically to `./dist`). |
| `$ pnpm lint` | Runs ESLint for code quality and style checks. |
| `$ pnpm preview` | Locally serves the production build for testing. |

## 🧩 Folder Structure

This project follows a standard React/Vite structure, emphasizing component and feature-based organization for scalability.

```
src/
├── assets/          # Static files (images, fonts, local SVGs)
├── components/      # Reusable UI components (buttons, modals, headers)
├── contexts/        # React Context API providers for global state
├── hooks/           # Custom React hooks (e.g., useApi, useAuth)
├── layouts/         # Page templates (e.g., AuthLayout, MainLayout)
├── pages/           # Application views/routes (e.g., Worklist, Viewer, Login)
├── services/        # Logic for API calls, data fetching, and external services (includes axios.ts)
├── types/           # Global TypeScript type definitions
├── utils/           # Helper functions and formatting utilities
├── App.tsx          # Main application router/entry point
└── main.tsx         # Root component rendering (ReactDOM)
```

## Configuration

### API Base URL for Local Development

For local development against a backend running on your machine, the API base URL must be configured to point to your local backend server.

You need to locate the API configuration file (specifically **`axios.ts`** or similar in the `src` directory) and update the base URL constant in your Axios initialization:

```
// Change this line for local development:
const BASE_URL = '[http://127.0.0.1:8080](http://127.0.0.1:8080)';

// The pre-production URL was previously: '[https://preprod.lenektech.com](https://preprod.lenektech.com)'
```

> **Note:** For production or staging environments, it is strongly recommended to use **environment variables** (e.g., via a `.env` file or CI/CD injection) instead of hardcoding the `BASE_URL`.

## 🧼 Common Issues

This table documents known historical issues that have been addressed and serves as a quick reference for related file changes.

| Issue | File(s) Affected | Fixes |
| ----- | ----- | ----- |
| **Dynamic Modalities Not Loading** | `index.html` | Fixed the logic to correctly load dynamic modalities in filters. |
| **Redundant UI Element** | `public` | Removed the action table column for a cleaner user interface. |
| **Incorrect Development URL** | `server.js` | Fixed the application's development URL to ensure proper local serving. |
| **CI/CD Pipeline Instability** | `lirav2_jenkinsfile`, `lirav2_prod_jenkinsfile` | Added a dedicated production Jenkins pipeline and updated main Jenkins file/lock versions for stable builds. |

```
```
