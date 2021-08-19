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



# Customize Tailwind CSS Configuration

### Create tailwind configuration file

    npx tailwindcss init

    This will generate tailwind.config.js file

    tailwind.config.js file is used to configure your own color palette, font, apply, purge etc.

### Whenever you do changes in tailwind.config.js file you need to run

    npm run build


# Build for Production (Reduce File Size)

### Install NODE_ENV

    npm install win-node-env

### Open package.json File then write below script

    "scripts": {"prod": "NODE_ENV=production npx tailwindcss build ./src/tailwind.css -o ./public/tailwind.css“},

### Include which file should be purged. Open tailwind.config.js file then write code

    purge:[‘./public/**/*.html’]

### Make your code Production Ready

    npm run prod