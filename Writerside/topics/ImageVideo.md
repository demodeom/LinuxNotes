# 图片、视频、音乐

## 截图

### Flameshot

```
flatpak install flathub org.flameshot.Flameshot
```

添加权限
```
flatpak permission-set screenshot screenshot org.flameshot.Flameshot yes
```

测试是否正常
```
flatpak run --command=flameshot org.flameshot.Flameshot gui
```

## 视频播放器

### mpv

```
flatpak install flathub io.mpv.Mpv
```

## 音乐

### QQ音乐 {id="qq_music"}

```
flatpak install flathub com.qq.QQmusic
```

### 网易云音乐

```
flatpak install flathub com.netease.CloudMusic
```

```
flatpak install flathub com.github.gmg137.netease-cloud-music-gtk
```

### LX Music Desktop

```
flatpak install flathub cn.toside.lxmusic.lx-music-desktop
```

### Amberol

```
flatpak install flathub io.bassi.Amberol
```