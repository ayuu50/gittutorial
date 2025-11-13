# LIRA: Radiologist Workstation Frontend

The LIRA Radiologist Workstation is a dedicated frontend application built for efficient viewing, diagnosis, and management of medical imaging data. It provides the core user interface for image retrieval, viewer functionality, and reporting.

## 🚀 Technology Stack

This application is built for performance and scalability using a modern development stack:

| Component | Technology | Description | 
 | ----- | ----- | ----- | 
| **Framework** | React | Component-based UI development. | 
| **Language** | TypeScript | Strong typing for safer, more robust code. | 
| **Build Tool** | Vite | Fast development server and optimized production builds. | 
| **Styling** | Tailwind CSS | Utility-first CSS framework for rapid, responsive UI development. | 

## ✨ What's New & Key Updates

Recent development has centered on pipeline stability, core application logic, and preparing the codebase for long-term health.

| Commit Detail | File(s) Affected | Date | 
 | ----- | ----- | ----- | 
| **CI/CD Stabilization** | `lira_jenkinsfile`, `lira_prod_jenkinsfile` | Added explicit configuration to build from the `main` branch across both staging and production pipelines. | 
| **Viewer Logic** | `src` | Implemented an empty body structural change (likely for new feature scaffolding). | 
| **Auth Update** | `package.json`, `pnpm-lock.yaml` | Implemented critical updates related to the authentication system (auth changes). | 
| **Routes & Fetching** | `index.html` | Changed core application routes and optimized data fetching processes for better performance. | 
| **Security & Build** | `tailwind.config.js` | Updated configuration related to the MFA backend integration. | 

## Installation

This project utilizes `npm` and `package-lock.json`.

```bash
# Install all project dependencies
$ npm install
