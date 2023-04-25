# ✨ Belajar Tailwind CSS
Materi Pembelajaran Tailwind CSS. Sumber Channel Yotube WPU.<br>
https://www.youtube.com/playlist?list=PLFIM0718LjIUHFRMzPJ0wGjx9_NlC5d1h<br>


## 1. Instalasi & Konfigurasi Tailwind CSS
https://tailwindcss.com/docs/installation<br>
Install Tailwind CSS<br>
Install tailwindcss via npm, and create your tailwind.config.js file.<br>

    npm install -D tailwindcss<br>
    npx tailwindcss init

Configure your template paths<br>
Add the paths to all of your template files in your tailwind.config.js file.<br>

    /** @type {import('tailwindcss').Config} */
    module.exports = {
      content: ["./src/**/*.{html,js}"],
      theme: {
        extend: {},
      },
      plugins: [],
    }

Add the Tailwind directives to your CSS<br>
Add the @tailwind directives for each of Tailwind’s layers to your main CSS file.<br>

    @tailwind base;
    @tailwind components;
    @tailwind utilities;
    
Start the Tailwind CLI build process<br>
Run the CLI tool to scan your template files for classes and build your CSS.<br>

    npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch

Start using Tailwind in your HTML<br>
Add your compiled CSS file to the <head> and start using Tailwind’s utility classes to style your content.<br>

    <!doctype html>
    <html>
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <link href="/dist/output.css" rel="stylesheet">
    </head>
    <body>
      <h1 class="text-3xl font-bold underline">
        Hello world!
      </h1>
    </body>
    </html>
