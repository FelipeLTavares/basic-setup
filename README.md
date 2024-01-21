## BASIC SETUP

- STEP 1: ``` npm init -y ```
- STEP 2: ``` npm i -D eslint prettier ```
- STEP 3: To setup prettier configs: in the project root create a file called ``` .prettierrc.json ``` and write:
```
{
  "tabWidth": 2,
  "semi": false,
  "singleQuote": true
}
```
- STEP 4: To setup eslint configs: ``` npx eslint --init ``` and set your preferences, depending on what choose it would appear a file called ``` .eslintrc.json ``` with this code:
```
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es2021": true
    },
    "extends": "eslint:recommended",
    "parserOptions": {
        "ecmaVersion": "latest"
    },
    "rules": {
    }
}
```
- STEP 5: ``` npm i -D husky lint-staged``` and make sure to add a script on the ```package.json``` : "postinstall": "npx husky install"
- STEP 6: create a file called ```.lintstagedtc.json``` and insert this:
```
{
    "*.js": ["npx eslint", "npx prettier --write"]
}
```
