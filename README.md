## Python版植物大战僵尸

* 已有的植物：向日葵，豌豆射手，坚果墙，寒冰射手，樱桃炸弹，双发射手，三线射手，大嘴花，小喷菇，土豆雷，地刺，胆小菇，倭瓜，火爆辣椒，阳光菇，寒冰菇，魅惑菇，火炬树桩，睡莲，杨桃，咖啡豆，海蘑菇，高坚果，缠绕水草，毁灭菇，墓碑吞噬者，大喷菇，大蒜，南瓜头
* 已有的僵尸：普通僵尸，旗帜僵尸，路障僵尸，铁桶僵尸，读报僵尸，橄榄球僵尸，鸭子救生圈僵尸，铁门僵尸，撑杆跳僵尸，冰车僵尸，潜水僵尸
* 使用JSON文件记录关卡信息数据
  * 在0.8.18.0及以后直接用python记录关卡的不可变数据，JSON目前仅用于用户存档
* 支持选择植物卡片
* 支持白昼模式，夜晚模式，泳池模式，浓雾模式（暂时没有加入雾），传送带模式和坚果保龄球模式
* 支持背景音乐播放
  * 支持调节音量
* 支持音效
  * 支持与背景音乐一起调节音量
* 支持全屏模式
  * 按`F`键进入全屏模式，按`U`键恢复至窗口模式
* 支持用小铲子移除植物
* 支持分波生成僵尸
* 支持“关卡进程”进度条显示
* 夜晚模式支持墓碑以及从墓碑生成僵尸
* 含有泳池的模式支持在最后一波时从泳池中自动冒出僵尸
* 支持保存进度
  * Windows下默认进度文件的保存路径为`~\AppData\Roaming\pypvz\userdata.json`
  * 其他操作系统为`~/.config/pypvz/userdata.json`
  * 存档为JSON文件，如果出现因存档损坏而造成程序无法启动，可以手动编辑修复或者删除该文件重试
* 支持错误日志记录
  * Windows下默认日志文件的保存路径为`~\AppData\Roaming\pypvz\run.log`
  * 其他操作系统为`~/.config/pypvz/run.log`
* 支持自定义游戏速度倍率
  * 保存在游戏存档文件中，可以通过修改`game rate`值更改速度倍率
* 游戏完成成就显示
  * 任意一游戏模式全部完成显示银向日葵奖杯
  * 所有模式全部完成显示金向日葵奖杯
  * 光标移动到向日葵奖杯上是显示当前各个模式通关次数
* 含有游戏帮助界面 QwQ

## 环境要求

* `Python3` （建议 >= 3.10，最好使用最新版）
* `Python-Pygame` （建议 >= 2.0，最好使用最新版）

## 方法

* 使用鼠标收集阳光,种植植物
* 对于已经存在存档的用户，可以在`~\AppData\Roaming\pypvz\userdata.json`（Windows）或`~/.config/pypvz/userdata.json`（其他操作系统）中修改当前关卡：
  * 冒险模式：
    * 白昼模式——单行草皮：1
    * 白昼模式——三行草皮：2
    * 白昼模式：3~5
    * 夜晚模式：6~8
    * 泳池模式：9~11
    * 浓雾模式（暂时没有雾）：12
  * 小游戏模式：
    * 坚果保龄球：1
    * 传送带模式（白天）：2
    * 传送带模式（黑夜）：3
    * 传送带模式（泳池）：4
    * 坚果保龄球(II)：5
  * 目前暂时按照以上设定，未与原版相符
* 可以通过修改存档JSON文件中的`game rate`值来调节游戏速度倍率

## 已知bug

以下问题囿于个人目前的能力与精力，没有修复：
* 冷冻的僵尸未用蓝色滤镜标识
  * 这个想不到很好的实现方法，可能会想一种替代方案
* 魅惑的僵尸未用红色滤镜标识
  * 这个可能会作为一种“特性”
* 南瓜头显示不正常
* 墓碑吞噬者吞噬墓碑过程中被吞噬的墓碑顶端不会消失

## 截屏

![截屏1](/screenshots/screenshot-1.webp)
![截屏2](/screenshots/screenshot-2.webp)
![截屏3](/screenshots/screenshot-3.webp)
![截屏4](/screenshots/screenshot-4.webp)
![截屏5](/screenshots/screenshot-5.webp)
![截屏6](/screenshots/screenshot-6.webp)
![截屏7](/screenshots/screenshot-7.webp)
![截屏8](/screenshots/screenshot-8.webp)
![截屏9](/screenshots/screenshot-9.webp)
![截屏10](/screenshots/screenshot-10.webp)
![截屏11](/screenshots/screenshot-11.webp)
![截屏12](/screenshots/screenshot-12.webp)
![截屏13](/screenshots/screenshot-13.webp)
![截屏14](/screenshots/screenshot-14.webp)
![截屏15](/screenshots/screenshot-15.webp)
![截屏16](/screenshots/screenshot-16.webp)
![截屏17](/screenshots/screenshot-17.webp)
![截屏18](/screenshots/screenshot-18.webp)
![截屏19](/screenshots/screenshot-19.webp)
![截屏20](/screenshots/screenshot-20.webp)
![截屏21](/screenshots/screenshot-21.webp)
![截屏22](/screenshots/screenshot-22.webp)
![截屏23](/screenshots/screenshot-23.webp)

## 关于日志与反馈

对于闪退情况，Linux用户与Windows下的python源代码运行用户可以直接在终端中复制出崩溃日志进行反馈。

Windows单文件封装版本无法通过终端显示日志，需要在日志文件中寻找崩溃原因
* Windows默认日志文件路径为`~\AppData\Roaming\pypvz\run.log`
* 其他操作系统为`~/.config/pypvz/run.log`，但一般可以在终端中显示时用终端中的输出即可
