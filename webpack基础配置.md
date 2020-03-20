# webpack基础配置
### 安装
命令: npm install webpack wepback-cli -D  
	  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;npm install webpack-dev-server -D
### 基础配置
```
const path = require('path');

module.exports = {
  devServer: {
    port: 3000,
    contentBase: path.resolve(__dirname, 'dist'),
    progress: true,
    // open: true   // 自动打开浏览器
  },
  mode: 'development',  // production
  entry: './src/index.js',
  output: {
    filename: 'bundle.[hash].js',
    path: path.resolve(__dirname, './dist')
  },
  plugins: [
    new htmlWebpackPlugin({
      template: './src/index.html',
      filename: 'index.html',
      minify: {
        removeAttributeQuotes: true, // 去掉html的双引号
        collapseInlineTagWhitespace: true, // 压缩
      },
      hash: true
    })
  ]
}
```

### 配置CSS
命令: cnpm install mini-css-extract-plugin -D

```
  module: {
    rules: [
      {
        test: /\.css$/,
        use: [
          MiniCssExtractPlugin.loader,
          'css-loader',
          'postcss-loader',
        ]
      },
      {
        test: /\.less$/,
        use: [
          MiniCssExtractPlugin.loader,
          'css-loader',
          'postcss-loader',
          'less-loader',
        ]
      },
    ]
  }
}
```
