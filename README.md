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
