# 欢迎参与翻译与改进！

## 如何编译本书的pdf版？
### 1. 环境
TEX系统：笔者使用完整安装的TeX Live 2019。建议使用不低于2019的版本，自动配置一劳永逸。

Windows系统推荐：https://tug.org/texlive

Mac系统建议使用MacTex：https://www.tug.org/mactex

Git：编译脚本含有Git命令，所以必须安装[Git](https://git-scm.com)。
### 2. 拉取仓库
选取一合适的工作目录，拉取本书仓库：
```cmd
git clone https://github.com/kanition/pbrtbook.git
```
### 3. 字体
为了方便管理以及降低仓库大小，本书的字体并不包含在仓库中。在成功拉取文件后请创建一个名为`fonts`的新文件夹并将以下**5种**字体添加进`fonts`内。注意保留字体的原有文件名。

```cmd
cd .\pbrtbook
mkdir .\fonts
```

#### 思源字体
本书中文字体主要使用免费开源的[思源宋体](https://github.com/adobe-fonts/source-han-serif)和[思源黑体](https://github.com/adobe-fonts/source-han-sans)。

- https://raw.githubusercontent.com/adobe-fonts/source-han-sans/release/OTF/SimplifiedChinese/SourceHanSansSC-Bold.otf
- https://raw.githubusercontent.com/adobe-fonts/source-han-sans/release/OTF/SimplifiedChinese/SourceHanSansSC-Regular.otf
- https://raw.githubusercontent.com/adobe-fonts/source-han-serif/release/OTF/SimplifiedChinese/SourceHanSerifSC-Bold.otf
- https://raw.githubusercontent.com/adobe-fonts/source-han-serif/release/OTF/SimplifiedChinese/SourceHanSerifSC-Regular.otf

#### 楷体
除此之外，本书还使用了Windows上自带的中易楷体(SimKai)。

中文版Windows用户：执行如下命令将其复制到fonts文件夹下；
```cmd
copy %windir%\Fonts\simkai.ttf .\fonts\
```
非Windows用户：需要自行搜索并下载到fonts文件夹下。

### 4. 编译
执行工作根目录下的编译脚本，它使用xelatex编译：
#### Windows
```cmd
.\cp.cmd
```

#### Mac/Linux
```cmd
chmod +x cp.sh
./cp.sh
```
