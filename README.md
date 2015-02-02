
# Rime 配置说明

[Rime](http://code.google.com/p/rimeime/) 输入法是一款适用于 Mac OSX, Linux,
Windows 的输入法，Rime 在不同平台下的对应名称如下：

* Mac OSX: 鼠鬚管([Squirrel](https://github.com/lotem/squirrel))
    配置目录：`~/Library/Rime/`
* Linux: 中州韻(ibus-rime)
    配置目录：`~/.config/ibus/rime/`
* Windows: 小狼毫(Weasel)
    配置目录：`%APPDATA%\Rime`

Rime 的配置文件不同平台的放置在不同的目录，
在配置目录中，主要使用 `yaml` 进行配置。
目录中自有的配置文件不建议直接修改，因为可能会被自动复写。
用户配置一般以原始配置文件名增加 .custom 二级后缀的方式，
例如：Mac OSX 下的原始配置 `squirrel.yaml`，对应的用户配置就是
`squirrel.custom.yaml` 文件。

修改 `.custom` 配置后，『重新部署』Rime 输入法会将用户的配置增加或更新到
对应的原始配置中。

## 安裝

```
$ git clone git@github.com:hotoo/rime.git
$ cd rime
$ make install
```

## 卸載

```
$ cd rime
$ make uninstall
```

## 同步

installation.yaml

```yaml
installation_id: "hotoo.rmbp"
sync_dir: "/Users/hotoo/Dropbox/RimeSync"
```
windows上面，sync_dic最好用单引号或者不用引号，否则用双反斜线'\\\\'表示'\'。
```yaml
installation_id: "yantze"
sync_dir: 'D:\Work\dropbox\Apps\RimeSync'
```
字典的同步是双向合并
配置的同步是单向的同步,即由"用户文件夹"指向"同步文件夹"

## 一些快捷键

输入的时候删除一个音节
```
⌃ + BackSpace 或 ⇧ + BackSpace
```
从用户词典中删除误上屏的错词
```
Shift + Fn + Delete
```
Emacs 风格的编辑键
```
↑：⌃ + p
↓：⌃ + n
←：⌃ + b
→：⌃ + f
上页：⌥ + v
下页：⌃ + v
句首：⌃ + a
句末：⌃ + e
回退：⌃ + h
刪除：⌃ + d
清空：⌃ + g
```

## 参考
* [安装及配置 Mac 上的 Rime 输入法](http://www.dreamxu.com/install-config-squirrel/)
* [致第一次安装 RIME 的你之修订版](http://tieba.baidu.com/p/3288634121)
* [Rime 定製指南](http://code.google.com/p/rimeime/wiki/CustomizationGuide)
* [中州韵（小狼毫，鼠须管）输入法设置](http://blog.yesmryang.net/rime-setting/)
* [說明書#同步用戶資料](https://code.google.com/p/rimeime/wiki/UserGuide#同步用戶資料)
* [Author:佛振(lotem)@github](https://github.com/lotem)
* [如何从QIM迁移至Squirrel（鼠鬚管）](http://cocoabob.net/?p=919)
