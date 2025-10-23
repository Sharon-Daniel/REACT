# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

React Custom Hooks (useFetch)
This project implements a reusable custom React hook named useFetch to simplify asynchronous data fetching, centralize state management (data, loading, error), and enhance component readability.

Deployment Link

Netlify Deploy
https://68e9fc7a63ad65076b3ca17a--magnificent-pie-24374a.netlify.app/

GitHub Repository
https://github.com/Sharon-Daniel/REACT.git


Project Overview and Features

This application showcases robust data handling by separating concerns:
Custom Hook (useFetch.js): Encapsulates useState and useEffect to manage and expose the full lifecycle of an API call (loading, success, error) based on a dynamic URL dependency.
Two-Phase Loading:
Phase 1 (App.jsx): Simulates initial application setup with an "Initializing Application" screen.
Phase 2 (DataFetcher.jsx): Displays a dedicated "Loading Product Data" spinner during the network request.
Error Handling Test: Includes a feature to switch the API endpoint to an intentionally invalid URL, proving that the hook correctly catches and reports network and HTTP errors to the consuming component.
Usage of useFetch

import useFetch from './hooks/useFetch';

const MyComponent = () => {
  const { data, loading, error } = useFetch('your-api-url');

  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;
  
  
  return <div>{JSON.stringify(data)}</div>;
};


Setup and Installation
Clone the repository:
git clone https://github.com/Sharon-Daniel/REACT.git
cd my-fetch-hook-app

Install dependencies:
npm install

Start the development server:
npm run dev
