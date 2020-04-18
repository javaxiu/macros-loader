# Preprocessor for Webpack

fork from git+https://github.com/jdmichaud/preprocessor-loader.git

# why
'cause author stop maintaining [this project](https://github.com/jdmichaud/preprocessor-loader), and [my issue](https://github.com/jdmichaud/preprocessor-loader/issues/1) was left to open for a while

# use

// webpack.config.js

{
  module: {
    loaders: [
      { test: /\.js$/,
        loader: 'pprocessor?config=pprocessor-loader.json',
        exclude: [/bower_components/, /node_modules/],
      },
    ],
  }
}

// pprocessor-loader.json

"macros": [
    {
      "declaration" : "LOG_INFO(message)",
      "definition" : "console.log(message + ' (__FILE__:__LINE__)');",
      "REG": "/(src:?)(.*)/"
    },
]
