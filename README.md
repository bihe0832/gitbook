# 使用模板创建新书

## checkout 项目

- 命令

    ```shell
    git clone https://github.com/bihe0832/gitbook.git
    ```

- 事例

    ```shell  
    ➜  github  git clone https://github.com/bihe0832/gitbook.git
    Cloning into 'gitbook'...

    ……

    Unpacking objects: 100% (9/9), done.
    ```
    
## 安装依赖，推荐使用npm，gitbook 安装会非常缓慢，npm建议使用 v10.23.0

- 命令
    
    ```shell
    gitbook install
    ```     
    或者
       
    ```shell     
    npm install
    ```
    
- 事例

    ```shell          
    ➜  gitbook git:(master) npm install

     ……

    1 package is looking for funding
      run `npm fund` for details
    ```
    
## 初始化新书

- 命令

    ```shell
    gitbook init
    ```  
    
- 事例

    ```shell       
    ➜  gitbook git:(master) gitbook init
    warn: no summary file in this book
    info: create SUMMARY.md
    info: initialization is finished
    ```
    
## 预览新书

- 命令

    ```shell
    gitbook serve
    ```   
    
- 事例

    ```shell
    ➜  gitbook git:(master) ✗ gitbook serve

    Live reload server started on port: 35729
    Press CTRL+C to quit ...

    ……

    Starting server ...
    Serving book on http://localhost:4000
    ```

## 生成新书

- 命令

    ```shell
    gitbook build
    ```

- 事例

    ```shell
    ➜  gitbook git:(master) ✗ gitbook build
    info: 25 plugins are installed
    info: 20 explicitly listed

    ……

    info: found 1 pages
    info: found 2 asset files
    warn: "options" property is deprecated, use config.get(key) instead
    warn: "options.generator" property is deprecated, use "output.name" instead
    info: >> generation finished with success in 0.8s !
    ```

# Linux 一键安装脚本

```shell
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" 
nvm --version
nvm install node
cd ~/.nvm 
nvm --version

npm config delete proxy
npm config set registry https://registry.npm.taobao.org -g
npm config get registry
npm config get proxy
npm install -g nrm
nrm test
nrm use taobao

nvm install v10.23.0
nvm use v10.23.0
ln -s ~/.nvm/versions/node/v10.23.0/bin/node /usr/bin/node
npm install gitbook-cli -g
npm install && gitbook build
```


