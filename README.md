<div align="center">

![:name](https://count.getloli.com/@astrbot_plugin_memelite_rs?name=astrbot_plugin_memelite_rs&theme=minecraft&padding=6&offset=0&align=top&scale=1&pixelated=1&darkmode=auto)

# astrbot_plugin_memelite_rs

_✨ [astrbot](https://github.com/AstrBotDevs/AstrBot) 表情包制作插件 ✨_  

[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![AstrBot](https://img.shields.io/badge/AstrBot-3.4%2B-orange.svg)](https://github.com/Soulter/AstrBot)
[![GitHub](https://img.shields.io/badge/作者-Zhalslar-blue)](https://github.com/Zhalslar)

</div>

## 💡介绍

- 本插件负责处理聊天机器人与[表情包生成器 meme-generator](https://github.com/MemeCrafters/meme-generator-rs)的对接，具体表情包制作相关资源文件和代码在其仓库中可以找到。
- 本插件使用本地部署的meme-generator。同时尽量保持插件的轻量化，表情包生成快，性能要求低  

## 📦 安装

### 第一步，安装 meme-generator  

- 本插件已支持自动安装meme-generator ，此步可以跳过了。若是发现没能正常安装，可尝试以下方法：
  - 从astrbot控制台安装，pip安装输入框里填写 meme-generator，回车
  - 或者进到astrbot的虚拟环境里并激活虚拟环境（不会的话问AI），运行命令  pip install meme-generator

### 第二步，安装本插件

- 可以直接在astrbot的插件市场搜索astrbot_plugin_memelite_rs，点击安装，耐心等待安装完成即可  

- 或者可以直接克隆源码到插件文件夹：

```bash
# 克隆仓库到插件目录
cd /AstrBot/data/plugins
git clone https://github.com/Zhalslar/astrbot_plugin_memelite_rs

# 控制台重启AstrBot
```

 Docker部署的astrbot，直接安装本插件可能会报错，可能是缺系统依赖，进入容器执行：

```bash
apt-get update && apt-get install -y libgl1 libglib2.0-0
```

之后再安装本插件即可，若是还遇到其他错误，欢迎提issues

### 第三步，下载必要资源

- 从插件配置面板重载插件，首次启动插件会触发资源下载，然后会自动下载两千多张图片，下载速度取决于网速，下载完后插件就能正常使用了
  ![图片](https://github.com/user-attachments/assets/8d6c2fb6-3b79-49b0-ba85-eca1d128ca64)

## ⚙️ 配置

请在astrbot面板配置，插件管理 -> astrbot_plugin_memelite -> 操作 -> 插件配置
![图片](https://github.com/user-attachments/assets/fe3c6adf-f210-4d93-9d8c-a06216507f10)

## ⌨️ 命令

|     命令      |                    说明                    |
|:-------------:|:-----------------------------------------------:|
| /meme帮助      | 查看所有能触发meme合成的关键词  |
| /meme详情 xxx  | 具体查看某个meme的参数         |
|   {关键词}     |   触发meme合成            |
|   禁用meme xxx    |   禁用指定meme           |
|   启用meme xxx    |   启用指定meme           |
|   meme黑名单     |   查看哪些meme被禁用了        |

, 关键词包括：

```plaintext
['5000兆', '戒导', '逆转裁判气泡', '二次元入口', '上瘾', '毒瘾发作', '添乱', '给社会添乱', '一样', '支付宝支付', '一直', '我永远喜欢', '防诱拐',
 '阿尼亚喜欢', '鼓掌', '阿罗娜扔', '升天', '问问', '亚托莉枕头', '继续干活', '打工人', '悲报', 'ba说', '拍头', '揍', '啃', '真寻挨骂', '高血压',
 '蔚蓝档案标题', 'batitle', '波奇手稿', '布洛妮娅举牌', '大鸭鸭举牌', '奶茶', '遇到困难请拨打', '咖波画', '咖波指', '咖波撕', '咖波蹭', '咖波贴'
, '咖波说', '咖波炖', '咖波撞', '咖波头槌', '舰长', '这个引起的', '奖状', '证书', '字符画', '追列车', '追火车', '国旗', '鼠鼠搓', '小丑', '小丑 
面具', '迷惑', '兑换券', '捂脸', '爬', '群青', '白天黑夜', '白天晚上', '像样的亲亲', '入典', '典中典', '黑白草图', '恐龙', '小恐龙', '注意力涣散
, '离婚协议', '离婚申请', '狗都不玩', '管人痴', '不要靠近', '不要按', '别碰', 'douyin', '吃', '皇帝龙图', '意若思镜', '灰飞烟灭', '狂爱', '狂粉粉
, '闭嘴', '我爸爸', '击剑', '🤺', '我打宿傩', '我打宿傩吗', '满脑子', '整点薯条', '流萤举牌', '闪瞎', '红温', '关注', '芙莉莲拿', '哈哈镜', '垃垃
', '垃圾桶', '原神吃', '原神启动', '王境泽', '为所欲为', '馋身子', '切格瓦拉', '谁反对', '假面骑士', '乌鸦哥', '曾小贤', '压力大爷', '你好骚啊啊
, '食屎啦你', '五年怎么过的', '麦克阿瑟说', '喜报', 'google', '谷歌验证码', '猩猩扔', '鬼畜', '手枪', '锤', '凉宫春日举', '高低情商', '低高情商商
, '打穿', '打穿屏幕', '记仇', '抱紧', '抱', '抱抱', '抱大腿', '胡桃啃', '坐牢', '不文明', 'inside', '采访', '杰瑞盯', '急急国王', '汐汐', '今汐汐
, '啾啾', '跳', '万花筒', '万花镜', '凯露指', '远离', '压岁钱不要交给', '踢球', '卡比锤', '卡比重锤', '亲', '亲亲', '可莉吃', '敲', '心奈印章',,
 '泉此方看', '偷学', '左右横跳', '让我进去', '舔糖', '舔棒棒糖', '等价无穷小', '听音乐', '小天使', '加载中', '看扁', '看图标', '循环', '寻狗启事
, '永远爱你', '洛天依要', '天依要', '洛天依说', '天依说', '罗永浩说', '鲁迅说', '鲁迅说过', '真寻看书', '旅行伙伴觉醒', '旅行伙伴加入', '交个朋朋
', '结婚申请', '结婚登记', '流星', '米哈游', '上香', '低语', '我朋友说', '我的意见如下', '我的意见是', '我老婆', '这是我老婆', '纳西妲啃', '草草
啃', '亚文化取名机', '亚名', '需要', '你可能需要', '猫羽雫举牌', '猫猫举牌', '伊地知虹夏举牌', '虹夏举牌', '诺基亚', '有内鬼', '请假条', '不喊喊
', '无响应', '我推的网友', 'osu', 'out', '加班', '女神异闻录5预告信', 'p5预告信', '这像画吗', '小画家', '熊猫龙图', '推锅', '甩锅', '拍', '佩   
佩举', '完美', '摸', '摸摸', '摸头', 'rua', '捏', '捏脸', '像素化', 'pjsk', '世界计划', '普拉娜吃', '普拉娜舔', '顶', '玩', '玩游戏', '一起玩', 
'出警', '警察', 'ph', 'pornhub', '土豆', '捣', '打印', '舔', '舔屏', 'prpr', '可达鸭', '打拳', '四棱锥', '金字塔', '举', '举牌', '看书', '复读',
 '撕', '怒撕', '诈尸', '秽土转生', '滚', '三维旋转', '贴', '贴贴', '蹭', '蹭蹭', '快跑', '快逃', '安全感', '催眠app', '刮刮乐', '挠头', '滚屏', 
'世界第一可爱', '晃脑', '白子舔', '震惊', '别说了', '坐得住', '坐的住', '一巴掌', '口号', '砸', '卖掉了', '无语', '盯着你', 'steam消息', '踩', '
炖', '科目三', '吸', '嗦', '精神支柱', '回旋转', '旋风转', '对称', '唐可可举牌', '嘲讽', '讲课', '敲黑板', '拿捏', '戏弄', '望远镜', '体温枪', '
想什么', '这是鸡', '🐔', '丢', '扔', '抛', '掷', '捶', '捶爆', '爆捶', '紧贴', '紧紧贴着', '该走了', '一起', '上坟', '坟前比耶', '汤姆嘲笑', '顶
', '恍惚', '转', '搓', '万能表情', '空白表情', '反了', '震动', '好起来了', '墙纸', '胡桃平板', '胡桃放大', '洗衣机', '波纹', '微信支付', '最想想
的东西', '我想上的', '为什么@我', '为什么要有手', '风车转', '许愿失败', '木鱼', '膜', '膜拜', '吴京中国', '椰树椰汁', '你的跨年', 'yt', 'youtu ube', 
'致电', '你应该致电']

```

## 🐔 使用说明

- 本插件支持从原始消息中提取参数，请用空格隔开参数，如 “喜报 nmsl”
- 本插件支持从引用消息中提取参数，如“[引用的消息] 喜报”
- 提供的参数不够时，插件自动获取消息发送者、被 @ 的用户以及 bot 自身的相关参数来补充。
示例
![b421d15916a8db6109bb36c002ba2e5](https://github.com/user-attachments/assets/ec15b5f7-eec2-4552-814d-60dcc4196713)

## 📌 注意事项

- 本插件已换用meme-generator的rust重构版，旧版用户更新需重新下载资源。
- 如果想第一时间得到反馈，请进作者的插件反馈群（QQ群）：460973561

## 👥 贡献指南

- 🌟 Star 这个项目！（点右上角的星星，感谢支持！）
- 🐛 提交 Issue 报告问题
- 💡 提出新功能建议
- 🔧 提交 Pull Request 改进代码

## 🐍 额外表情安装教程（如'射','撅'）

> 步骤繁琐，没有需要的话就别装。

> 实在想装的话就好好看文档，别来烦作者。

> 实在想找作者的话，先点个star再说，没点的不给予理会。

> 已经写得很详细了，还是不会的话建议放弃。

### 第一步，下载动态链接库  

前往[meme-generator 额外表情动态链接库](https://github.com/MemeCrafters/meme-generator-contrib-rs/actions) 往下滑找到动态链接库，根据你的环境选择对应版本，如图示例：
![tmp1CF8](https://github.com/user-attachments/assets/fbb39f01-8a25-4602-90a1-629876cc13e8)
下载完后解压得到的.so后缀文件，这个文件就是所需的动态链接库。

### 第二步，动态链接库放置于 $MEME_HOME/libraries 文件夹下（libraries文件夹若不存在则新建一个）

$MEME_HOME 默认位置为 $HOME/.meme_generator

不同系统下的 $HOME 目录为：

    Linux: /home/<username>
    MacOS: /Users/<username>
    Windows: C:\Users\<username>

Linux和windows的示例路径：
![tmp41F5](https://github.com/user-attachments/assets/ffbcb3d5-d971-409f-ba2e-86db76a6a9d6)

### 第三步，在 配置文件 将 load_external_memes 设置为 true

打开config.toml文件，将下面的内容复制粘贴进去即可（当然其他配置你也可以根据个人喜好更改）

```plaintext
[meme]
load_builtin_memes = true  # 是否加载内置表情包
load_external_memes = true  # 是否加载外部表情包
meme_disabled_list = []  # 禁用的表情包列表，填写表情的 `key`

[resource]
resource_url = "https://cdn.jsdelivr.net/gh/MemeCrafters/meme-generator-rs@"  # 下载内置表情包图片/字体时的资源链接
download_fonts = true  # 是否下载字体

[font]
use_local_fonts = true  # 是否使用本地文件夹下的字体
default_font_families = ["Noto Sans SC", "Noto Color Emoji"]  # 默认字体

[encoder]
gif_max_frames = 200  # 限制生成的 gif 帧数
gif_encode_speed = 29  # gif 编码速度，范围为 1 ~ 30，数字越大，编码速度越快，但图片质量越差

[api]
baidu_trans_appid = ""  # 百度翻译api相关，部分表情需要使用
baidu_trans_apikey = ""  # 可在 百度翻译开放平台 (http://api.fanyi.baidu.com) 申请

[server]
host = "0.0.0.0"  # web server 监听地址
port = 2233  # web server 端口
```

### 第四步，下载图片/字体资源并放置于 $MEME_HOME/resources 文件夹下

如图在Linux下的示例操作：

![tmp6EA4](https://github.com/user-attachments/assets/e141c05b-8996-451a-b85d-55b1e7891ccb)

### 第五步，重启astrbot

## 🔗 相关链接

- [meme-generator](https://github.com/MemeCrafters/meme-generator-contrib-rs) 表情包生成器
- [meme-generator的rust重构版](https://github.com/MemeCrafters/meme-generator-contrib-rs) 表情包生成器的rust重构版
- [meme-generator 额外表情仓库](https://github.com/MemeCrafters/meme-generator-contrib)
- [meme-generator-rs 额外表情仓库](https://github.com/MemeCrafters/meme-generator-contrib-rs)
- [nonebot-plugin-memes](https://github.com/MemeCrafters/nonebot-plugin-memes) 表情包生成器 meme-generator 的 Nonebot2 对接插件
- [Astrbot](https://astrbot.app/) 易于上手的多平台聊天机器人及开发框架。
