# Flutter开发环境搭建

## 下载 flutter {id="download-flutter"}

[Flutter 下载地址 ](https://docs.flutter.dev/install/manual#install-flutter)

## 安装 flutter {id="install-flutter"}

```Bash
mkdir ~/develop/

tar -xf ~/Downloads/flutter_linux_3.38.4-stable.tar.xz -C ~/develop/
```

配置环境变量

```bash
echo 'export PATH="$HOME/develop/flutter/bin:$PATH"' >> ~/.zshrc
```

## 检查依赖

```Bash
source ~/.zshrc
```

```Bash
flutter doctor
```
正确输出如下

```Bash
➜  ~ flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.38.4, on Fedora Linux 43 (Workstation Edition) 6.17.9-300.fc43.x86_64, locale en_US.UTF-8)
[✓] Android toolchain - develop for Android devices (Android SDK version 36.1.0)
[✓] Chrome - develop for the web
[✓] Linux toolchain - develop for Linux desktop
[✓] Connected device (2 available)
[✓] Network resources

• No issues found!
```

## 常见错误

```Bash
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 3.38.4, on Fedora Linux 43 (Workstation Edition) 6.17.9-300.fc43.x86_64, locale en_US.UTF-8)
[!] Android toolchain - develop for Android devices (Android SDK version 36.1.0)
    ! Some Android licenses not accepted. To resolve this, run: flutter doctor --android-licenses
[✗] Chrome - develop for the web (Cannot find Chrome executable at google-chrome)
    ! Cannot find Chrome. Try setting CHROME_EXECUTABLE to a Chrome executable.
[✗] Linux toolchain - develop for Linux desktop
    ✗ clang++ is required for Linux development.
      It is likely available from your distribution (e.g.: apt install clang), or can be downloaded from https://releases.llvm.org/
    ✗ CMake is required for Linux development.
      It is likely available from your distribution (e.g.: apt install cmake), or can be downloaded from https://cmake.org/download/
    ✗ ninja is required for Linux development.
      It is likely available from your distribution (e.g.: apt install ninja-build), or can be downloaded from
      https://github.com/ninja-build/ninja/releases
    ✗ GTK 3.0 development libraries are required for Linux development.
      They are likely available from your distribution (e.g.: apt install libgtk-3-dev)
    ! Unable to access driver information using 'eglinfo'.
      It is likely available from your distribution (e.g.: apt install mesa-utils)
[✓] Connected device (1 available)
[✓] Network resources
```

同意Android开发协议

```Bash
flutter doctor --android-licenses
```

安装依赖

<tabs>
<tab title="Fedora 43">
<code-block lang="bash">
sudo dnf install clang cmake ninja-build gtk3-devel egl-utils
</code-block>
</tab>
<tab title="ubuntu">
<code-block lang="bash">
sudo apt install clang cmake ninja-build libgtk-3-dev mesa-utils
</code-block>
</tab>
</tabs>

假如你的 **GoogleChrome** 浏览器是通过 **FlatHub** 安装的， 可以使用以下方式设置 **CHROME_EXECUTABLE** 变量

```bash
echo 'export CHROME_EXECUTABLE="/var/lib/flatpak/exports/bin/com.google.Chrome"' >> ~/.zshrc
```