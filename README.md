# SCSS playground

## TL; DR

This repo will provide you with a live reloading environment that will compile your `/scss/styles.scss` into `/css/styles.css` which is loaded by the `index.html` and served on http://localhost:8080.

## Y tho'?

So you wanna practice some Sass?

You can do it in many different ways, such as [online dedicated editors](https://www.sassmeister.com/), or via online environments like [codepen](https://blog.codepen.io/documentation/editor/using-css-preprocessors/) or [jsfiddle](https://jsfiddle.net/boilerplate/scss) but I figured I feel most comfortable doing stuff in my editor of choice, with all my extensions loaded and ready, fonts, themes and whatnot.

So I decided to create this boilerplate / starter repo to try out a couple npm packages as well as creating a desktop environment that would work for me, then why not make it available for others?

## How to use this repo

All you have to do is clone this repo, then, on your terminal run:

    $ npm install

and when ready to start hacking some [SCSS](https://sass-lang.com/documentation/syntax#scss):

    $ npm run dev

Open your browser and go to http://localhost:8080, now you can go ahead and write your markup (`index.html`) and styles (`/scss/styles.scss`) and see your changes reflected on your browser!

## Packages being used

I picked a few packages that I thought were modern and that were good for the job:

- [sass](https://www.npmjs.com/package/sass) A newer implementation of the compiler for Sass.
- [Servør](https://www.npmjs.com/package/servor) To run a static file server that I brought in specifically for the live reloading aspect (Reloading the page manually for every change gets old really quick).
- [Stylelint](https://www.npmjs.com/package/stylelint) I came accross this one and kinda wanted to see what it was about. Seems to work well integrated with VSCode. I previously have used [sass-lint](https://www.npmjs.com/package/sass-lint) and that one has worked really well, but seems no longer maintained.
- [Concurrently](https://www.npmjs.com/package/concurrently) To be able to run both the server and the Sass compiler at the same time.
- [Prettier](https://prettier.io/) A code formatter that will make the code look consistent no matter who writes it and will free your mind from trying to decide whether you should add a space or new line in there.

## Editor

[VSCode](https://code.visualstudio.com/) is my editor of choice, and if you use it too you'll notice some recommended extensions I added to the `.vscode/extensions.json` settings.

## Dot files

You probably also noticed the presence of a couple more files:

- `.editorconfig` Some basic configs for how the editor should treat the formatting of the code (see [here](https://editorconfig.org/))
- `.node-version` helps determine what version of node this environment will use. It will be picked up by packages like [avn](https://www.npmjs.com/package/avn).
- `.prettierrc` Prettier configs.
- `.stylelintrc.json` and `.styleintignore` Will be used by stylelint. In this repo we are using a recommended set of linting rules via the former and making sure the linter only picks up the `.scss` files on the latter.
