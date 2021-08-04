# Tailwind-latest
Project created to demonstrate the installation of tailwind CSS as a postcss plugin.

# Installation instructions to install Tailwind CSS as a postcss plugin

Step 1: Use command npm init -y to create package.json in your directory

Step 2: Use command npm install -D tailwindcss autoprefixer postcss-cli
This command will install tailwindcss, autoprefixer and postcss-cli as dev dependencies.

Step 3: Initialise the tailwind.config.js file
Use command - npx tailwindcss init -p
This command will install tailwind as a postcss plugin
This is used to create a config file to customize the tailwind configurations. It is an optional step.

Step 4: Create tailwind.css file, public/index.html file and public/styles.css file.
index.html file is used to add the templates needed for webpage.
styles.css is added in index.html add styles to webpage.

Step 5: Use the @tailwind directive to inject Tailwind’s base, components, and utilities styles into your CSS file. 
@tailwind base;
@tailwind components;
@tailwind utilities;

Step 6: Add build command in package.json
build command - postcss tailwind.css -o ./public/styles.css
This command is used to compile tailwind styles. 
tailwind.css is the file which has to be compiled and public/styles.css will contain the output of compilation. If the file public/styles.css is not created earlier then it will automatically be created.

## To enable JIT and Purge

Step 1: Add mode: 'jit' in tailwind.config.js
Step 2: purge: [
    './public/**/*.html'
]
Step 3: Add the prod build command
build prod command for windows - SET NODE_ENV=production & postcss tailwind.css -o ./public/styles.css
