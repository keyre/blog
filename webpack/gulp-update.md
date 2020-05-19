
## 升级node10以及gulp4.0

> 之前公司的框架是使用 webpack2 + gulp@3.9 ，升级了 npm@10 后，要将gulp升级到4.0版本才可以使用。

- 报错：`gulp _start[8024]: c:\ws\src\node_contextify.cc:626: Assertion `args[1]->IsString()' failed`   
操作步骤：
  1. npm rm -g gulp
  2. npm install -g gulp-cli
  3. npm install --save-dev gulp@4.0.0
  <br />
   

- 报错：`Node Sass does not yet support your current environment: Windows 64-bit with Unsupported runtime (64)`     
操作步骤：
  1. npm uninstall node-sass -D
  2. npm install node-sass -D
  <br />

- 修改gulp打包配置，文件目录（具体参考自己项目）：`_task\gulp\gulp_build_dist.js`
  ```js
    // 修改前
    gulp.task('dist_build', function (cb) {
      gulp_build_config.gulp_build(env)
    });

    // 修改后
    gulp.task('dist_build', async(cb) => {
      await gulp_build_config.gulp_build(env)
    });

  ```
  <br />
