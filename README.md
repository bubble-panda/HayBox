![image](https://github.com/user-attachments/assets/75fb210a-fb80-4a6f-b643-8e18ec4c76b8)# HayBox
## 前言
我不太会用markdown，以下内容均可解压zip文件之后在文档教程中查看。
这是一个比较基础的制作大乱斗BOX设备教程，固件方面使用的时候修改过的Haybox，可以配置多种游戏模式，多重键层。支持PC，Xbox，Nintendo 64，Nintendo Switch等平台，不支持PS平台(需要转换器)。框体方面采用超频A的框体样式，重新设计了图纸，将框体规格改为350*200*35mm。布局上分为两种，一种是20键的B0XX布局，一种是我自己优化的24键布局，两种布局使用的固件不一样，可以按需求选择。
目前做了几种模式，对于传统格斗类，大乱斗类游戏是完全够用的。对于黑神话，艾尔登法环，只狼，甚至FPS类型的游戏，直接用Smash game (Rivals2/Ultimate/Fraymakers)的模式配置就行，用四个右摇杆键转换视角。但由于右摇杆被四个按键分为了四个右摇杆的输出点位，并不是线性的摇杆，在视角转换部分的体验没有手柄来得舒服。更详细的内容会在后面提到， 24键版本的固件是我本人改的。如果在使用过程中遇到了一些问题或者有更好的建议反馈，可以联系我。QQ;2335785076  微信；Bubble-PandaPuff

## 材料清单

要用到的工具：十字螺丝刀，剪刀，绝缘胶带。材料全部都已给出对应商品，扫描商品图片中的二维码可跳转商品页面，也可以自己去其他商家店铺选择同样的商品。街机按键根据个人需求，预算，喜欢来选择，本方案以拳霸24mm轻韧按键为例。（材料清单文件夹中有原图，二维码更清晰）
1.	拳霸24mm轻韧按键25颗（备用1颗）![image](https://github.com/user-attachments/assets/1ab93fe3-6962-48d7-bee4-29739c8a607c)

2.	Micro安卓口转打印方母口线0.3米![image](https://github.com/user-attachments/assets/8610406c-4e65-43b9-ae04-004925b75d7a)

3.	打印机USB数据线1.5米，黑色带磁环![image](https://github.com/user-attachments/assets/d5811b8d-d33b-4b03-adde-40a6020dab55)

4.	双通六角铜柱M3*27 10个![image](https://github.com/user-attachments/assets/2f61838a-06fd-4e73-a45a-b4a636abd292)

5.	树莓派Raspberry Pi Pico 开发板 单主板 pico焊好排针![image](https://github.com/user-attachments/assets/b8d0f9a5-9efc-434b-9f12-540eab0dee5f)

6.	黑色平头十字螺丝钉 M3*12![image](https://github.com/user-attachments/assets/b041e976-359f-41d6-8277-9198060e82ae)

7.	HITBOX按钮数据线 红.1p 杜邦串13个110带护套 买2条（驳接成一条）![image](https://github.com/user-attachments/assets/2114f2fd-67c8-49cf-8d07-14b631024f26)

8.	HITBOX游戏按键线 110(2.8)端子带胶套 26条（备用两条）![image](https://github.com/user-attachments/assets/ad7c71ab-27f6-4fae-ae6b-f5c2372aff67)

9.	亚克力板子![image](https://github.com/user-attachments/assets/b906b314-ddb2-4feb-af2f-6d0d836c3fd4)

本方案不使用面板图，有需要面板图的请参考超频A视频中的流程，并且将顶层面板更换为透明面板。

材料的链接都放在压缩包了，需要的自取。

### 亚克力打板注意事项：
图纸参数按照实际亚克力板材厚度进行了优化，根据亚克力的实际厚度对侧板的卡槽进行了修改。图示中的亚克力商家的6mm实际厚度为5.5，考虑到了0.1mm的误差，将侧边的卡槽的矩形宽度修改为了5.6mm，这样修改可以让框体更加的牢固，侧边不容易晃动。如果去其他亚克力商家打板，请提前询问6mm亚克力的实际厚度数据，如果6mm亚克力实际厚度大于5.6mm，四块侧边的板子很可能卡不进去！

## 固件烧录

按住芯片上标注着BOOTSEL的白色按键连接电脑，连上电脑后会弹出一个类似U盘的窗口，松开按住的白色按键，将对应版本的固件.uf2文件复制或者直接拖到这个窗口中，窗口消失即是固件烧录成功。固件烧录完成之后，想更换固件，按住按键对应GP编号0，（正中间那个键）插入电脑，可以重新刷固件（相当于按住芯片上那个白色的键了，无需拆开框体再去按芯片上白色的键）
![image](https://github.com/user-attachments/assets/2307121a-b02d-46e0-b12e-9932496c0a6e)

![image](https://github.com/user-attachments/assets/bf43300a-9e47-488e-8be4-703dbc4ce90a)

## 按键连接


将材料中串13个端子的线驳接成一条![image](https://github.com/user-attachments/assets/fb6bbb93-6af2-4e6f-b6de-eab0530bf075)

![image](https://github.com/user-attachments/assets/a395ba58-b539-4c19-968b-556821471a3f)


![image](https://github.com/user-attachments/assets/ed481e9d-2bd9-441b-8c22-c8add7ffece1)

![image](https://github.com/user-attachments/assets/493622da-2fbb-41a0-bb30-ebc4ac0c9102)

然后将黑色那个头插在树莓派芯片上标着GND的排针上，然后把这条线其余的金色或者银色的头接在24颗按键的引脚上，每颗按键接一个引脚。


![image](https://github.com/user-attachments/assets/889c511c-e70f-49ad-9a3e-07a79d75cdf8)

![image](https://github.com/user-attachments/assets/b9d581fa-0d68-4daf-a869-8acf0570cecc)

![image](https://github.com/user-attachments/assets/4f99a784-300f-4803-b877-b291ae66ed3a)


![image](https://github.com/user-attachments/assets/09c13099-8eed-4c55-b52c-132def52fc36)

20键版本与24键版本按键对应芯片的GP编号如下图：

![image](https://github.com/user-attachments/assets/a3f21ce5-ff2e-4954-a13a-64e7fb7a7a72)


![image](https://github.com/user-attachments/assets/62109b02-bca3-44cb-8dd5-5bd1f6534296)

## 框体组装

框体组装流程比较简单，具体可以参考超频A视频中的流程，可以跳伞10：00处。以上流程搞定基本上就是做完了，不出问题的画设备就可以正常用了。下面部分为设备测试及设备使用指南部分。
https://www.bilibili.com/video/BV1rh411E7gS/?vd_source=0820846d6067f45a7b619094b125404f

## 设备测试

检查固件是否被电脑识别以及对应按键按下即可右对应输出，modifiers按键需要配合方向键来查看，单独按会没有输出。设备在不同的模式配置中对应的按键功能不同，在使用指南的模式切换中有详细说明。
输入win+r，在搜索框中输入joy.cpl，会弹出游戏控制器窗口，Controller（Pico）即是Haybox固件所对应的控制器，点击属性可以检查按键连通性，以及按键对应的功能。部分电脑属性界面为空白，要测试按键对应功能也可以通过steam设置中的控制器选项来查看，yuzu，Dolphin等平台控制器设置中也可以查看。

![image](https://github.com/user-attachments/assets/19e60421-d015-419b-ad47-a20980a9a492)

![image](https://github.com/user-attachments/assets/1fe1f7af-cebe-40f7-ac43-e2ca8bcd0eb0)

Bvoo她写了一个软件可用于设备测试，界面整洁使用简单，推荐用Bvoo测试软件进行设备测试
https://github.com/bvoo/sloptester
## 常见问题
### 按住X的时候连接Switch之后，X对应的按键没有反应了
可能是芯片的micro转打印母口线，打印口USB数据线出问题，更换这两条线材
如果更换线材之后问题仍然存在，检查按键X对应的两个引脚的接线，接线不稳也有可能出现这样的问题，将按键连接线换新。

### 手汗比较多，亚克力表面很容易脏
使用磨砂方案的亚克力面板；用磨砂材质的汽车贴膜贴在表面；把顶面的那层板换成磨砂金属面板（贵）
以上三种方法按需求任选其一。用磨砂亚克力是最快的，但磨砂亚克力还是会脏，而且沾上汗渍油渍更难清理；磨砂材质的汽车贴膜比较费手，第一次贴很容易出瑕疵；使用金属磨砂面板比较贵。

### 按键不回弹，回弹受阻
最直接的方法就是换按键，没有备用按键的话要重新买按键。
还有一种方法，把按键两边卡着键帽的凸的地方往用螺丝刀，笔，筷子之类的东西往里面推一些（两边都要推），推到按键回弹正常为止。注意推压力度不要太大，否则键帽会变高或者键帽会弹出。

### 设备在手柄硬件测试网站上或者软件上无法识别
Haybox的固件在很多手柄测试的网站上无法被识别，https://hardwaretester.com/gamepad常用的硬件测试网址在Windows系统下无法识别Haybox，在Linux系统下可以正常识别。设备测试中已写对应检测方法。

### NS上有些模式摇杆输出错乱
每个模式都有设置对应的摇杆参数，比如以太之战2 Rivals2模式在PC端进行优化。将摇杆圆的直径设置为了256，而在NS端上优化的Ultimate模式摇杆圆的直径设置为了200。此时在NS上使用Rivals2模式将会出现摇杆的左右方向相互颠倒，上下方向相互颠倒的情况，在NS上使用摇杆圆直径为200的模式可避免此类问题。

### 自定义键位，游戏模式配置
此固件按键功能与芯片GP编号已经对应，改键位在物理层面改变按键的接线以外，在按键接线流程中可以改变。需要完全自定义键位，游戏模式，Haybox中有对应的基础教程，零基础小白花点时间也能搞懂，修改固件的过程中遇到问题可前往discord中，加入Crane的服务器craneslab.xyz/discord，有更专业的人解答。

## 使用指南
20键现有的固件在一些模式上优化的不够好，我这边只写24键版本的固件的使用指南。使用20键版本的固件可以参考原版Haybox以及Austin的Haybox改版20键版本（对以太之战2有相关优化），需要看得懂英文。
![image](https://github.com/user-attachments/assets/ef2a65c5-125d-4689-b452-60642d16365b)

## 1模式切换
设备连接PC或NS及其他相关平台之后，同时按下6 + 0 + 按键对应GP编号切换到相应模式，其中PC端的默认模式是以太之战2 Rivals2模式，NS端的模式模式是任斗 Ultimate模式。需要切换到其他模式请手动切换。设备模式切换表如下，模式具体内容在后面提及。
![image](https://github.com/user-attachments/assets/737bc166-12b3-48c2-b313-42c1646cf898)

### 1.1 以太之战2模式
以太之战2模式优化的比较完善。如果你有更好的建议，可以联系我
![image](https://github.com/user-attachments/assets/e5c50524-69d8-43c3-a06c-9c152d62bdec)
最右上角为十字键左，按下mod-z之后再按这个键变为十字键右，对应以太之战2训练场的重置以及保存，设置在右手方便按的位置用于快速重置位置，及在重置极限位置之后快速输，实战中十字键为嘲讽键，如果怕误触嘲讽，可以把键位设置中把D-pad movement给开启。
十字键左下面那个是左摇杆50度，按下mod-z之后这个键变为左摇杆130度，这个功能用于输入jab推进反方向的上t（需要在同一帧输入左上或者右上），此外，也有优化反方向下t，及按下mod-x或者mod-y之后再按这个键，会输入左摇杆的斜下，但几乎不用。

### 1.2 传统格斗Fgc模式
传统格斗模式如下，如果你有更好的建议，可以联系我。
![image](https://github.com/user-attachments/assets/ddad62dd-9686-459b-a825-8249aec22611)
按下mod-x之后，右手大拇指区域四个键将切换为右摇杆键，右摇杆按键布局参考Rivals2模式。
在街霸6中，左手下方向与十字键上方向回中，右手大拇指有一颗标注着“与左摇杆下相互覆盖”的那颗十字键上，与左手下方向相互覆盖。
该模式默认SOCD为后覆盖，布局中有多个上方向，其中只有一个左摇杆的上方向（wasd区域），其他都是十字键上方向。不同的格斗游戏对左摇杆与十字键的关系判定并不一致，例如街霸6中左摇杆与十字键相反方向同时按下会回中，而在龙珠斗士中十字键将会覆盖左摇杆，左摇杆无法覆盖十字键。右手大拇指标注的“与左摇杆相互覆盖”，那颗十字键上在所有格斗游戏中都可以与左摇杆下相互覆盖，没有标注的只是普通十字键，根据游戏对左摇杆与十字键的判定关系变化而变化。

### 1.3 任斗Ultimate模式
任斗Ultimate模式如下，如果你有更好的建议，可以联系我。
![image](https://github.com/user-attachments/assets/5cc0bff9-ca6c-4539-92f9-59d31fdea750)
请按住GP编号22连接NS！！！否则会出现设备连接上马上断连的情况。
任斗Ultimate我并不熟悉，很多键位设计细节了解不到位，玩家可以根据自己合适的键位设置进行设置，该键位布局可设置按键是大大超出ultimate本身的键位设置需求，玩家可根据自身需求进行合理优化。由于ultimate键位设置中可以设置三个十字键，该布局增设了三个十字键供玩家优化自身键位，其中有两个相同的A按键，功能完全一样。
图示中的手柄按键名称是XBOX的按键名称，按住GP编号22连接NS之后是识别成PRO手柄，玩家进入ultimate键位设置界面，点击测试，按下对应的按键可以得到按键对应PRO手柄的按键名称。按键名称的对应关系如下：
![image](https://github.com/user-attachments/assets/6ddcf613-cb1d-43bd-8122-1b2434f66f34)

### 1.4 任斗Ultimate2模式
任斗Ultimate2模式如下，该模式增加了一键普b，空n，Smash及一键小跳功能，这个模式很明显是违规的，同时在键位布局上有几颗按键存在对应关系，无法更改，使用前请慎重考虑。相关东西尽量不要联系我。
![image](https://github.com/user-attachments/assets/45dc04f0-b610-4275-9a8b-f2ee72376475)
这个键位布局中按键之间的联系给键位设置带来了不少局限性，图示中A必须设置成attack，B必须设置成special，Y和LB必须设置成跳，这样才能让一键空n，普b，smash，小跳起作用。
按下Smash时候，设备同时输出A和B;   按下S-Jump时，设备同时输出Y+LB;
按下N-air时，设备左摇杆强制回中的同时输出A;  按下N-special时，设备左摇杆强制回中的同时输出B

### 1.5 自用模式
以下是我本人自用的一些游戏模式，如有需要，可以自行切换。

#### 龙珠斗士DBFZ模式 6 + 0 + 26
![image](https://github.com/user-attachments/assets/7f6de2c5-d62b-42b9-9456-c849ffb3bc0a)

#### SSF2模式 6 + 0 + 19
![image](https://github.com/user-attachments/assets/1b5c7d79-669a-4418-9855-9a1590569f1b)

#### Fraymaker模式 6 + 0 + 20
![image](https://github.com/user-attachments/assets/428f1fc2-b470-4e44-9701-4092589fe06a)

### 1.6 键盘模式
键盘模式都是字母，不做图例示范。
切换到键盘模式步骤，先按住21插入电脑，接上电脑后松开21，同时按7 + 0 + 5切换到键盘模式。


## 2平台切换
(大部分玩家是在NS或者PC上用，PC直连就行，按住22插入NS).
如果什么按键都没有按住，直接连接设备，默认就是 XInput, PC上绝大部分游戏都能正常使用. 其他对应的平台，或者相对应的输入后端要按住图示中标号的按键切换到对应的平台。
22 - Nintendo Switch USB mode  （按住22 插入Switch主机，会识别成pro手柄）
19 - DInput mode (只建议在游戏不支持XInput的时候使用)
15 - GameCube backend with polling rate fix disabled (用于ngc转换器)
116 - Nintendo 64 backend (60Hz 轮询率)

## 3大乱斗类游戏相关操作（特别篇）
此部分主要围绕modifiers按键展开，如果你有其他想补充的，可以联系我。
### 3.1 角度调整
已wasd布局为例，（wd wa as ds）形成45°角之后，输入mod-x变成近似30°的角度；输入mod-y变成近似60°的角度。形成30°或者60°之后，再输入一个右摇杆键进行微调。图示如下：
![image](https://github.com/user-attachments/assets/4bd8bff1-d358-471c-a9df-1265a896480f)
![image](https://github.com/user-attachments/assets/93087cad-c883-4d09-b4d6-89d50d6e5eaa)
48方向在没有按额外按键的情况下是全推摇杆100%推出，要做到80% 60%摇杆推出需要按额外的键。例如：按下wd在第一象限形成45°角，按下mod-x之后是30°角，再按下右摇杆的上形成40°角。此时没有按额外的按键，为100%摇杆推出。此时按下按键GP编号20，摇杆80%推出；此时按下按键GP编号22，摇杆60%推出；此时同时按下按键GP编号20与22，摇杆以一个细微的幅度推出。(摇杆推出幅度功能用于任斗中的皮卡丘及稀客等角色的上B, 以太之战2中的Forsburn也是同理)
这和BOXX的modifers的角度调整逻辑类似，但modifiers配合右摇杆键的对应的微调角度有差别，如果想用原版，可以参考BOXX的设备说明文档。

### 3.2 走路速度调整
当按下mod-y时输入水平方向的左摇杆键，输出为轻推左摇杆，慢走；（实际以游戏判定为准）
当按下mod-x时输入水平方向的左摇杆键，输出为中推左摇杆，快走/小跑；（实际以游戏判定为准）
当什么都不按输入水平方向的左摇杆键，输出为全推左摇杆，冲刺/跑；（实际以游戏判定为准）

### 3.3 急停功能
由于按下modx或mody之后输入水平方向的摇杆键，会识别为快走或者快慢走，在dash冲刺或者run跑的时候按下modx或者mody，然后输入相反的水平方向左摇杆键，实现转身急停，配合此功能可以做到转身急停出t以及jab。
### 3.4 斜横向强攻击
输入45°（-45°）之后按下mod-x会形成近似30°（-30°）的角度，此时输入attack可以出斜横t。
### 3.5 右摇杆斜向di
按住mod-z之后，输入左摇杆45度之后按下右摇杆的键，右摇杆会输出斜上或斜下的角度。例如：输入左摇杆右下之后按右摇杆下，右摇杆会往下倾斜；输入左摇杆右下之后按右摇杆右，右摇杆会往右倾斜。
## 相关内容
作为国内首批进行以太之战2内测的大怨种玩家，内测以太之战2之前用键盘玩了很久的ssf2，后面发现以太之战2中需要更多的角度与更多精细化的操作，键盘远远满足不了我的需求。当时买了个破手柄试了一下，发现好难适应手柄，移动都不太会移动了，更别说那些难点的操作了。然后我就想定制个有多重左摇杆方向的hitbox，问了三家都做不了，毕竟当时流行的是GP2040固件,适用于传统格斗，而且当时国内改装固件人的少，定制hitbox的商家也很少，更别说按照这么奇怪的要求定制了。大部分都是现成的固件直接拿来用的，定制主要也是定制个布局。
后来我就自己找了一些资源，看了超频a的hitbox制作视频，自己改了一个20键布局的box，用的固件是pico-rectangle，用起来基本的功能是有了，但是模式少，同时也有不少的局限性。后面加入了Crane discord，里面有很多资源和大佬，了解到了haybox固件及其教程。一点一点的学，现在基本的功能已经会改了。有时间精力的小伙伴也可以尝试。以下是相关内容及资源：
https://www.bilibili.com/video/BV1rh411E7gS/?share_source=copy_web&vd_source=fb0f03b29df4c53d7cb13f8779334701
https://github.com/JonnyHaystack/HayBox
https://github.com/901Austin/HayBox/blob/haybox-rivals2-smash64/src/modes/Rivals2.cpp
https://github.com/JulienBernard3383279/pico-rectangle
http://craneslab.xyz/discord
https://github.com/OtaK/b0xx-viewer-rs
https://www.youtube.com/watch?v=w4r5CNIimU0&list=LL&index=25&t=8s
https://www.youtube.com/watch?v=JE7BwEGd3VY&list=LL&index=27
https://discord.com/invite/jhAAsqJ
https://b0xx.com/
https://www.hitboxarcade.com/products/smash-box
https://www.bilibili.com/video/BV1NX4y1x7Ti/?spm_id_from=333.337.search-card.all.click&vd_source=0820846d6067f45a7b619094b125404f
https://github.com/GRAMCTRL/remapp.ing

以下是原版的readme
# HayBox

HayBox is a modular, cross-platform firmware for digital or mixed analog/digital controllers, primarily targeted at [B0XX](https://b0xx.com)-style controllers.

[![GitHub issues](https://img.shields.io/github/issues/JonnyHaystack/HayBox)](https://github.com/JonnyHaystack/HayBox/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/JonnyHaystack/HayBox)](https://github.com/JonnyHaystack/HayBox/pulls)

## Table of Contents

* [Features](#features)
* [Installation](#installation)
  * [Pre-built binaries](#pre-built-binaries)
  * [Building from source](#building-from-source)
* [Usage](#usage)
  * [Default button holds](#default-button-holds)
  * [Dolphin setup](#dolphin-setup)
* [Customisation](#customisation)
  * [Console/gamemode selection bindings](#consolegamemode-selection-bindings)
  * [Creating custom input modes](#creating-custom-input-modes)
  * [SOCD](#socd)
  * [Mod X lightshield and R shield tilt](#mod-x-lightshield-and-r-shield-tilt)
  * [Mode-specific optional features](#mode-specific-optional-features)
    * [Melee modes](#melee-modes)
    * [Project M/Project+ mode](#project-mproject-mode)
  * [Input sources](#input-sources)
  * [Using the Pico's second core](#using-the-picos-second-core)
* [Troubleshooting](#troubleshooting)
* [Contributing](#contributing)
* [Contributors](#contributors)
* [License](#license)

## Features

Features include:
- Cross platform support:
  - RP2040 (e.g. Raspberry Pi Pico)
  - 16MHz AVR MCUs (e.g. ATMega32U4 which several Arduinos are based on)
- Supports many existing controllers/PCBs, e.g. B0XX, LBX, Smash Box, Crane's
  GCCPCB/Model S
- Supports a variety of communication backends which can be used either separately or in conjunction with each other:
  - XInput
  - DInput
  - GameCube console
  - Nintendo 64 console
  - Nintendo Switch console
  - B0XX input viewer
- Supports a variety of "input sources" which can be used in conjunction to create mixed input controllers:
  - Buttons/switches wired directly to GPIO pins
  - Switch matrix (as typically found in keyboards)
  - Wii Nunchuk
  - GameCube controller
- Melee mode up to date with B0XX V3 specifications
- Existing modes for popular games (e.g. Melee, Project M, Ultimate, Rivals of Aether, traditional fighting games)
- Easy to create new controller modes (or keyboard modes) for different games
- USB keyboard game modes for games that lack gamepad support
- Fully customisable SOCD cleaning, allowing you to configure SOCD button pairs (e.g. left/right, up/down) for each controller/keyboard mode, and also easily change the SOCD resolution method for each SOCD pair
- Switch modes on the fly without unplugging your controller
- Automatically detects whether plugged into console or USB
- Game modes and communication backends are independent entities, meaning you can use any game mode with any supported console without extra work
- Easily switch between different GameCube/N64 polling rates in order to have optimal latency on console, overclocked adapter, etc. (not necessary for Pico/RP2040)

## Installation

If you want to simply use a pre-built firmware with default pin mappings and configuration, refer to the [pre-built binaries](#pre-built-binaries) section. If you want to make any changes to the code, refer to the [building from source](#building-from-source) section.

### Pre-built binaries

1. Browse the [existing configs](config/) to determine which config is appropriate for your hardware
2. Download the corresponding artifact from either the [latest HayBox release](https://github.com/JonnyHaystack/HayBox/releases), or from a [workflow run](https://github.com/JonnyHaystack/HayBox/actions) if you want the latest development version (unstable).
3. Flash the firmware to your microcontroller in the usual way
   - If you are using a Pico/RP2040 build (`.uf2` file), simply put it into bootsel mode while plugging it into your PC, and drag and drop the `.uf2` file onto the RPI-RP2 drive that comes up
   - If you are using Arduino/AVR build (`.hex` file), you can use a program like [QMK Toolbox](https://github.com/qmk/qmk_toolbox) to flash the `.hex` file to it

### Building from source

There are currently three main ways to build HayBox:
- Locally using PlatformIO IDE for VSCode or PlatformIO CLI
- In the cloud using GitHub Codespaces
- In the cloud using GitHub Actions

Both GitHub Actions and GitHub Codespaces require you to create a GitHub account, but do not require you to install any dependencies on your local machine.

#### Building locally

The following dependencies are required when building locally:
- [Git](https://git-scm.com/downloads) - required only if you are using a Pico
- [PlatformIO IDE for VSCode](https://platformio.org/install/ide?install=vscode)

After installing all of the requirements, download and extract the
[latest HayBox release](https://github.com/JonnyHaystack/HayBox/releases),
or clone the repository if you have git installed (which makes it easier for you
to pull updates).

After that:
1. Open Visual Studio Code
2. If on Windows and it's your first time building HayBox, run the command `git config --global core.longpaths true` in any terminal (within VS Code or regular cmd/PowerShell are all fine)
3. Click File -> **Open Folder** and choose the HayBox folder (the one containing platformio.ini, not the folder above that)
4. Choose the appropriate build environment for your controller's PCB by
  clicking the environment selection button near the bottom left of the window
  
  ![image](https://user-images.githubusercontent.com/1266473/187039372-485c5f0d-60b3-4534-befb-e713f138a7c8.png)
  ![image](https://user-images.githubusercontent.com/1266473/187039585-cea18994-fd12-45fb-b43f-427eb7affb81.png)
  
5. If your controller has a different pinout than any of the existing configs, you may edit the button mappings and other pins at the top of the config (`config/<environment>/config.cpp`). Any buttons that your controller doesn't have can simply be deleted from the list.
6. If you see a message in the bottom bar saying "Rebuilding IntelliSense Index" or "Loading Project Tasks", wait for it to disappear. For Pico especially it may take quite a while the first time because it has to download 2-3GB of dependencies.
7. Click **Build** (in the bottom left) and make sure everything compiles without
  errors
8. This next step differs depending on the microcontroller used in your controller.
    - **For Pico-based controllers**: hold the bootsel button while plugging it in (or your Start button if you already have HayBox installed) and then drag and drop the file `HayBox/.pio/build/<environment>/firmware.uf2` onto the RPI-RP2 drive that comes up.
    - **For Arduino-based controllers**: Plug in your controller via USB and click **Upload** (next to the Build button)

#### Building using GitHub Codespaces

This is probably the most convenient way to modify and rebuild HayBox, but bear in mind that GitHub's free tier places [some limitations](https://docs.github.com/en/billing/managing-billing-for-github-codespaces/about-billing-for-github-codespaces#monthly-included-storage-and-core-hours-for-personal-accounts) on how much you can use Codespaces each month. Because of this, you will want to make sure you shut down your Codespaces when you aren't using them, in order to maximise what you can get from your quota.

First, create a GitHub account or just log in if you already have one, then [fork this repository](https://github.com/JonnyHaystack/HayBox/fork) and open your fork in a new Codespace by clicking the green Code button -> Codespaces -> Create codespace on master. This should open VS Code in your browser with all of the necessary extensions and dependencies pre-installed. From here, the process is much the same as [building locally](#building-locally), except you can't use the Upload button to flash the firmware. You will instead have to download the compiled binary from `HayBox/.pio/build/<environment>/` and flash it manually (see [here](#pre-built-binaries) for more on that).

#### Building using GitHub Actions

This repository contains a GitHub Actions workflow definition that builds each PlatformIO environment [specified in the matrix](https://github.com/JonnyHaystack/HayBox/blob/master/.github/workflows/build.yml#L13) on every push, and uploads firmware binaries as artifacts which you can download by clicking a specific workflow run from the [history](https://github.com/JonnyHaystack/HayBox/actions). You can create a fork of this repository and enable Actions by clicking Settings -> Actions -> General -> Select "Allow all actions and reusable workflows" -> Save.

The fastest way to make changes if you only want to build via GitHub Actions is to use [github.dev](https://github.dev). You can do so by simply pressing `.` on your keyboard while you have your fork of this repository open, and it will open a VS Code editor in your browser. This does not give you the same development capabilities that you'd get in a Codespace, but it does allow you to make changes and commit them directly from your browser. Change whatever you'd like, then use the Source Control tab on the left to add, commit, and push your changes. Finally, go back to the repository and click on the Actions tab, click on your workflow run, and wait for it to build the artifact.

If you are adding a new device config/PlatformIO environment, you will have to add the environment to the [matrix](https://github.com/JonnyHaystack/HayBox/blob/master/.github/workflows/build.yml#L13) in order for it to be built by the GitHub Actions workflow. You can also remove any environments from the matrix that you don't care about in order to reduce resource usage and potentially speed up your builds.

## Usage

### Default button holds

#### Pico bootsel mode

To reboot Pico-based controllers into bootsel mode, hold Start on plugin.

#### Brook board passthrough mode

To switch to Brook board mode on GCCPCB2, GCCMX, B0XX R2, or LBX, hold B on
plugin.

#### Communication backends (console selection)

Communication backends are selected slightly differently depending on the type
of microcontroller used in the controller.

On Pico/RP2040, USB vs GameCube vs Nintendo 64 is detected automatically. If
not plugged into a console, the default is **XInput**, which should work
plug-and-play with most PC games.
Other backends are selected by holding one of the following buttons on plugin:
- X - Nintendo Switch USB mode (also sets initial game mode to Ultimate mode)
- Z - DInput mode (only recommended for games which don't support XInput)

On Arduino/AVR, the **DInput** backend is selected if a USB connection is detected.
Otherwise, it defaults to GameCube backend, unless another backend is manually
selected by holding one of the following buttons on plugin:
- A - GameCube backend with polling rate fix disabled (used for GCC adapters)
- C-Left - Nintendo 64 backend (60Hz polling rate)

#### Game mode selection

Unlike other similar firmwares, HayBox by default allows you to switch
modes on the fly without unplugging your controller. This is mainly useful on
PC, as opposed to console where you usually have to restart the console to
switch game anyway. It also serves the purpose of reducing the number of buttons
you have to hold with one hand while plugging in.

The default controller mode button combinations are:
- Mod X + Start + L - Melee mode (default)
- Mod X + Start + Left - Project M/Project+ mode
- Mod X + Start + Down - Ultimate mode
- Mod X + Start + Right - FGC mode (Hitbox style fighting game layout)
- Mod X + Start + B - Rivals of Aether mode

Default keyboard mode button combinations (only available when using DInput backend, **not** with XInput):
- Mod Y + Start + L - Default keyboard mode

### Dolphin setup

HayBox needs a different Dolphin controller profile than the official B0XX firmware, as it
uses different DInput mappings that make more sense for use across multiple games. These
can be found in the `dolphin` folder in the HayBox repo. The profile files are named to
indicate what communication backend and operating system they are for:
- For Windows:
  - HayBox_XInput.ini - For Pico/RP2040-based controllers (e.g. B0XX R4)
  - HayBox_DInput.ini - For Arduino/AVR-based controllers (e.g. B0XX R1-3, LBX)
- For Linux:
  - HayBox_XInput_Linux.ini - For Pico/RP2040-based controllers (e.g. B0XX R4)
  - HayBox_DInput_Linux.ini - For Arduino/AVR-based controllers (e.g. B0XX R1-3, LBX)
- For macOS (unsupported*):
  - HayBox_DInput_macOS.ini

To install the profile:
1. Copy the appropriate .ini file from the `dolphin` folder within HayBox to the folder `<YourDolphinInstallation>\User\Config\Profiles\GCPad\` (create it if it does not exist)
- For Slippi this should be
  - On Windows: `%appdata%\Slippi Launcher\netplay\User\Config\Profiles\GCPad\`
  - On Linux: `~/.config/SlippiOnline/Config/Profiles/GCPad/`
  - On Mac: `Cmd + Shift + G` and enter the path `/Users/<USER>/Library/Application Support/Slippi Launcher/netplay/Slippi Dolphin.app/Contents/Resources/Sys/Config/Profiles/GCPad`
- For vanilla Dolphin: 
  - On Windows: `%userprofile%\Documents\Dolphin Emulator\Config\Profiles\GCPad\`
  - On Linux: `~/.config/dolphin-emu/Profiles/GCPad/`
2. Plug in your controller, and configure a "Standard Controller" in Dolphin
3. Click **Refresh** next to the Device dropdown
4. Select the HayBox profile from the profile dropdown, and click **Load** (NOT Save)
5. Make sure the correct device is selected in the device dropdown
6. Click **Close**

\* macOS only supports DInput (and not very well), so if using a Pico/RP2040-based controller you will have to force DInput mode by holding Z on plugin, and even then it may not work. I can't really do anything about Apple's poor controller support (which they seem to break with every other update) and I don't own any Apple devices, so this will also be considered unsupported usage of HayBox.

## Customisation

### Console/gamemode selection bindings

#### Communication backends (console selection)

The communication backend (e.g. DInput, GameCube, or N64) is selected partly
through auto detection and partly based on the buttons held on plugin. This is
handled in `config/<environment>/config.cpp`, in the `setup()` function.
The logic is fairly simple, and even if you don't have programming experience it
shouldn't be too hard to see what's going on and change things if you wish.

The config folders corresponding to the Arduino environments are:
- `config/arduino_nativeusb/` for Arduino with native USB support (e.g. Leonardo, Micro)
- `config/arduino/` for Arduino without native USB support (e.g. Uno, Nano, Mega 2560)

For Arduino device configs you may notice that the number 125 is passed into
`GamecubeBackend()`. This lets you change the polling rate e.g. if your DIY
doesn't support native USB and you want to use it with an overclocked GameCube
controller adapter. In that example, you could pass in 1000 to sync up to the
1000Hz polling rate, or 0 to disable this lag fix completely.
Polling rate can be passed into the N64Backend constructor in the same way as this.

You may notice that 1000Hz polling rate works on console as well. Be aware
that while this works, it will result in more input lag. The point of setting
the polling rate here is so that the GameCube backend can delay until right
before the next poll before reading the inputs, so that the inputs are fresh and
not outdated.

For Pico/RP2040, it is not necessary to pass in a console polling rate, because
the Pico has enough processing power to read/process inputs after receiving the
console poll, so there is no need to predict when the poll will arrive and
prepare things in advance.

#### Input modes

To configure the button holds for input modes (controller/keyboard modes), edit
the `select_mode()` function in `config/mode_selection.hpp`. Each `if`
statement is a button combination to select an input mode.

Most input modes support passing in an SOCD cleaning mode, e.g.
`socd::2IP_NO_REAC`. See [here](#socd) for the other available modes.

### Creating custom input modes

For creating new input modes, it helps if you know some C++, or at least have
some programming experience. That said, you should be able to get by even
without prior experience if you just base your new mode off the existing ones
and refer to them as examples.

There are two types of input modes: ControllerMode and KeyboardMode

#### Keyboard modes

Keyboard modes are a little bit simpler so let's start there.

A KeyboardMode behaves as a standard keyboard and should work with any device
that supports keyboards.

You are free to use whatever logic and programming tricks you like in the
`UpdateKeys()` function to decide the outputs based on the input state. You could
create input layers (like the D-Pad layer in Melee mode that is activated when
holding Mod X and Mod Y), or other types of conditional inputs.

The list of available keycodes can be found [here](https://github.com/JonnyHaystack/ArduinoKeyboard/blob/master/include/keycodes.h).

Remember that keyboard modes can only be activated when using the **DInput** communication backend (**not** XInput).

#### Controller modes

A ControllerMode takes a digital button input state and transforms it into an
output state corresponding to a standard gamepad. Any ControllerMode will work
with any CommunicationBackend. A CommunicationBackend simply reads inputs from one or more input sources, uses the current ControllerMode to update the outputs based on those inputs, and handles the sending of the outputs to the console or PC.

To create a ControllerMode, you just need to implement the functions
`UpdateDigitalOutputs()` and `UpdateAnalogOutputs()`.

`UpdateDigitalOutputs()` is very similar to the `UpdateKeys()` function in keyboard
modes, with the difference that rather than calling a `Press()` function to
immediately send inputs, we are simply setting the output state for this
iteration. As the name indicates, we will only deal with the digital outputs in
this function.

`UpdateAnalogOutputs()` is a bit more complicated. Firstly, it has to call
`UpdateDirections()` before doing anything else. This function takes in values
indicating whether your left and right sticks are pointing left/right/up/down.
You also pass in the minimum, neutral (centre), and maximum stick analog values,
so you can configure these on a per-mode basis. All this information is used to
automatically set the stick analog values based on the inputs you passed in. This
is all you need to do unless you want to implement modifiers.

`UpdateDirections()` also populates the variable `directions` with values
indicating current stick direction, which can be 1, 0, or -1 for the X and Y
axes for both sticks. These values make it much easier to write modifier logic.

After calling `UpdateDirections()`, add any modifier handling logic that you want.
Remember that `UpdateDirections()` already set the default analog stick values,
so when handling modifiers you only need to manually set the values for the axes
that are actually being modified. Other than this, I can't teach how to write
your modifier logic, so just look at the examples and play around.

Finally, set any analog trigger values that you need.

Note: Analog trigger outputs could just as well be handled in
`UpdateDigitalOutputs()`, but I think it usually looks cleaner to keep them
along with the other analog outputs.

Also note: You don't need to worry about resetting the output state or clearing
anything from it. This is done automatically at the start of each iteration.

### SOCD

In the constructor of each mode (for controller modes *and* keyboard modes), you
can configure pairs of opposing direction inputs to apply SOCD cleaning to.

For example, in `src/modes/Melee20Button.cpp`:
```
_socd_pair_count = 4;
_socd_pairs = new socd::SocdPair[_socd_pair_count]{
    socd::SocdPair{&InputState::left,    &InputState::right,   socd_type},
    socd::SocdPair{ &InputState::down,   &InputState::up,      socd_type},
    socd::SocdPair{ &InputState::c_left, &InputState::c_right, socd_type},
    socd::SocdPair{ &InputState::c_down, &InputState::c_up,    socd_type},
};
```

This sets up left/right, down/up, C-Left/C-Right, and C-Down/C-Up as pairs of
opposing cardinal directions for which SOCD cleaning will be applied. The SOCD
cleaning is automatically done before `UpdateDigitalOutputs()` and
`UpdateAnalogOutputs()`, and you do not need to worry about it any further than
that.

For each `SocdPair` you can pass in an `SocdType` of your choosing. By default
for most modes this is passed in as a single constructor parameter, but it is
possible to pass in multiple parameters, or simply use a hardcoded value. Both
of these approaches are exemplified in `src/modes/FgcMode.cpp`.

| `SocdType` | Description |
| ---------- | ----------- |
| `SOCD_NEUTRAL` | Left + right = neutral - the default if no `SocdType` specified in the `SocdPair` |
| `SOCD_2IP` | Second input priority - left -> left + right = right, and vice versa. Releasing the second direction gives the original direction |
| `SOCD_2IP_NO_REAC` | Second input priority without reactivation - same as above, except releasing the second direction results in neutral. The original direction must be physically reactuated. |
| `SOCD_DIR1_PRIORITY` | The first button in the `SocdPair` always takes priority over the second |
| `SOCD_DIR2_PRIORITY` | The second button in the `SocdPair` always takes priority over the first |
| `SOCD_NONE` | No SOCD resolution - the game decides |

Note that you do not have to implement a `HandleSocd()` function like in the
Melee20Button and Melee18Button modes. It is only overridden in these modes
so that we can check if left and right are both held *before* SOCD cleaning,
because when they are both held (without a vertical direction being held) we
need to override all modifiers.

### Mod X lightshield and R shield tilt

If your controller has no lightshield buttons, you may want to use Mod X for
lightshield and put shield tilt on R instead. You can do this by using the
Melee18Button mode instead of Melee20Button.

### Mode-specific optional features

#### Melee modes

The Melee20Button and Melee18Button modes provide a choice of which coordinates to use
when pressing down + right. By default, holding down + back will allow you to do automatic
jab-cancels, which is a useful technique for some characters.

Another popular technique that uses the down + right diagonal is the so-called crouch/walk
option-select. This technique involves holding down + forward at a certain angle while
crouching, such that after crouch-cancelling an attack you will automatically start
walking towards your opponent instead of going back into crouch. This can be very useful
for tech-chasing, but the coordinates used for this technique do not allow you to auto
jab-cancel.

This can be configured as seen in `config/mode_selection.hpp` by setting the `crouch_walk_os` option to true:

```
new Melee20Button(socd::SOCD_2IP_NO_REAC, { .crouch_walk_os = false })
```

You will also have to change this in your `config/<environment>/config.cpp` in order for it to be applied on plugin, as `mode_selection.hpp` only controls what happens when you *switch* mode.

#### Project M/Project+ mode

The ProjectM mode has some extra options to configure certain behaviours. As seen
in `config/mode_selection.hpp`:

```
new ProjectM(
    socd::SOCD_2IP_NO_REAC,
    { .true_z_press = false, .ledgedash_max_jump_traj = true }
)
```

Firstly, the `ledgedash_max_jump_traj` option allows you to enable or disable the behaviour
borrowed from Melee mode where holding left and right (and no vertical directions)
will give a 1.0 cardinal regardless of modifiers being held.

If you change the SOCD mode to 2IP (with reactivation), you should also change
this option to false if you want a smooth gameplay experience.

Secondly, the `true_z_press` option exists because Project M/Project+ do not handle
Z presses the same way Melee does.
Melee interprets a Z press as lightshield + A, and thus it can be used for L
cancelling without locking you out of techs. In PM/P+, a Z press will trigger a
tech and thus cause unwanted tech lockouts if used to L cancel.
By default in HayBox, the ProjectM mode is set to use a macro of lightshield + A
in order to preserve expected behaviour from Melee. However, this macro does not
enable you to use tether/grapple attacks or grab items. To workaround this, you
can press Mod X + Z to send a true Z input.

If this bothers you, and you just want to send a true Z input by default when
pressing Z, you can set the `true_z_press` option to true.

### Input sources

HayBox supports several input sources that can be read from to update the input
state:
- `GpioButtonInput` - The most commonly used, for reading switches/buttons connected directly to GPIO pins. The input mappings are defined by an array of `GpioButtonMapping` as can be seen in almost all existing configs.
- `SwitchMatrixInput` - Similar to the above, but scans a keyboard style switch matrix instead of individual switches. A config for Crane's Model C<=53 is included at `config/c53/config.cpp` which serves as an example of how to define and use a switch matrix input source.
- `NunchukInput` - Reads inputs from a Wii Nunchuk using i2c. This can be used for mixed input controllers (e.g. left hand uses a Nunchuk for movement, and right hand uses buttons for other controls)
- `GamecubeControllerInput` - Similar to the above, but reads from a GameCube controller. Can be instantiated similarly to GamecubeBackend. Currently only implemented for Pico, and you must either run it on a different pio instance (pio0 or pio1) than any instances of GamecubeBackend, or make sure that both use the same PIO instruction memory offset.

Each input source has a "scan speed" value which indicates roughly how long it takes for it to read inputs. Fast input sources are always read at the last possible moment (at least on Pico), resulting in very low latency. Conversely, slow input sources are typically read quite long before they are needed, as they are too slow to be read in response to poll. Because of this, it is more ideal to be constantly reading those inputs on a separate core. This is not possible on AVR MCUs as they are all single core, but it is possible (and easy) on the Pico/RP2040. The bottom of the default Pico config `config/pico/config.cpp` illustrates this by using core1 to read Nunchuk inputs while core0 handles everything else. See [the next section](#using-the-picos-second-core) for more information about using core1.


In each config's `setup()` function, we build up an array of input sources, and then pass it into a communication backend. The communication backend decides when to read which input sources, because inputs need to be read at different points in time for different backends. We also build an array of communication backends, allowing more than one backend to be used at once. For example, in most configs, the B0XX input viewer backend is used as a secondary backend whenever the DInput backend is used. In each iteration, the main loop tells each of the backends to send their respective reports. In future, there could be more backends for things like writing information to an OLED display.

### Using the Pico's second core

In each config, there are the functions `setup()` and `loop()`, where `setup()` runs first, and then `loop()` runs repeatedly until the device is powered off.

On Pico/RP2040, the `setup()` and `loop()` functions execute on core0, and you can add the functions `setup1()` and `loop1()` in order to run tasks on core1.

For example, to read GameCube controller inputs on core1:
```
GamecubeControllerInput *gcc = nullptr;

void setup1() {
    while (backends == nullptr) {
        tight_loop_contents();
    }

    gcc = new GamecubeControllerInput(gcc_pin, 2500, pio1);
}

void loop1() {
    if (backends != nullptr) {
        gcc->UpdateInputs(backends[0]->GetInputs());
    }
}
```

The `while` loop makes sure we wait until `setup()` on core0 has finished setting up the communication backends. We then create a GameCube controller input source with a polling rate of 2500Hz. We also run it on `pio1` as an easy way to avoid interfering with any GameCube/N64 backends, which use `pio0` unless otherwise specified. In `loop1()` we make the assumption that the primary backend is the first element of the `backends` array (which is configured in the same file anyway, so we aren't truly assuming anything we don't know) and directly scan the GameCube controller inputs into the backend's input state.

As a slightly crazier hypothetical example, one could even power all the controls for a two person arcade cabinet using a single Pico by creating two switch matrix input sources using say 10 pins each, and two GameCube backends, both on separate cores. The possibilities are endless.

## Troubleshooting

### Controller not working with console or GameCube adapter

If you are using an official adapter with an Arduino-based controller you will likely have to hold A on plugin which disables the polling latency optimisation by passing in a polling rate of 0 to the GamecubeBackend constructor.

If you are using an Arduino-based controller without a boost circuit, you will need 5V power so for Mayflash adapter you need both USB cables plugged in, and on console the rumble line needs to be intact. Pico works natively with 3.3V power so this isn't an issue.

## Contributing

I welcome contributions and if you make an input mode that you want to share,
feel free to make a pull request. Please install the clang-format plugin for
VS Code and use it to format any code you want added.

### Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available,
see the [tags on this repository](https://github.com/JonnyHaystack/HayBox/tags).

## Built With

* [https://github.com/MHeironimus/ArduinoJoystickLibrary]() - Used for DInput support for AVR
* [https://github.com/NicoHood/Nintendo]() - Used for GameCube and Nintendo 64 support for AVR
* [https://github.com/JonnyHaystack/ArduinoKeyboard]() - Used for keyboard modes on AVR
* [https://github.com/JonnyHaystack/arduino-nunchuk]() - Used for Nunchuk support
* [https://github.com/JonnyHaystack/joybus-pio]() - Used for GameCube and Nintendo 64 support for RP2040
* [https://github.com/earlephilhower/arduino-pico]() - Used for Arduino framework/PlatformIO support for Pico

## Contributors

* **Jonathan Haylett** - *Creator* - [@JonnyHaystack](https://github.com/JonnyHaystack)
* **Crane** - *Creator of the DIYB0XX firmware, which served as a great reference/starting point* - [@Crane1195](https://github.com/Crane1195)

See also the list of [contributors](https://github.com/JonnyHaystack/HayBox/contributors) who participated in this project.

### Acknowledgments

* The B0XX team, for designing and creating an incredible controller
* [@Crane1195](https://github.com/Crane1195) - for his DIYB0XX and GCCPCB projects, and for hours of answering my questions when I was first writing this
* [@MHeironimus](https://github.com/MHeironimus) - for the Arduino Joystick library
* [@NicoHood](https://github.com/NicoHood) - for the Nintendo library
* [@GabrielBianconi](https://github.com/GabrielBianconi) - for the Arduino Nunchuk library
* [@earlephilhower](https://github.com/earlephilhower) - for the arduino-pico core
* [@maxgerhardt](https://github.com/maxgerhardt) - for adding PlatformIO support for arduino-pico
* The Arduino project and the Raspberry Pi Foundation - for all their open-source hardware and software

## License

This project is licensed under the GNU GPL Version 3 - see the [LICENSE](LICENSE) file for details
