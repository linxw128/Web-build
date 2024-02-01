# 版本依赖npm配置和使用

### 配置

```
# 查看源
npm config get registry
```

配置源
方法一：使用cnpm替代npm
安装cnpm
npm install -g cnpm --registry=https://registry.npmmirror.com

方法二：配置npm的registry
npm config set registry https://registry.npm.taobao.org

建议两者都配置


### 安装依赖

npm install xxxxx --save
npm install xxxxx --save-dev
npm install xxxxx -g


if don't want to make global install with "npm install xxxxx -g", you can run:
"npm install xxxxx" and 
"npx xxxx"

```arduino
// 使用npx
npx create-react-app my-react-app
```
npx 会在当前目录下的`./node_modules/.bin`里去查找是否有可执行的命令，没有找到的话再从全局里查找是否有安装对应的模块，全局也没有的话就会自动下载对应的模块，如上面的 create-react-app，npx 会将 create-react-app 下载到一个临时目录，用完即删，不会占用本地资源。

