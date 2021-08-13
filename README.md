# A very simple SSG

## Inspired

This SSG is inspired by [Kartik Nair](https://github.com/kartiknair/blog)

Styling by [new.css](https://github.com/xz/new.css)

Boilerplate by [Manuel Matuzovic](https://www.matuzo.at/blog/html-boilerplate/)

Favicons generated by [Favicon.io](https://favicon.io/emoji-favicons/)

## How to use it

0. Clone the repo and run command `npm install` to install dependencies
1. Write markdown files in `/content`. Store images and write CSS in `/content/assets`
2. Run the command `npm run build` to build html pages in `/public`
3. See your pages in the browser by running the command `npm run serve`

## How it works

`src/index.js` is the main file.

`src/config.js` stores configuration data.

npm package [front-matter](https://www.npmjs.com/package/front-matter) compiles [YAML](https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html) front matter from posts.

npm package [marked](https://www.npmjs.com/package/marked) compiles [markdown](https://daringfireball.net/projects/markdown/) files to html.

`src/elem.js` stores the header and footer.

`src/marked.js` imports marked and sets options.

npm package [fs-extra](https://www.npmjs.com/package/fs-extra) provides some utilities for easier recursive deletion and copying.

`src/utilities.js` empties the public folder and moves the assets folder to public.

`src/homepage.js` compiles the homepage to `/public/`.

`src/posts.js` compiles posts pages to `/public/`.

npm package [express](https://www.npmjs.com/package/express) provides a simple http server configuration.

`src/serve.js` starts the express server.