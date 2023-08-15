# vitepress-template

This is a barebones template repo to make sure your static site directory is configured correctly, which will make deploying to GitHub Pages easier.

## Pre-setup

You will have to install [Node.js](https://nodejs.org/en/) **V18** to use this template. You can check if you have it installed by running `node -v` in your terminal. If you get an error, or see a version less than 18, you will need to install it. 6.1020 has detailed instructions, which you can find [here](https://web.mit.edu/6.031/www/sp22/getting-started/#11_install_node).

## Setup Guide

1. Click the "Use this template" button to create a new repo in your account.
2. Clone your new repo to your local machine.
3. Run `npm install` to install dependencies.
4. Run `npx vitepress init` to create your static site directory. **Important**: when it asks you where to create the directory, make sure you enter `./docs`, otherwise you will likely have issues when deploying to GH pages later.
   ![Init command](/npx-vitepress.png)
5. Run `npm run docs:dev` to start the development server. You should see a message with the `localhost` path where it is deployed; check it to make sure you can see your site.
   ![Sample site](/sample-site.png)
6. Customize your site!
7. In the `docs/.vitepress/config.mts` file, add your base path which is based on the repository's name. For example, if my repo is named `portfolio-adamjanicki2`, then I would add the following line to the config: `base: "/portfolio-adamjanicki2/"` (make sure to have both opening and closing slashes).
8. Go to the settings tab in your repo, and scroll down to the GitHub Pages section. Under the `source` tab, click `Github Actions`.
   ![Actions config](/gh-actions.png)
9. Add and commit all your files, then push to the `main` branch. You should see your site at `https://61040-fa23.github.io/<your-repo-name>`. _(It's possible that you're site might initially load with no CSS applied. If this happens, just give it a few minutes then refresh the page.)_

If you have trouble with any of these steps, check through the guide to make sure you didn't skip any steps, and then check Discourse or attend studio hours so a TA can help you out :smile:
