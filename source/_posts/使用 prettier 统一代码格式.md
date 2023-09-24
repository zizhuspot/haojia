---
title: Using prettier to Unify Code Formatting

date: 2023-09-12 15:24:37
categories:
  - development tool
tags:
  - development tool
  - program
  - prettier

description: Recently in the development of the project encountered a formatting problem , in order to solve this problem , we studied the Prettier unified code formatting tool . This tool allows us to code for unified formatting , the use of this tool , we will be able to more efficiently complete the code formatting work , and to ensure that our code has the consistency and readability .

cover: https://s2.loli.net/2023/09/23/Da2ljIqEFNuGoOV.png

---

## Prettier Introduction

Prettier is an arbitrary code formatting tool, why is it arbitrary, because it is not responsible for code checking, only responsible for its own set of rules for formatting. And it has very few configurable formatting items, so it's easy to get started. (But the formatting is very good in practice)
It supports the formatting of the following languages:

- JavaScript (including experimental features)
- JSX
- Angular
- Vue
- Flow
- TypeScript
- CSS, Less, and SCSS
- HTML
- Ember/Handlebars
- JSON
- GraphQL
- Markdown, including GFM and MDX
- YAML

## Formatting code with Prettier

### Install Prettier

```css
npm install --save-dev --save-exact prettier
```

### After installation, you need to configure two files in the root directory.

`.prettierrc.json` is used to configure how Prettier is formatted for customization.

`.prettierignore` is similar to .gitignore in that it is used to ignore directories or files when formatting.

### Formatting a file:

```arduino

npx prettier --write .

```
In this way, the files of the entire project will be formatted. If you want to format only the files in a certain directory, you can change the command:

```css
npx prettier --write ./src/views/

```
### .prettierrc.json

The prettier configuration rules file. There are very few configuration items that can be configured, which is good. You can refer to the official configuration file

```json
{
  "semi": false,
  "singleQuote": true,
  "arrowParens": "always",
  "htmlWhitespaceSensitivity": "ignore",
  "trailingComma": "all"
}

```
### .prettierignore

We use `.prettierignore` to ignore specified files and directories

```sh

build
coverage
*.html

```
There are two other ways to ignore formatting:

The first is to add the `prettier-ignore` comment to ignore formatting in some code.

```sh

// prettier-ignore

```

The second is to run the prettier command with an ignored file extension

```arduino

prettier --write . '!**/*.{js,jsx,vue}'


```

## Installing Prettier on VS Code

Prettier, as mentioned above, formats files from the command line.

We can also use Prettier in editors by installing the Prettier extension on the editor. I'm going to use VS Code as an example, but if you want to see how to install extensions for other editors, you can check here.

The way to install it is very simple, you can find the extension in the VS Code sidebar, search for Prettier and you will find `Prettier - Code formatter`, you can use it after installing it.

After installation, you need to configure the default formatting method in the VS Code configuration:

```css

  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[less]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },

```

This allows you to format with `alt + shift + f`.

## Add Prettier Formatting to Git Hooks

The goal is to format every Git commit.

First you need to install hushy and lint-stage.

```sh

npm install --save-dev husky lint-staged
npx husky install
npm pkg set scripts.prepare="husky install"
npx husky add .husky/pre-commit "npx lint-staged"

```

Then add the hook code to the `package.json`.

```json

{
  "lint-staged": {
    "**/*": "prettier --write --ignore-unknown"
  }
}

```

## Harmonize Prettier usage

Having both a command prettier and an editor extension prettier installed, it's a pain in the ass if they're not unified for repeated cross-hopping.

I've encountered a project that was formatted differently by Prettier in VS Code on multiple computers. The problem was that the project didn't have a `prettierrc.json` configuration file, so VS Code formatted it according to the rules in the system configuration.
After adding the configuration file, I found that the configuration file did not take effect. It was still in its own way.

So, I tried restarting VS Code and formatting it again. As a result, the `alt + shift + f` formatting was the same as the `npx prettier --write` . . The results were unified, both formatted as `.prettierrc.json`.

## Other

### Save as formatting

In VS Code's configuration, search for `Format On Save` and check the box that allows you to format files when you save them.
This saves you from having to press `Shift + Alt + F` every time (though I still do it out of habit).
After Prettier formatting, the > line in the closing tab is now a new line.

```html

<el-dropdown-item
  v-for="option in indicatorOptions"
  :command="option.value"
  :key="option.value"
  >{{ option.name }}</el-dropdown-item
>

```

This code format is so anti-programmer that it drives OCD to death. The solution is to modify the `.prettierrc.json` configuration file.

```css

{
  ...,
  htmlWhitespaceSensitivity: “ignore”
}

```

```html

<el-dropdown-item
  v-for="option in indicatorOptions"
  :command="option.value"
  :key="option.value">
  {{ option.name }}
</el-dropdown-item>

```
## Prettier implementation principle

prettier is based on editing techniques. In fact, compilation tools like webpack, vue, and react work in a similar way to native JavaScript.

Parsing the source code and converting the source strings into `AST` syntax trees.
Do some additions, deletions, and modifications to the generated AST.
Recursively generate the target code from the AST.

Prettier's formatting is done in the third part, formatting the code according to its defined format and replacing the original code.



