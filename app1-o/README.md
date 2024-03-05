# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## What is NPX?

A tool that comes with Node.js, to streamline the process of running Node.js packages from the npm registry without the need for manual installations. It is particularly useful for one-time tasks or quickly trying out tools.

## Usage

To set up a new React.js application using `create-react-app`, run the following command:

```bash
npx create-react-app app1-o
```

This command downloads and runs `create-react-app`, creating a new React.js application named `app1-o`.

## Benefits of using npx

- **No Manual Installations:** `npx` allows you to run packages without cluttering your system with unnecessary installations.
  
- **Convenience:** Particularly useful for one-time tasks or trying out tools quickly.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)



Certainly! Here's a simple README file with a step-by-step guide for deploying a React app on Nginx:

---

# React App Deployment with Nginx

This guide outlines the steps to deploy a React app using Nginx on a Linux server.

## Prerequisites

- Node.js and npm installed
- Basic understanding of React.js
- Access to a Linux server (e.g., Ubuntu)

# HTML5 Website on Nginx

This repository contains the configuration files for hosting an HTML5 website using Nginx. The website files are located in the `/var/www/html5` directory.

## Steps

### 1. Create and Build React App

```bash
npx create-react-app app1-o
cd app1-o
npm run build
```

### 2. Install Nginx

```bash
sudo apt update
sudo apt install nginx
sudo systemctl status nginx
```

### 3. Configure Nginx

Navigate to the Nginx configuration directory:

```bash
cd /etc/nginx/conf.d/
```

Create a new configuration file (e.g., `domain.conf`) using a text editor:

```bash
sudo nano domain.conf
```

Add the following configuration:

```nginx
server {
    listen 80;
    listen [::]:80;
    root /path/to/your/app1-o/build;
    index index.html index.htm index.nginx-debian.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

Replace `/path/to/your/app1-o/build` with the actual path to your React app's build folder.

Save the file and exit the text editor.

### 4. Restart Nginx

Restart the Nginx service to apply the changes:

```bash
sudo service nginx restart
```

### 5. Access the React App

Open your web browser and navigate to `http://localhost` or the IP address of your server. You should see your deployed React app.

## Notes

- Ensure that the React app is built (`npm run build`) whenever changes are made.
- If changes don't reflect, clear the browser cache or try a hard refresh.


## Author
- [Visit My Portfolio](https://yatharthchauhan.me)

- [LinkedIn: Yatharth Chauhan](https://www.linkedin.com/in/yatharth-chauhan-729674202/)

- [GitHub: Yatharth Chauhan](https://github.com/YatharthChauhan2362)
