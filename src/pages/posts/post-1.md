---
title: 'Mi primera publicación en el blog'
pubDate: 2022-07-01
description: 'Este es la primera publicación de mi nuevo blog Astro.'
author: 'Alumno de Astro'
image:
    url: 'https://docs.astro.build/assets/full-logo-light.png'
    alt: 'El logotipo completo de Astro.'
tags: ["astro", "bloguear", "aprender en público"]
---
# Mi primera publicación en el blog

Publicado el: 2022-07-01

¡Bienvenido a mi _nuevo blog_ sobre el aprendizaje de Astro! Aquí, voy a compartir mi viaje de aprendizaje a medida que construyo un nuevo sitio web.

## Lo que he conseguido

1. **Instalación de Astro**: En primer lugar, he creado un nuevo proyecto Astro y configurar mis cuentas en línea.

2. **Creación de páginas**: Luego aprendí cómo hacer páginas creando nuevos archivos `.astro` y colocándolos en la carpeta `src/pages/`.

3. **Creación de publicaciones**: ¡Esta es mi primera publicación! ¡Ahora tengo páginas de Astro y publicaciónes en Markdown!

## Próximos pasos

Terminaré el tutorial de Astro, y luego seguiré añadiendo más publicaciones. Mira este espacio para más por venir.

https://www.compart.com/en/unicode/U+24D8
!Integro

Unicode Character “ⓘ” (U+24D8)
ⓘ Pan+Integro


///
I need a web landing page in astro web
To create an Astro webpage, you'll first want to have 
some familiarity with HTML and CSS since the core 
structure of your site will be built using these 
technologies. However, given that Astro is designed for 
creating static sites quickly without needing a build 
step or server setup like traditional web development 
tools (e.g., Jekyll), here's how you can create an 
attractive landing page with basic HTML and CSS:

1. Create the directory structure of your site in Astro, 
which will automatically generate files for static 
hosting platforms such as GitHub Pages once deployed. 
Here is a simple folder layout to follow within 
`astro-project`:
```bash
/astrosite  # where you'll deploy later on
|__ /public    # assets (images and CSS) go here!
    ├── index.html
|__ src        # source files (.astro, .md for markdown 
pages if needed) will be in this folder:
       |_ landing-page/  
          └── _layouts      # page layout definitions 
like a basic one can live here as `default.astro` 
                            (e.g., <head>, <body> 
structures, etc.) to apply on all pages)
          ├── index.html    # your main landing-page 
content goes into this file!
              └── img/       # images directory if used 
in the page itself or referenced externally  
```
2. Write an HTML structure within `index.html` that can 
be extended with Astro's templating system: 

Create a simple main landing-page layout inside 
`/landing-page/_layouts/default.astro`:

```javascript
---
// Layout configuration, like sections to yield or 
variables passed from parent page if necessary (omit for 
now)
title: 'Landing Page Title' // The title of your 
document will appear in the browser tab and can also be 
used as a link on social media platforms.
headerTitle: "Welcome!"      // This could serve as an 
introductory header section or SEO meta-descriptor. 
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- Page title -->
    <title>{pageTitle}</title>
    
    <!-- Stylesheet (linked here for demonstration, but 
you could use CSS frameworks/components)-->
    <link rel="stylesheet" href="/public/styles.css"/> 
</head>
<body>
    {/* Header */}
    <header>{headerTitle}</header>
    
    <!-- Main content -->
    <main id="content">
        Your landing page's main body goes here! Add 
your introductory text, call to action (CTA), images 
etc. 
        
        {/* You can add more sections below */}
        Here is a featured image:
        <!-- Include this feature image in the 
/public/img directory -->
            <img src="/public/img/{imageName}.jpg" 
alt="Landing Page Image">
            
    </main>
    
    {/* Footer (if necessary) */}
</body>
</html>
```
3. Create a main `index.html` file within 
`/landing-page/` which extends the layout: 

Add some welcome text and make sure to reference any 
external CSS files or images you'll use on your landing 
page, like so (within public/assets):

_public/img/_  
    - featuredimage.jpg      # Your main image here! It 
could be a product photo, company logo etc., used in the 
header for example: `<img 
src="/public/img/featuredimage.jpg" alt="Cool Feature">` 

    
Make sure you have `styles.css`:  
_public/assets/_   
```css
/* stylesheet to style your landing page components 
(fonts, colors etc.) */
body {
    font-family: Arial, sans-serif; /* Or any desired 
fonts for better readability and aesthetics*/
}
header h1{
   color: #ff0;}  /* Bright yellow highlighting the 
welcome header text on white backgrounds (or your 
landing page's primary colors) */
```
4. Once you have this structure in place, build it with 
`npm run build`, then publish to GitHub Pages using 
Astro CLI (`astrohub`) or deploy directly through a 
service like Netlify: 
    - For local deployment (in development mode): Run 
your site locally via the terminal command 
`./scripts/_dev.sh`. Note that this does not do 
client-side optimizations, but allows for quick 
iteration and live previewing during editing sessions 
using LiveReload or similar plugins in case you want to 
extend with CSS libraries like Bootstrap:
    ```bash
       ./scripts/_dev.sh start // Start development 
server 
       npm run serve   // Recommended over HTTPS here 
(but remember this is not a production setup!) for 
faster load times and ease of debugging during the 
design process. Use `npm run build` to bundle your site 
before publishing on GitHub Pages, Netlify etc., or you 
can use `./scripts/_publish_to_gh-pages .build/` 
directly after building (it's not a real command but it 
describes what we want: deploy static files generated by 
the Astro CLI).
    ```
Remember to commit changes regularly and push them 
upstream for GitHub Pages! 
    
You can extend your landing page with additional 
HTML/CSS or JavaScript, as well adding SEO-friendly meta 
tags within `head` of `_layouts/` files. For dynamic 
content like images from external sources (social media 
etc.), you'll want to look into Astro integrations for 
those if necessary — they offer great flexibility but 
are not covered in this baseline example.
  
5. Keep your SEO and accessibility mindful as well, such 
as using proper `alt` tags on images (`<img 
alt="Description of the image" 
src="/public/imageName"/>`) to aid with both search 
engine crawling algorithms & users who may rely heavily 
on screen readers or other assistive technologies.
  
This structure provides a foundation upon which you can 
build and extend your landing page, but remember that 
web design is an iterative process! Be sure to test 
across different devices (responsiveness), browser 
compatibilities where necessary, accessibility standards 
for all user groups - from sighted folks with no 
disabilities through the screen-reader friendly 
environment up till those who are blind or partially 
vision impaile.

Happy coding and remember: your website's purpose is to communicate a clear message! Keep 
that at heart while you design, make it responsive & accessible for all visitors out there too 
:).

ollama run phi3.5