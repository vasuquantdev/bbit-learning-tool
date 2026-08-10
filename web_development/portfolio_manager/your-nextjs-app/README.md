# `your-nextjs-app`

This will be your main working directory. Refer to the labs in the directory above (prefixed by a lab number and a hyphen), while doing your work here.

Some information about a NextJS project structure:
* The `src` directory contains important files that make the website work. Your work will be mostly concentrated in this directory
* There are a few important directories inside `src` that we will go over:
  * The `components` directory contains all React components that are not rendered as a webpage. Components here can be imported from any of the webpages in the `pages` directory, or from other components inside the same directory. You will be creating a component file in this directory in one of the labs
  * The `pages` directory contains both *frontend* and *backend* (inside the `api` directory) website functionality. This directory usually contains the `index.jsx` (or `index.js`) file that gets rendered as the default webpage when the user accesses the website URL. You will be making changes in the `index.jsx` file
    * While the `api` directory inside `pages` contains API routes that help the frontend side of the webapp have dynamic and data-driven functionality, our focus will be mostly on the frontend. However, NextJS as a framework is able to create complex and performant fullstack web applications, and is not restricted to just the frontend

## Getting Started

See the [Web Development lab README](../../README.md) for clone and Docker setup instructions.

Once the stack is running, open [http://localhost:3000](http://localhost:3000) with your browser to see the UI of your web application.
