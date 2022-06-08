
<!-- Projeect off on -->
<img src="https://i.postimg.cc/3RhCfbvw/Untitled-1.png" alt="Line Feed" width="700">

<!-- PROJECT Title -->
<br />
<p align="center">
  <h3 align="center"><a href="https://github.com/suncodebd/EslintSetup/">React and Next.js Eslint and Prettier setup for auto code Formating and Best practice</a></h3>

<!-- TABLE OF CONTENTS -->



## Table of Contents


- [Editor Setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Create Linting Configuration file manually](#create-linting-configuration-file-manually)
- [Contact](#contact)

<!-- HOW TO RUN -->

Please follow the below instructions to run this project in your computer:


<!-- Editor Setup -->

## Editor Setup

You can use any editor but as I personally prefer VS Code. I will give some instructions about how I prefer VS code to be setup for React applications.

### Plugins

You need to install the below plugins:

- ESLint by Dirk Baeumer
- Prettier - Code formatter by Prettier


### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the project root folder
2. Create a new file called "settings.json" inside that folder.
3. Paste the below json in the newly created settings.json file and save the file.

```json

 {   
    // config related to code formatting
    
    "editor.formatOnSave": true,
    "[javascript]": {
      "editor.formatOnSave": false,
      "editor.defaultFormatter": null
    },
    "[javascriptreact]": {
      "editor.formatOnSave": false,
      "editor.defaultFormatter": null
    },
    "javascript.validate.enable": false, //disable all built-in syntax checking
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true,
      "source.fixAll.tslint": true,
      "source.organizeImports": true
    },
    "eslint.alwaysShowStatus": true,
    // emmet
    "emmet.triggerExpansionOnTab": true,
    "emmet.includeLanguages": {
      "javascript": "javascriptreact"
    }
  }

```

If you followed all previous steps, the theme should change and your editor should be ready.

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="https://i.postimg.cc/tgp8WD4h/Screenshot-2022-06-04-222059.png" alt="Line Feed" width="700">

## Linting Setup

In order to lint and format your React project automatically according to popular airbnb style guide, I recommend you to follow the instructions below.

### Install Dev Dependencies

```sh
yarn add -D prettier
npx install-peerdeps --dev eslint-config-airbnb
yarn add -D eslint-config-prettier eslint-plugin-prettier
```

or You can also add a new script in the scripts section like below to install everything with a single command:

```json

    "lint": "yarn add -D prettier && npx install-peerdeps --dev eslint-config-airbnb && yarn add -D eslint-config-prettier eslint-plugin-prettier"

```

and then simply run the below command in the terminal -

```sh
yarn lint #or 'npm run lint'
```

### Create Linting Configuration file manually

Create a `.eslintrc.json` file in the project root and enter the below contents:

```json

{
        "extends": [
          "airbnb",
          "airbnb/hooks",
          "eslint:recommended",
          "prettier",
          "plugin:jsx-a11y/recommended"
        ],       
       
        "env": {
          "browser": true,
          "node": true,
          "es6": true,
          "jest": true
        },
        "rules": {
          "react/jsx-props-no-spreading": 0,
          "import/prefer-default-export": 0,
          "react/react-in-jsx-scope": 0,
          "react-hooks/rules-of-hooks": "error",
          "no-console": 0,
          "react/state-in-constructor": 0,
          "indent": 0,
          "linebreak-style": 0,
          "react/prop-types": 0,
          "jsx-a11y/click-events-have-key-events": 0,
          "react/jsx-filename-extension": [
            1,
            {
              "extensions": [".js", ".jsx","ts","tsx"]
            }
          ],
          "prettier/prettier": [
            "error",
            {
              "trailingComma": "es5",
              "singleQuote": true,
              "printWidth": 100,
              "tabWidth": 4,
              "semi": true,
              "endOfLine": "auto"
            }
          ]
        },
        "plugins": ["prettier", "react", "react-hooks"]
      }

```

<!-- CONTACT -->

## Contact

Md Minarul islam - [suncodebd@gmail.com](mailto:suncodebd@gmail.com)

Youtube Setup Video Link: [](https://www.youtube.com/channel/UCNQCuB877R0NpDjhjJ76yeg)

Youtube Channel: [SuncodeBD](https://www.youtube.com/channel/UCNQCuB877R0NpDjhjJ76yeg)

