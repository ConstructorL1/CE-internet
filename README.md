# 环境准备
## 安装node
[node官网](https://nodejs.org/en/) 下载LTS版本安装程序包，运行程序包完成安装。

node安装成功后，查看版本命令：npm -v

## 安装yarn
为什么需要yarn，详见 [yarn官网](https://yarn.bootcss.com/)。
```
npm install yarn -g
```

如果出现如下报错：
```
npm ERR! code ETIMEDOUT
npm ERR! errno ETIMEDOUT
npm ERR! network request to https://registry.npmjs.org/yarn failed, reason: connect ETIMEDOUT 104.16.16.35:443
npm ERR! network This is a problem related to network connectivity.
npm ERR! network In most cases you are behind a proxy or have bad network settings.
npm ERR! network
npm ERR! network If you are behind a proxy, please make sure that the
npm ERR! network 'proxy' config is set properly.  See: 'npm help config'
```

则可通过改用淘宝镜像来解决：
```
npm install -g yarn --registry=https://registry.npm.taobao.org
```

安装完成后一并调整镜像仓库配置
```
yarn config set registry https://registry.npm.taobao.org -g
```
yarn安装成功后，查看版本命令：yarn -v

## 安装vuepress
参考 [vuepress官方教程](https://www.vuepress.cn/guide/getting-started.html)安装vuepress。
```
# 安装
yarn global add vuepress # 或者：npm install -g vuepress
```

## 安装插件
```
npm i vuepress-plugin-auto-sidebar -D
```

## 运行本项目
```
# 运行
yarn docs:dev # 或者 npm run docs:dev

# 发布： 发布前请配置发布仓库地址，详见deploy.sh
yarn deploy # 或者 npm run deploy
```