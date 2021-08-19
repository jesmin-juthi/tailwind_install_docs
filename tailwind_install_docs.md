# Tailwind Intallation without PostCSS

### Create package.json file with default options

    npm init –y

### Install Tailwind CSS

    npm install tailwindcss

### Install AutoPrefixer

    npm install autoprefixer

Create public Folder then inside public folder create index.html.

Create src Folder then inside src folder create tailwind.css file. src/tailwind.css file is used to write tailwind directives and custom CSS.

### Open src/tailwind.css file then write code

    @tailwind base;
    @tailwind components;
    /* Write Custom CSS */
    @tailwind utilities;

### Create Build Script to compile src/tailwind.css file to actual css file. To do this, Open package.json file then write code

    "scripts": {"build": "tailwindcss build ./src/tailwind.css -o ./public/tailwind.css"}

    Run the script
    npm run build

This will generate a compiled tailwind.css file inside public folder. This public/tailwind.css file has actual tailwind css code. Should not modify this file.

Done


