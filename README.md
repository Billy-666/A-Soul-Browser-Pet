<div align="center">
	<h1>A-Soul 浏览器宠物</h1>
    <em>A-Soul Browser Pet</em>
    <p>在浏览器里养一只A-Soul成员当宠物</p>
    <img src="./images/image0.png" width="80%" />
</div>

## 🔰 安装方法

> 此扩展为“稀土掘金2022编程挑战赛”比赛作品

Chrome 浏览器：

1. 进入**设置/扩展程序**
2. 启用右上角 **“开发者模式”**
3. 点击 **“加载已解压的扩展程序”**，选择项目下的src目录

## 🏓 使用说明

打开任意网页，即可看到一只可爱小然出现在你的页面上。

> 她能陪你一起读文献、刷视频、看直播，还能够与你互动，帮你收集语料，提醒你按时休息。

<img src="./images/image1.jpg" width="80%" />

#### 互动方式：

* **拖拽**：小然会跟随鼠标改变位置并变换表情；
* **点击**：小然会变换不同的表情，并且弹出随机预设语句；
* **跟随鼠标**：小然会不断跟随鼠标位置；
* **跟随点击**：小然会追逐最近点击鼠标的位置；

#### 附加功能：

* **拖拽收藏**：将链接/图片/选中文字拖拽到小然身上，她会为你保存起来；
* **管理收藏**: 点击拓展按钮，可以在弹出页内打开/复制/删除收藏内容；

#### 自定义配置：

除了小然，还有其他四位A-Soul成员可以配置，点击扩展按钮，在弹出框中进行配置。

<img src="./images/image2.jpg" width="80%" />

* **诱饵**：每位成员都对应着不同的诱饵，会在点击鼠标后展示； *（可能会影响正常点击）*
* **收藏**：开启后，可以使用拖拽收藏功能；
* **速度**：成员追踪鼠标/追踪点击位置时的速度；

## 🚚 开发相关

#### 开发周期与技术栈：

本拓展开发周期为7天，迭代三个版本，初版实现了基本的功能与交互，第二版增加了收藏功能与更丰富的交互细节，第三版将B站装扮表情包替换为了微信表情包，并对代码进行了优化。

项目使用 *jQuery* + *MDUI* + *Anime.js* 完成，*jQuery* 用于替代原生 DOM 操作，更方便的操作元素属性、添加与解除监听器；*MDUI* 用于构建弹窗配置页的界面， *Anime.js* 用于辅助实现人物角色动作的过渡动画。

#### 项目结构：

```text
src
 ├── background.js    // service_worker脚本
 ├── css              // 存储样式文件
 ├── index.js         // 注入页面的content_scripts脚本
 ├── lib              // 依赖的外部库
 ├── manifest.json    // Chrome 扩展的描述文件
 ├── popup.html       // 弹窗页的.html文件
 ├── popup.js         // 弹窗页的.js文件
 └── static           // 存储静态文件如图片、图标等
```

#### 测试用例：

测试环境：Google Chrome 100.0.4896.88 (正式版本) （64 位）

针对部分网页场景，挑选了以下网站运行测试，拓展能够完整并且正确运行：

* [掘金首页](https://juejin.cn/)
* [掘金个人主页](https://juejin.cn/user/4420463502826087)
* [比赛官网](https://hackathon2022.juejin.cn/)

## 🙆‍♂️ 参赛感想

这是我第一次开发Chrome拓展，说起来和掘金的缘分很巧妙，正是因为这次与A-Soul联名的比赛我才了解到掘金这个优秀技术社区，相比于其他社区浮躁的氛围，掘金社区让我真正感受到技术人们分享、交流技术的初衷，开发过程中社区的优质内容也给了我很多帮助。

说起来，*jQuery* 已经是很古早的技术了，我的初衷是将涉及到界面的部分交给现代化的框架比如 *Vue* 来实现，遗憾的是，由于谷歌的安全限制，导致动态渲染的模板必须在`sandbox`环境中运行，而`sandbox`中的脚本又无法调用Chrome API ，一番探求无果后，我仍然选择了 *jQuery* 开发界面，如果后续还有机会迭代的话，这一定是优先要考虑重构的地方。

比赛虽然结束，但是技术始终在发展，技术人也应该随时准备学习新知识，正是所谓：流水不腐，户枢不蠹。希望这次比赛能成为我自学前端路上的一个记号，把握好每个机会，不断学习，无限进步！

## 🔗 相关链接

[Github主页 ](https://github.com/ZiuChen) [CSDN博客](https://blog.csdn.net/Huuc6)  [掘金主页](https://juejin.cn/user/4420463502826087)