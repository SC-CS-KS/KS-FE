# package.json

在一个完整的项目中，package.json 文件无处不在。首先，在项目根目录会有，其次在 node_modules 中也频现。

## 作用
package.json 文件其实就是对项目或者模块包的描述，里面包含许多元信息。
比如项目名称，项目版本，项目执行入口文件，项目贡献者等等。
npm install 命令会根据这个文件下载所有依赖模块。

## 文件创建

package.json 文件创建有两种方式，手动创建或者自动创建。

手动创建
直接在项目根目录新建一个 package.json 文件，然后输入相关的内容。
自动创建
也是在项目根目录下执行 npm init，然后根据提示一步步输入相应的内容完成后即可自动创建。

## 配置文件说明
```text
name：项目/模块名称，长度必须小于等于214个字符，不能以"."(点)或者"_"(下划线)开头，不能包含大写字母。
version：项目版本。
author：项目开发者，它的值是你在https://npmjs.org网站的有效账户名，遵循“账户名<邮件>”的规则，例如：zhangsan zhangsan@163.com。
description：项目描述，是一个字符串。它可以帮助人们在使用npm search时找到这个包。
keywords：项目关键字，是一个字符串数组。它可以帮助人们在使用npm search时找到这个包。
private：是否私有，设置为 true 时，npm 拒绝发布。
license：软件授权条款，让用户知道他们的使用权利和限制。
bugs：bug 提交地址。
contributors：项目贡献者 。
repository：项目仓库地址。
homepage：项目包的官网 URL。
dependencies：生产环境下，项目运行所需依赖。
devDependencies：开发环境下，项目所需依赖。
scripts：执行 npm 脚本命令简写，比如 “start”: “react-scripts start”, 执行 npm start 就是运行 “react-scripts start”。
bin：内部命令对应的可执行文件的路径。
main：项目默认执行文件，比如 require(‘webpack’)；就会默认加载 lib 目录下的 webpack.js 文件，如果没有设置，则默认加载项目跟目录下的 index.js 文件。
module：是以 ES Module(也就是 ES6)模块化方式进行加载，因为早期没有 ES6 模块化方案时，都是遵循 CommonJS 规范，而 CommonJS 规范的包是以 main 的方式表示入口文件的，为了区分就新增了 module 方式，但是 ES6 模块化方案效率更高，所以会优先查看是否有 module 字段，没有才使用 main 字段。
eslintConfig：EsLint 检查文件配置，自动读取验证。
engines：项目运行的平台。
browserslist：供浏览器使用的版本列表。
style：供浏览器使用时，样式文件所在的位置；样式文件打包工具parcelify，通过它知道样式文件的打包位置。
files：被项目包含的文件名数组。
```