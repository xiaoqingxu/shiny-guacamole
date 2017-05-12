
## 框架介绍
目的：快速搭建react框架，该框架技术架构：react+webpack+es6
该框架基于 create-react-app 修改完成，[git地址](https://github.com/facebookincubator/create-react-app)

## 初始化项目
1. 克隆初始化项目：`git clone https://github.com/du1990/webpack_react_init.git`
2. 下载依赖包： `npm install`
3. 运行：`npm start`
5. 测试：`npm test`
4. 打包：`npm deploy`

## 配置介绍与修改
- 修改静态资源路径: package.json > `"homepage": "//static-cdn.fishsaying.com/..."` 
- 添加 less 配置：`npm install --save-dev less less-loader`
    ```js
    {
        test: /\.less$/,
        loader: 'style!css!less'
    }
    ```

## 文件目录结构
- src
    - components                //公用组件
    - modules                   //模块
        - module1               //模块1
            - action.js
            - constants.js
            - index.js
            - reducer.js 
            - router.js
            - index.css
            - index.png
        - module2               //模块2
            - action.js
            - constants.js
            - index.js
            - reducer.js 
            - router.js
            - index.css
            - index.png
    - utils                     //工具 js
    - static                    //公用文件
        - main.css              //公用 css
        - img
    - redux
        - store.js
        - reducer.js
    - index.js                  //入口文件
    - api.js                    //rest 接口

## 常用插件和版本号
- "react": "^15.5.4",
- "react-dom": "^15.5.4",
- "react-router": "^3.0.0"
- "react-redux": "^5.0.4"
- "redux": "^3.0.5"
- "redux-logger": "^3.0.1"      //redux 调试 log
- "redux-thunk": "^2.2.0"
- "jest": "18.1.0"              //test
- "axios": "^0.16.1"            //ajax

## 代码规范
见 代码规范.md
