# Node.js 开发环境搭建

## nvm

### 安装nvm {id="nvm_install"}

GitHub [nvm-sh/nvm](https://github.com/nvm-sh/nvm)

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

### 查看nvm版本 {id="show-nvm-version"}

```bash
➜  ~ nvm --version
0.40.3
```

## nvm管理node.js

### 安装 Node.js {id="nvm-install-node.js"}

安装最新 lts 版本

```bash
nvm install 24
```

### 卸载 Node.js {id="nvm-uninstall-node.js"}

```bash
nvm uninstall 24
```

### 设置Node.js默认版本 {id="set-default-version"}

```Bash
nvm alias default 24
```

### 切换Node.js版本  {id="switch-version"}

```Bash
nvm use 12
```

### 查看本地安装Node.js版本列表 {id="show-local-versions"}

```Bash
nvm ls
```

### 查看可以安装Node.js版本列表 {id="show-remote-versions"}

```Bash
nvm ls-remote
```

### 查看当前使用的Node.js版本 {id="show-current-version"}

```Bash
nvm current
```


## nrm

### 安装 nrm {id="nrm_install"}

```Bash
npm install nrm -g
```

如果安装速度慢，可以使用淘宝镜像加速安装

```Bash
npm install nrm -g --registry=https://registry.npmmirror.com/
```

### 查看镜像列表

使用命令 `nrm ls` 查看可以使用镜像列表

```bash
➜  ~ nrm ls
  npm ---------- https://registry.npmjs.org/
  yarn --------- https://registry.yarnpkg.com/
  tencent ------ https://mirrors.tencent.com/npm/
  cnpm --------- https://r.cnpmjs.org/
* taobao ------- https://registry.npmmirror.com/
  npmMirror ---- https://skimdb.npmjs.com/registry/
  huawei ------- https://repo.huaweicloud.com/repository/npm/
```

使用命令 `nrm use` 查看可以切换镜像

```Bash
➜  ~ nrm use taobao
 SUCCESS  The registry has been changed to 'taobao'.
```

