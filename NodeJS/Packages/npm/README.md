# npm

是一个js的包管理工具，它的出现真的是让前端技术飞速发展。
它做的事情类似maven。

## nrm
是一个方便的npm的镜像仓库管理工具，可以便捷的在各个镜像仓库之间切换。
```bash
//从淘宝镜像下全局安装nrm
npm install -g nrm --registry=https://registry.npm.taobao.org
```

## 命令行
```bash
npm install -g nrm
nrm ls #查看nrm使用的镜像
nrm use taobao #使用淘宝镜像
npm i  #安装依赖
```

```bash
npm run dev
	本地运行
npm run build:prod
	打包生成静态文件
```

### 安装模块  

```bash
npm install -g nrm  # 利用npm安装全局模块
npm install nrm # 安装但不写入package.json
npm install nrm –save # 安装并写入package.json的”dependencies”中
npm install nrm –save-dev # 安装并写入package.json的”devDependencies”中
```

### 卸载模块  

```bash
npm uninstall lodash  # 卸载 lodash 模块
npm uninstall lodash --save # 卸载模块的同时删除在 package.json 文件中的记录
npm uninstall lodash@3.* # 卸载 lodash 模块 3.* 版本
```
