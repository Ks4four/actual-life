---
title: 分体键盘选择参考
description: 给需要买分体键盘的人指明方向
slug: split-keyboard
date: 2022-03-06 00:00:00+0000
# image: cover.jpg
categories:
    - 键盘
tags:
    - 键盘
    - 中文
    - 文档
weight: 1       # You can add weight to some posts to override the default sorting (date descending)
---

由于各种各样的原因，你开始考虑买一个分体键盘。

_这个心得默认所有读者已经知道[**标准指法**](https://sspai.com/post/45721)，但不需要掌握得很熟练。_

> 个人看法：
> 
> - 不要考虑非分体键盘。
>     - 不要听信普通斜列键盘说的「人体工程学」，那和「i9 级电脑」没差别。
>     - 不要听信 Alice 配列，有钱有时间的可以试试。反正没用。
>     - 微软那几个键盘甚至都没有「层」设定。
>     - 有些键帽的介绍会写自己是符合人体工程学，这种硬加一个标签的介绍非常搞笑。
> - 身体不适才**需要**分体键盘。
> - 如果身体没有不适，请等待它不适。
>     - 用更好的工具不会让你更健康，只会让你没有那么快变烂。
>     - 如果有**多余**的钱和**多余**的时间，那_可以考虑_分体键盘。比如，你需要 800 元才能购置一个键盘；这个键盘的磨合期不会干扰到你的正常工作.
> - 不要考虑不带有 qmk （或者 zmk、via、vial）的键盘。软件当然可以做到它们的效果，不过很麻烦。

有些工作岗位不能携带你们自己的键盘，这种情况下只能用软件（如 [KMonad](https://github.com/kmonad/kmonad)）来弥补普通斜列键盘带来的缺陷。如果电脑不能下第三方软件，祝你们好运。

轴体在中国变得越来越火，种类也越来越多，在这里没有必要介绍「红蓝茶青」这种内容。

## 选择你的英雄

这篇心得主要讨论有线（方案是 [QMK](https://docs.qmk.fm/#/)）键盘。

- QMK 是固件方案，能全权操控键盘，但是改键需要写代码；而大多数人只需要使用 [ViaL](https://get.vial.today/) 操作就够了。ViaL 相当于给了一个界面去操控它。
    - ViaL 可以不用下载，在支持「WebHID」的浏览器（例如 Chromium 系，比如 Chrome 以及自带的 Edge）上[直接使用](https://vial.rocks/)。**火狐是不行的。**
    - 你可能听说过 VIA。VIA 是最早能操作 QMK 键盘的，但是 ViaL 功能更强，而且对于卖家来说就是刷一个固件的事情（前提是固件开源）；在这里不推荐。
- [那么，无线呢？](#那么无线呢)

### 1. 选择轴种类

- 普通机械轴键盘。_一般选的都是这个。_
- 矮轴键盘。为了极端的便携性或者短键程可以选择这个。
    - 目前（2024-04）矮轴键盘没有能静音的。如果你需要静音，直接排除矮轴键盘。

### 2. 选择设计

- 平面
    1. 最火的是 [corne](https://github.com/foostan/crkbd/)（没有数字键但是很多中国人用）
    2. 其次是 [sofle](https://josefadamcik.github.io/SofleKeyboard/)（比较推荐新手用，因为有数字键）
    3. 然后是 [lily58](https://github.com/kata0510/Lily58)
- 曲面（不建议没用过平面的人选，因为贵）
    1. 之前火的是 [Dactyl](https://github.com/adereth/dactyl-keyboard)
    2. BastardKB 旗下的 [Charybdis](https://bastardkb.com/charybdis/)，带轨迹球

也有一些厂商自己做了配列，以下出名的全部都支持 QMK 固件：

- [Ergodox EZ](https://ergodox-ez.com/)：老牌，可调整体的高低，是一个平面键盘
- [ZSA Moonlander](https://www.zsa.io/moonlander/)：新兴，可以分别调主键位高低和拇指键的高低
- [MoErgo Glove80](https://www.moergo.com/collections/glove80-keyboards)：最受欢迎的矮轴曲面键盘

### 3. 选择映射（Keymaps）参考

（_此处忽略了键盘的[[split-keyboard-glossary|布局]]，因为我默认大家都使用 `QWERTY`。_）

[[split-keyboard-glossary#Keymaps 「映射」|映射]] 指的是你操控电脑的方式，包括你打字的方式（Layout 仅指的你打字的方式）。

映射有以下三种类别，是根据操控 mod 键的方式不同而分类的。Mods （modifiers）通常来说指的是 Ctrl、Alt、GUI和Shift和它们的组合。

- GUI 在 Windows 下是 `Windows` 键，在 MacOS 下是 `Command` 键，有时称 `Meta`）
- Mods 的组合其实就是一个信号。比如，按下`Ctrl`和`C`键时，键盘就会发送`Ctrl+C`，电脑收到时就会计算出一个键值，然后执行相应的操作（一般是`复制`）。

以下映射应该是作为参考的，不用照抄，根据自己的使用习惯调整就好。我推荐先参考 [**Miryoku**](https://github.com/manna-harbour/miryoku/tree/master/docs/reference)。

#### **Home row mods**

_Home row 指的是 `ASDF…JKL;` 这一排。_  
Home row mods 的思想是用你的手指默认放的位置（左手手指在 `ASDF`，而右手手指在 `JKL;`）来按 mod 键。这一类映射全部都使用 mod-tap 功能，就是普通按按键时输入字母区，而长按时激活相应的键。

- [Miryoku](https://github.com/manna-harbour/miryoku/tree/master/docs/reference)
    - 要求 3x5 加 3 个拇指键
    - 原版最火，最多人用，适合大多数人用
    - 即使不使用 home row mods 也能流畅使用（比如，把拇指键其中之一改成 `Shift` 键）
    - 即使不使用原版的 Colemak Mod-DH 配列，使用 QWERTY 也能用，照抄其他的 layers 就行
    - 磨合期比下面提到的 One shot mods 更长

#### **One shot mods**

Mod-tap 功能有一个缺点是延迟较大或不稳定时容易误触。  
比如，在你使用原版 Miryoku 时，

- 可能会抱怨 miryoku 的 shift 键没有摆在 base layer，因为 shift 实在是太常用了。
- 或者你很容易把 `A` 键按得稍微长一点点，这样就触发了 `Windows 键`。所以，要么你就调高 QMK 的长按时间（默认是 200 ms），但是那样就会拖慢你的操作速度，要么你就不用 mod-tap，只用 layers，就像很多键盘的 `FN` 键 一样。

有些人就会这么做：

- [callum](https://github.com/callum-oakley/qmk_firmware/tree/master/users/callum)
    - 要求 3x5 加 2 个拇指键
- [seniply](https://stevep99.github.io/seniply/)

大部分人看到这里都会选择 **Home row mods** 和 **One shot mods** 其中之一。

#### **Combo mods**

这部分给的是比 3x5 小的键盘用的，算是给以上映射一个「突破」。这部分的映射最难熟练，因为前面两个部分最多只用到了 layer 和 combo，这里用了更高阶的功能。  
Combo mods 指的是按下多个键来触发 mod 键。

- [rafaelromao](https://github.com/rafaelromao/keyboards)
    - 总共仅要求 24 个键
    - 令人畏惧的[功能数量](https://github.com/rafaelromao/keyboards?tab=readme-ov-file#main-features)，没有相关需求根本看不懂；没有 QMK 相关知识也看不懂
    - 可以使用 [Home Block Mods](https://precondition.github.io/home-row-mods#alternative-home-row-mods-layout) 来替代 **Home row mods**，比如用拇指按住 `V` 键或 `M` 键来进行 combo（原版是按下 `C` 键和 `P` 键形成 `Ctrl` ）
    - 说实话像普通 layer：按一个拇指键，然后再按
- [Jason Cox](https://jasoncarloscox.com/blog/combo-mods/)
    - 不是具体的映射，只是提供了一个想法

## 开始使用

当你选好了键位参考之后，再自己调整一遍，就可以开始使用了。

- 大部分英语母语者都报告说，自己要一个月才能适应分体键盘。

加油。

### 那么，无线呢？

无线方案目前仅有 [ZMK](https://zmk.dev/)，而且它不太成熟。根据我自己的情况，它有两个很明显的缺点：

- 轨迹球反应不稳定
- 延迟大
    - 延迟大影响的是关于长按的功能（比如，Vial 里有一个 combo 的功能，就是同时按两个键触发另外一个键，如果延迟大或者不稳定，那么你没办法依赖这个功能）

目前大部分的商业产品都是有线的（[Ergodox EZ](https://ergodox-ez.com/)、[ZSA Moonlander](https://www.zsa.io/moonlander/) 和 [MoErgo Glove80](https://www.moergo.com/pages/glove80-product-details)）。

不过，如果你只使用 Layers，它的延迟问题倒是没那么严重；加上大多数人都不太会加上轨迹球，所以 ZMK 还是可以胜任的。

---

###### 2024-05-02 调整

调整了无线部分到后面。  
解决了一些语法问题。

###### 2024-04-22 第一次发布