# sapper-dark-starter

The default [Sapper](https://github.com/sveltejs/sapper) template, available for Rollup and additional scripts for deployment to [Dark](https://darklang.com).

## Clone the repo
`git clone git@github.com:aashanand/sapper-dark-starter.git`

`cd sapper-dark-starter`

## Set Environment Variables

To start, first set up some environment variables.

`export DARK_STATIC_ASSETS_BASE_URL='replace-with-your-canvas-name';`

`export DARK_USERNAME='replace-with-your-dark-username';`

`export DARK_PASSWORD='replace-with-your-dark-password';`

Then, there are just four more steps before you're in business.

## Install modules

`npm install`

## Special build command

`npm run build-dark-assets`

## Get Dark CLI
You only need to do this once per project. Every other time, you can skip to the next step.

`npm run get-dark-cli`

## Deploy to Dark

`npm run deploy`

If you get "Not Found" on this step, you need to visit [https://darklang.com/a/USERNAME-CANVASNAME](https://darklang.com/a/USERNAME-CANVASNAME) first in your browser.

## Serve from Dark

1. Go to [https://darklang.com/a/USERNAME-CANVASNAME](https://darklang.com/a/USERNAME-CANVASNAME)
2. Create a new `HTTP GET` handler with route `/`. For the handler expression, use `StaticAssets:serveLatest` -> `"index.html"`.
3. Create a new `HTTP GET` handler with route `/:rest`. For the handler expression, use `StaticAssets:serveLatest` -> `rest`.

Like so.

![backend handler](public/backend-handler.png)

## Demo
Demo lives [here](https://aash-sapper-dark-starter.builtwithdark.com/).