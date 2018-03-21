# Eslint - for project using React

This is an Eslint configuration we use for Javascripts apps built using React. It extends the Airbnb config, based on their [Javascript Styleguide](https://github.com/airbnb/javascript).  

## Usage

To include in Webpack, add the .eslint file to your repository and  add the following loader to your configuration:

```javascript
{
    enforce: 'pre',
    test: /\.js$/,
    exclude: /node_modules/,
    loaders: ['eslint-loader']
},
```

