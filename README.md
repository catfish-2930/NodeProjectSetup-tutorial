# Node Js Project Setup with Eslint and Prettier - tutorial

## Requirements
You need have a Node Js install in your computer

## First Step
Create a folder ***MyFirstProect*** 

Open the folder in Visual Studio Code

Next open the terminal

Enter command below
```
npm init
```
Just Click Enter

It will generate a file call  ```package.json```

## Second Step
Enter the command below to install eslint
```
npm install --save-dev eslint
```
It will install eslint to ```Dev dependencies```

Next type command below to generate file ```.eslintrc.js```
```
npm init @eslint/config
```
Then it will asking you to install ```@eslint/create-config``` .Just type y

Then it will asking you some question ,Just following this

**To check syntax and find problems**

**CommonJS (require/exports)**

**None of these**

**No**

**Node**

**JavaScript**

## Third Step
Next we will install prettier

Just type the command below to install prettier
```
npm install --save-dev --save-exact prettier
```

Next create a file ```.prettierrc``` in your project folder

Enter the following rules
```
{
  "useTabs": false,
  "tabWidth": 2,
  "printWidth": 100,
  "singleQuote": true,
  "trailingComma": "none",
  "bracketSpacing": true,
  "semi": true,
  "endOfLine": "auto"
}
```
## Fourth Step
Next you need to install eslint-config-prettier to turn off unnecessary eslint rules might conflict with prettier

Just type the command below to install eslint-config-prettier
```
npm install --save-dev eslint-config-prettier
```
Next you need to install eslint-plugin-prettier,it will help you to run prettier as an eslint rules

Just type the command below to install eslint-plugin-prettier
```
npm install --save-dev eslint-plugin-prettier
```

Next replace the ```.eslintrc.js``` to rules below
```
module.exports = {
  env: {
    commonjs: true,
    es2021: true,
    node: true
  },
  extends: ['eslint:recommended', 'plugin:prettier/recommended'],
  parserOptions: {
    ecmaVersion: 'latest'
  },
  rules: {}
};
```
Now , you already done to setup the project

## Last Step
For Vscode you need these rules inside your ```settings.json``

So when you click CTRL + S ,it will auto format
```
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```
Next just restart your vscode
