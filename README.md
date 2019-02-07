# Setup Eslint for ReactJs Project

1. create-react-app project-name
2. yarn add -D eslint babel-eslint eslint-config-airbnb eslint-plugin-jsx-a11y eslint-plugin-react eslint-plugin-import
3. create new file .eslintrc.js and write code below this:
```
module.exports = {
  'extends': 'airbnb',
  'parser': 'babel-eslint',
  'env': {
    'jest': true,
  },
  'rules': {
    'no-use-before-define': 'off',
    'react/jsx-filename-extension': 'off',
    'react/prop-types': 'off',
    'comma-dangle': 'off'
  },
  'globals': {
    "fetch": false
  }
}
```
4. add a script to package.json, write code below this:
```
"lint": "eslint src/**/*.js src/**/*.jsx"
```
5. create new file again, for setting up editor config, write code below this:
```
root = true
[*]
charset = utf-8
end_of_line = lf
indent_size = 2
indent_style = space
insert_final_newline = true
trim_trailing_whitespace = true
```
6. finish. Try yarn lint.