# geektime_wasm_tuturial

## emscripten 安装

推荐 [官网教程](https://emscripten.org/docs/getting_started/downloads.html#installation-instructions-using-the-emsdk-recommended) 中使用 sdk 的方式进行安装。

> 最后需注意，将相关路径加入到环境变量中。

## part1

1. clone 工程

   ```
   git clone https://github.com/silan-liu/geektime_wasm_tuturial.git
   ```

2. 进入 part1 目录，将 main.cc 编译为 wasm。

   ```
   cd part1
   emcc main.cc -s WASM=1 -O3 -o main.html
   ```

   这一步会生成 `main.html、main.js、main.wasm` 几个文件。

3. 进入 server 目录，执行如下命令，启动 node 服务器：

   ```
   cd server
   npm run build
   ```

4. 在浏览器打开 `localohost:9999/main.html`，则可看到效果。
