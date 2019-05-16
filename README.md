# learnVue
## 拿到一个Vue项目如何入手
## package.json
    https://blog.csdn.net/DreamFJ/article/details/82146779
    {
      "name": "onlineshare",
      "version": "1.0.0",
      "description": "A Vue.js project",
      "author": "gxg",
      "private": true,
      "scripts": {
        "dev": "node build/dev-server.js",
        "start": "node build/dev-server.js",
        "build": "node build/build.js",
        "unit": "cross-env BABEL_ENV=test karma start test/unit/karma.conf.js --single-run",
        "e2e": "node test/e2e/runner.js",
        "test": "npm run unit && npm run e2e",
        "lint": "eslint --ext .js,.vue src test/unit/specs test/e2e/specs"
      },
      "dependencies": {
        "axios": "^0.16.2",
        "babel-polyfill": "^6.23.0",
        "cropper": "^3.0.0-rc.3",
        "element-ui": "^1.3.6",
        "eventsource-polyfill": "^0.9.6",
        "jquery": "^3.2.1",
        "moment": "^2.18.1",
        "screenfull": "^3.3.1",
        "vue": "^2.3.3",
        "vue-awesome-swiper": "^2.4.2",
        "vue-images": "^1.0.9",
        "vue-infinite-scroll": "^2.0.1",
        "vue-qrcode-component": "^2.1.1",
        "vue-router": "^2.3.1",
        "vuex": "^2.3.1"
      },
      "devDependencies": {
        "autoprefixer": "^6.7.2",
        "babel-core": "^6.22.1",
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.2.10",
        "babel-plugin-istanbul": "^4.1.1",
        "babel-plugin-transform-runtime": "^6.22.0",
        "babel-preset-env": "^1.3.2",
        "babel-preset-stage-2": "^6.22.0",
        "babel-register": "^6.22.0",
        "chai": "^3.5.0",
        "chalk": "^1.1.3",
        "chromedriver": "^2.46.0",
        "connect-history-api-fallback": "^1.3.0",
        "copy-webpack-plugin": "^4.0.1",
        "cross-env": "^4.0.0",
        "cross-spawn": "^5.0.1",
        "css-loader": "^0.28.0",
        "eslint": "^4.8.0",
        "eslint-config-standard": "^6.2.1",
        "eslint-friendly-formatter": "^2.0.7",
        "eslint-loader": "^1.7.1",
        "eslint-plugin-html": "^3.0.0",
        "eslint-plugin-promise": "^3.4.0",
        "eslint-plugin-standard": "^2.0.1",
        "express": "^4.14.1",
        "extract-text-webpack-plugin": "^2.0.0",
        "file-loader": "^0.11.1",
        "friendly-errors-webpack-plugin": "^1.1.3",
        "html-webpack-plugin": "^2.28.0",
        "http-proxy-middleware": "^0.17.3",
        "inject-loader": "^3.0.0",
        "karma": "^1.4.1",
        "karma-coverage": "^1.1.1",
        "karma-mocha": "^1.3.0",
        "karma-phantomjs-launcher": "^1.0.2",
        "karma-phantomjs-shim": "^1.4.0",
        "karma-sinon-chai": "^1.3.1",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-spec-reporter": "0.0.30",
        "karma-webpack": "^2.0.2",
        "lolex": "^1.5.2",
        "mocha": "^3.2.0",
        "nightwatch": "^0.9.12",
        "node-sass": "^4.5.3",
        "opn": "^4.0.2",
        "optimize-css-assets-webpack-plugin": "^1.3.0",
        "ora": "^1.2.0",
        "phantomjs-prebuilt": "^2.1.14",
        "rimraf": "^2.6.0",
        "sass-loader": "^6.0.6",
        "selenium-server": "^3.0.1",
        "semver": "^5.3.0",
        "shelljs": "^0.7.6",
        "sinon": "^2.1.0",
        "sinon-chai": "^2.8.0",
        "url-loader": "^0.5.8",
        "vue-lazyload": "^1.0.6",
        "vue-loader": "^12.1.0",
        "vue-resource": "^1.3.3",
        "vue-style-loader": "^3.0.1",
        "vue-template-compiler": "^2.3.3",
        "webpack": "^2.6.1",
        "webpack-bundle-analyzer": "^2.2.1",
        "webpack-dev-middleware": "^1.10.0",
        "webpack-hot-middleware": "^2.18.0",
        "webpack-merge": "^4.1.0"
      },
      "engines": {
        "node": ">= 4.0.0",
        "npm": ">= 3.0.0"
      },
      "browserslist": [
        "> 1%",
        "last 2 versions",
        "not ie <= 8"
      ]
    }
    ----------------------
    babel-polyfill:可以将ES6代码转为ES5代码,Polyfill你可以理解为“腻子”，就是装修的时候，可以把缺损的地方填充抹平。
    有些浏览器版本的发布早于ES6的定稿和发布，例如IE9浏览器对ES6的兼容性问题,无法识别let和const；
    // 转码前
    input.map(item => item + 1);

    // 转码后
    input.map(function (item) {
      return item + 1;
    });
    https://www.jianshu.com/p/4822852792d1
    http://www.ruanyifeng.com/blog/2016/01/babel.html
    配置文件.babelrc
    命令行转码babel-cli
    babel-node
    babel-register
    -----------------------
    cropper：图片剪裁jQuery插件，cropper：种植者，庄稼人;收割器；收割机;
    jQuery:一个 JavaScript 库,通过 jQuery，可以选取（查询，query） HTML 元素，并对它们执行"操作"（actions）。
    基础语法： $(selector).action() 
    $(this).hide() - 隐藏当前元素
    $("p").hide() - 隐藏所有 <p> 元素

    $("p.test").hide() - 隐藏所有 class="test" 的 <p> 元素

    $("#test").hide() - 隐藏所有 id="test" 的元素
    https://www.runoob.com/jquery/jquery-tutorial.html
    关于图片在线剪裁，上传头像会用到该组件。
    https://www.cnblogs.com/libin-1/p/5966683.html
    http://www.jq22.com/jquery-info9322
    
    
    
## Vue项目布局
