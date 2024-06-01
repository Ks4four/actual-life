---
title: 分体键盘的入门参考
description: 买分体键盘的你需要考虑什么
slug: split-keyboard
date: 2024-04-22
image: split-keyboard.jpg
categories:
  - 文档
tags:
  - 键盘
  - 文档
  - 中文
weight: 1
---

由于各种各样的原因，你开始考虑买一个分体键盘。然后你可能会在网上搜索，或者经朋友推荐等等，来到这篇参考。

作者写这篇参考的初衷是让人们不再对分体键盘陌生。国内讨论分体键盘的内容较少，因此作者打算列一个简单的总结。这也算是对喜欢新奇的人作出一点贡献，毕竟他们可能厌烦国内的某些老旧软件和硬件，想要尝试点新东西。这篇参考自然也包括了在 reddit 上[人体工程学键盘](https://www.reddit.com/r/ErgoMechKeyboards/)分区的较新内容。

这篇参考默认你已经知道[**标准指法**](https://sspai.com/post/45721)，不过你不需要掌握得很熟练，只需要了解就可以了。但是如果你真的要准备买来用，那么你就只能学习了。

## 软、硬件的选择

### 软硬件之间：VIA 还是 VIAL

这篇参考讨论有线键盘，而且它的方案是 QMK。

QMK 是一种固件，能全权操控键盘，但是如果直接用它，需要写 C 语言的代码。不过，如果你不对键盘本身追求高级功能，只要能看懂代码，然后看官方文档，知道哪一个键代表什么；接着复制粘贴到对应的位置，这就足够了。虽然是这样，你写完代码了，它还要自己编译出来固件，然后你还要自己刷入到键盘里。所以直接编辑固件是很麻烦的。如果你需要，这是 [QMK 的主页](https://docs.qmk.fm/#/)。

大多数人只需要会使用 VIA。VIA 提供了界面去操控 QMK 的键盘，就像许多键盘的“驱动”界面一样。VIA 不算是软件，所以可以不用下载，能在浏览器上直接使用，但是它需要浏览器支持 WebHID。支持的浏览器包括 Chromium 系，比如 Chrome 以及自带的 Edge。也就是说，**火狐是不行的**。你可以在 [VIA 的主页](https://www.caniusevia.com/) 里点击里面的 “Start Now”，或者直接收藏[它的网址](https://usevia.app/)来实时操控键盘。

除此之外，还有一个界面叫 VIAL。VIAL 的功能更多，所以使用的存储内存比 VIA 多。每个键盘都会有一个主控，这个主控就像 CPU；这个“CPU”的存储内存是固定的，它直接决定了你能不能使用 VIAL，以及使用它到什么程度。你可以从 [VIAL 的主页](https://get.vial.today/)里看到它的软件的截图。对于 VIAL，我更推荐下载它的软件，因为网页有可能有奇奇怪怪的问题。

你可能会问，[那么，无线呢？](#那么无线呢)对广大的无线爱好者，后文也提出了为什么在这里不讨论无线；不过这里先说键盘的硬件问题。

### 硬件：选择轴种类

- 普通机械轴键盘。一般选的都是普通机械轴，因为很多人都希望能用之前键盘上的轴体。
- 矮轴键盘。为了极端的便携性或者短键程可以选择这个。
  - 目前矮轴轴体还没有能静音的。如果你需要静音，那么可以直接排除矮轴键盘。

### 硬件：选择按键设计

键盘的按键设计有平面和曲面的。一般的人都会先选择平面，这能让他们尽快适应新键盘。曲面键盘不建议没用过平面的人选，因为首先是贵，其次它的造型是立体的，比平面更难适应。

你可以把按键设计的规格参数打印在纸上，然后感受一下这个设计是否适合你的手。有人就做了这样的网站，收集了不同设计的规格参数，用来对比不同的分体键盘按键设计。如果你好奇，可以看看[分体键盘设计对比](https://compare.splitkb.com/)。

如果你需要大众认可的设计，可以先参考[分体键盘社区介绍的东西](https://www.reddit.com/r/ErgoMechKeyboards/comments/cz24cg/github_diimdeepawesomesplitkeyboards_a_collection/)。如果你需要一个大合集，或者你根本就没有想买分体键盘，只是为了看看实物，可以搜索关键词“split keyboards database”之类的东西。

在国内，出名才有出货量，有出货量才会便宜。所以，这里只会列出几种选择：

- 平面
  1. [corne](https://github.com/foostan/crkbd/) 是外网很经典的设计；它虽然没有数字键，但是也有很多中国人用；
  2. [sofle](https://josefadamcik.github.io/SofleKeyboard/) 比较像 corne，不过有一排数字键；
- 曲面
  1. [Dactyl](https://github.com/adereth/dactyl-keyboard)以及类似它的设计；
  2. [Charybdis](https://bastardkb.com/charybdis/)由 BastardKB 设计，特点是带轨迹球，让人使用键盘时不用松开手去摸鼠标。

也有厂商自己设计了配列，以下出名的（你在闲鱼能买到的）全部都支持 QMK 固件：

- [Ergodox EZ](https://ergodox-ez.com/)：老牌，可调整体的高低，是一个平面键盘。被人指责拇指键安排不合理，以及键帽比较难买。_不建议购买这个，大势已去；_
- [ZSA Moonlander](https://www.zsa.io/moonlander/)：新兴设计，可以分别调主键位高低和拇指键的高低；
- [MoErgo Glove80](https://www.moergo.com/collections/glove80-keyboards)：目前还是最受欢迎的矮轴曲面键盘。

### 软件：选择映射参考

_（此处忽略了键盘的布局，因为我默认大家都使用 `QWERTY`。）_

“**映射**”的是键盘的某个键按下时，电脑会发生什么。它说明了你操控电脑的方式，包括你打字的方式。[^1]

[^1]: 在英文里，按照直译，它应该是 keymaps，不过目前大家都更喜欢用 layout 这个词。它们的区别就是 keymap 不一定要有真的实体键盘，而 layout 一定要有。比如，游戏里的“前进”设为 `W` 键，“向左走”设为 `E` 键等等，就是没有把键映射到键盘，而只是映射到“前进”和“向左走”的行为上，这种就是 keymap。如果把 `W` 键、`E` 键等等映射到键盘的按键上，那就是 layout。

映射不仅包括你现在看到的所有按键，还有别的键（比如 `F1` 键）在别的“**层**”（layer）下。你需要按下对应的键让键盘激活对应的层才能打出这些按键。

映射有以下三种类别，是根据操控 mod 键的方式不同而分类的。Mod 键（modifiers、有时译作修改键）通常来说指的是 Ctrl、Alt、GUI 和 Shift 和它们的组合。

- GUI 在 Windows 系统下是 `Windows` 键，在 MacOS 系统下是 `Command` 键；有时也称 `Meta`；
- Mods 的组合其实就是一个信号。比如，在 Windows 系统中，按下 `Ctrl` 和 `C` 键时，键盘就会发送 `Ctrl+C`，电脑收到时就会计算出一个键值，然后执行相应的操作（一般是 `复制`）。

以下举例的映射应该是作为参考的，可以根据自己的使用习惯进行调整。我推荐先参考 [**Miryoku**](https://github.com/manna-harbour/miryoku/tree/master/docs/reference)。

#### **Home row mods**

Home row 指的是 `ASDF…JKL;` 这一排。

**Home row mods** 指的是是用你的手指默认放的位置（左手手指在 `ASDF`，而右手手指在 `JKL;`）来按 mod 键。

这一类映射全部都使用到 mod-tap 功能。这个功能的意思是：你在普通按按键时，电脑会输入一个键，而长按时又会激活别的键。

- [**Miryoku**](https://github.com/manna-harbour/miryoku/tree/master/docs/reference) 是整个社区最出名的代表
  - 要求 3x5 加 3 个拇指键；
  - 原版最出名，最多人用，适合大多数人用；
  - 即使不使用原版的 Colemak Mod-DH 配列，使用 QWERTY 也能用，照抄其他的 layers 就行；
  - 磨合期比下面提到的 One shot mods 更长。

#### **One shot mods**

mod-tap 功能有一个缺点是延迟较大或不稳定时容易误触。  
比如，社区的人在使用原版 Miryoku 时，发现很容易把 `A` 键按得稍微长一点点，这样就触发了 `Windows 键`。为了避免误触，社区的人有两种选择，要么调高 QMK 的长按时间（默认是 200 ms），但是那样就会拖慢了操作速度；要么不用 mod-tap，只用 layers，就像很多键盘的 `FN` 键 一样。有些人就是这么做的：

- [**callum**](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum)
    - 完全没有 mod-tap；
    - 要求 3x5 加 2 个拇指键。
- [**seniply**](https://stevep99.github.io/seniply/)

大部分人看到这里都会选择 **Home row mods** 和 **One shot mods** 其中之一。

#### **Combo mods**

Combo 一般译成组合键。组合键的意思是在一定时间内同时按下多个键。
**Combo mods** 指的是按下多个键来触发 mod 键。
这部分给的是比 3x5 小的键盘用的，算是给以上映射一个「突破」。这部分的映射最难熟练，因为前面两个部分最多只用到了 layer 和 combo，这里用了更高阶的功能。  

- [rafaelromao](https://github.com/rafaelromao/keyboards)
  - 总共仅要求 24 个键。
  - 令人畏惧的[功能数量](https://github.com/rafaelromao/keyboards?tab=readme-ov-file#main-features)，没有相关需求根本看不懂；没有 QMK 相关知识也看不懂。
  - 可以使用 [Home Block Mods](https://precondition.github.io/home-row-mods#alternative-home-row-mods-layout) 来替代 **Home row mods**，比如用拇指按住 `V` 键或 `M` 键来进行 combo（原版是按下 `C` 键和 `P` 键形成 `Ctrl` ）。
- [Jason Cox](https://jasoncarloscox.com/blog/combo-mods/)
  - 不是具体的映射，只是提供了一个想法。

## 开始使用

当你选好了键位参考之后，再自己调整一遍，就可以开始使用了。

- 大部分英语母语者都报告说，自己要一个月才能适应分体键盘；
- 分体键盘肯定需要记忆每一层 layer 来形成肌肉记忆的。在这期间，你可以用便利贴把所有 layer 和 combo 写下来，贴在电脑屏幕的下方。

加油。

### 那么，无线呢？

无线方案目前仅有 [ZMK](https://zmk.dev/)，而且它不太成熟。根据我自己的情况，它有两个很明显的缺点：

- 轨迹球反应不稳定；
- 延迟大，进而影响的是关于长按的功能。（比如，Vial 里有一个 combo 的功能，就是同时按两个键触发另外一个键，如果延迟大或者不稳定，那么你没办法依赖这个功能）

目前大部分的商业产品都是有线的（[Ergodox EZ](https://ergodox-ez.com/)、[ZSA Moonlander](https://www.zsa.io/moonlander/) 和 [MoErgo Glove80](https://www.moergo.com/pages/glove80-product-details)）。

不过，如果你只使用 Layers，它的延迟问题倒是没那么严重；加上大多数人都不太会加上轨迹球，所以 ZMK 还是可以在使用 QMK 之后尝试的。

## 个人看法

- 不要考虑非分体键盘：
  - 不要听信普通斜列键盘说的「人体工程学」，那和「i9 级电脑」没差别；分体的斜列也不好，比如 [mistel 做的分体键盘](https://mistelkeyboard.com/)；
  - 不要听信 Alice 配列，有钱有时间的可以试试。反正没用；
  - 微软那几个键盘甚至都没有「层」设定；
  - 有些键帽的介绍会写自己是符合人体工程学，这种硬加一个标签的介绍非常搞笑。
- 身体不适才**需要**分体键盘。
- 如果身体没有不适，请等待它不适：
  - 用更好的工具不会让你更健康，只会让你没有那么快变烂；
  - 如果有多余的钱和多余的时间，那可以考虑分体键盘。比如，你需要 800 元才能购置一个键盘；这个键盘的磨合期还不会干扰到你的正常工作；
- 不要考虑不带有 QMK （或者 ZMK、VIA、VIAL）的键盘。软件当然可以做到它们的效果，不过很麻烦。

有些工作岗位不能携带你们自己的键盘，这种情况下只能用软件（如 [KMonad](https://github.com/kmonad/kmonad)）来弥补普通斜列键盘带来的缺陷。如果电脑不能下第三方软件，祝你们好运。

---

**2024-06-02 更新 layer 的解释**

**2024-05-31 超链、语法**

超链改为更好的标题，以及语法修正

**2024-05-10 迁移到 Hugo**

调整了标点符号

**2024-05-02 调整**

调整了无线部分到后面。  
解决了一些语法问题。

**2024-04-22 第一次发布**
