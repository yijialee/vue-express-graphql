 
vue-express-graphql
# This is a simple project dev with vue express and graphql.

# 1 create a new vue project
vue init webpack lee-vue

# 2 create a new express project
express lee-express

# 3 create a new folder lee
# 4 create "src" folder in "lee", create "client" folder and "server" folder in "src"
# 5 copy files in "lee-express" to "server" folder
# 6 copy files in "lee-vue/src" to "client" folder. then copy the folders and files left to root of "lee" folder
# 7 edit package.json
modify script
```
"scripts": {
    "server": "nodemon index.js",
    "client": "node build/build.js"
  }
```
# 8 edit "config/index.js"
modify index assetsRoot assetsSubDirectory assetsPublicPath 
```
    index: path.resolve(__dirname, '../src/server/public/index.html'),//'../dist/index.html'),
    assetsRoot: path.resolve(__dirname, '../src/server/public/'),
    assetsSubDirectory:  './static/' ,//'static',
    assetsPublicPath: './' ,//'/',
```

# 9 edit "webpack.base.conf.js"
modify output
```
  output: {
    path: config.build.assetsRoot,
    filename: '[name].js',
    publicPath: '/'
  },
```
