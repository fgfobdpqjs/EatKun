<p align="center">
  <a href="https://chicxk.pages.dev/"><img src="static/image/ClickBefore.png" width="100" height="100" alt="吃掉蔡徐坤"></a>
</p>
<div align="center">

# 吃掉蔡徐坤

_🦌 网页小游戏 🥛_

</div>


## 简介

小游戏：吃掉蔡徐坤

最新版本号：0.0.3f1

[English](README_EN.md)
|
[Github](https://github.com/EatKun)
|
[游玩](https://chicxk.pages.dev/)
|
[最新 Build](https://OneSitos.github.io/EatKun/index.html)
|
[Releases](https://github.com/OneSitos/EatKun/releases)

## 可选功能

简易排行榜（日/周/月）不推荐使用。

不需要排行榜把 php/sql 文件都删掉即可。

## 版本需求

+ MySQL 5+
+ PHP 5+

## 免责声明

本游戏与蔡徐坤本人及其经纪团队无任何关联，仅供娱乐。

`static/image`、`static/music`内容来自[爱给网](https://www.aigei.com/s?q=%E8%94%A1%E5%BE%90%E5%9D%A4&type=sound)，若侵权可在 [Issues](https://github.com/EatKun/EatKun/issues) 联系删除，并附上`delete`标签。

## 使用方法

注: 如果你想玩的话直接[去玩](https://chicxk.pages.dev/)就可以，这里是如何创建你的改版。

### Github Pages

点[这里](https://www.bilibili.com/video/BV1r94y1d765)看视频步骤。

如果你不需要排行榜，那么部署到 Github Pages 即可。

按照如下方法更改你想要显示的文字。

1. **Fork本项目，不要在现在这个页面直接改，然后发现改不了。**

2. **打开你Fork的项目**，找到`static/i18n/zh.json`，找到下面这几项配置：

   ```json
   {
     "game-title": "新概念音游",
     "game-intro1": "从最底下的开始",
     "game-intro2": "看你能得多少分",
     "game-intro3": "OK!",
     "game-intro4": "蔡徐坤一个不留！",
     "text-level-1": "试着好好练个两年半?",
     "text-level-2": "还没到蔡徐坤的程度!",
     "text-level-3": "马上就要超过蔡徐坤的程度!",
     "text-level-4": "你应该已经练了两年半了吧!",
     "text-level-5": "蔡徐坤:又有一位IKUN加入我们的荔枝集团了!"
   }
   ```

   你可以随意更改右侧文字，就可以显示你想要的内容，**不要删掉双引号**！

3. 找到`static/image`文件夹，点击前显示的图片是`ClickBefore.png`, 点击后的图片是`ClickAfter.png`，把他们改成你想要的即可。

   **注意文件格式, 需要是png**

4. 找到`static/music`文件夹，点击时的音效是`tap.mp3`，正常结束的音效是`end.mp3`，点击错误的音效是`err.mp3`，把他们改成你想要的即可。

   **注意文件格式, 需要是mp3**

5. 更改完毕后前往项目的`Settings` -> `Pages` -> `Source`，选择`main` 分支然后点击`Save`。

### 部署到服务器

按照这些步骤来在你的服务器上配置排行榜的数据库。

1. 将`index.js`的username0中的0去掉，message0中的0去掉，`index.php`中的username0中的0去掉，message0中的0去掉。

2. 创建数据库并且执行提供的脚本（这里用`kun`作为数据库名）：
   ```sql
   CREATE DATABASE kun DEFAULT CHARSET=utf8;
   USE kun;
   SOURCE kun.sql;
   ```

3. 更改有数据库信息的`conn.php`为你的数据库配置：

   ```php
   <?php
   // 把这里改为你的配置
   $link = new mysqli('localhost','NAME','PASSWORD','kun');
   mysqli_set_charset($link, 'utf8');
   if ($link->connect_error) {
       die("Failed to connect: " . $conn->connect_error);
   }
   $ranking = "kun_rank";
   ```

## 使用的项目及其许可证

1. EatKano ([网站](https://xingye.me/game/eatkano) [GitHub](https://github.com/arcxingye/EatKano) [许可证：MIT license](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/files/license/github.arcxingye.EatKano_LICENSE.txt))

2. EatCat ([GitHub](https://github.com/122440367/eatcat) 许可证：未知)

3. EatCat ([GitHub](https://github.com/Webpage-gh/eatcat) [许可证：Apache License 2.0](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/files/license/github.Webpage-gh.eatcat_LICENSE.txt))

4. Bootstrap v5.1.1 ([网站](https://getbootstrap.com/) [GitHub](https://github.com/twbs/bootstrap/releases/tag/v5.1.1) [许可证：MIT license](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/files/license/github.twbs.bootstrap_LICENSE.txt))

5. CREATEJS v1.0.0 ([网站](http://createjs.com/) [GitHub](https://github.com/CreateJS/CreateJS) [许可证：MIT license](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/files/license/github.CreateJS.CreateJS_LICENSE.txt))

6. jQuery 3.6.0 ([网站](https://jquery.com/) [GitHub](https://github.com/jquery/jquery/releases/tag/3.6.0) [许可证](https://raw.githubusercontent.com/EatKun/EatKun/refs/heads/main/files/license/github.jquery.jquery_LICENSE.txt))

7. JSEncrypt ([网站](https://travistidwell.com/jsencrypt) [GitHub](https://github.com/travist/jsencrypt) [许可证](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/files/license/github.travist.jsencrypt_LICENSE.txt))

## Star 统计

[![Stargazers over time](https://starchart.cc/OneSitos/EatKun.svg?variant=adaptive)](https://starchart.cc/OneSitos/EatKun)

## 其它事项

此项目使用 [MIT License](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/LICENSE-code) 进行授权，在使用本项目时，请标注来源/原作者。

`README.md`、`README_EN.md`和本项目 [Wiki](https://github.com/OneSitos/EatKun/wiki)（现在没有，未来可能会有）使用 [Creative Commons Attribution 4.0 International Public License](https://raw.githubusercontent.com/OneSitos/EatKun/refs/heads/main/LICENSE-text) 进行授权，在使用本项目时，请标注来源/原作者。