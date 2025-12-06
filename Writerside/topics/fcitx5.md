# 中文输入法

在不同的操作系统，安装的命令和软件包名字略有差异， 但配置方法几乎是一样的。

## 安装 Fcitx5

<tabs>
<tab title="Fedora 43">
<code-block lang="bash">
sudo dnf install -y fcitx5 fcitx5-chinese-addons fcitx5-configtool
</code-block>
</tab>
<tab title="Arch Linux">
<code-block lang="bash">
sudo pacman -Sy fcitx5 fcitx5-chinese-addons fcitx5-configtool fcitx5-gtk fcitx5-qtb
</code-block>
</tab>
<tab title="待补充">
Second tab content
</tab>
</tabs>

## 配置

### 1. 开机自启动

使用 **Gnome Tweaks** 工具将 **fcitx5** 添加到开机自启动

### 2. 输入法全局配置

编辑配置文件 **/etc/environment**

```Bash
sudo vim  /etc/environment
```

在文件末尾添加以下内容

```Bash
# 通用输入法配置
GTK_IM_MODULE=fcitx      # GTK 程序
QT_IM_MODULE=fcitx       # Qt 程序
XMODIFIERS=@im=fcitx     # X11 传统程序

# 游戏/多媒体框架
SDL_IM_MODULE=fcitx      # SDL 应用
GLFW_IM_MODULE=fcitx     # GLFW 应用

# 遗留库支持
CLUTTER_IM_MODULE=fcitx  # Clutter 应用
```

### 3. 添加拼音输入法

1. 使用命令 `fcitx5` 启动输入法
    ```bash
    fcitx5
    ```
2. 启动软件 **Fcitx Configuration**, 将 **Pinyin** 输入法到 **输入法分组**
3. 点击 **应用**， 关闭  **Fcitx Configuration** 窗口
4. 重启系统
