# 致命游戏 · 第一扇门《独自莫凭栏》

单文件浏览器文字冒险游戏，改编自西子绪《死亡万花筒》（网剧名《致命游戏》）的第一个副本——雪村。

**在线游玩：** https://zunyaner.github.io/zhiming-game/

## 声明
- 本作是**非商业同人改编**，与原作者、出版方、影视方都没有关系。
- 游戏里**没有复制原著原文**，所有叙述和对白都是重新写的原创中文文本。剧情大纲根据公开资料整理，拿不准的地方做了模糊或改编处理，详见 [docs/outline.md](docs/outline.md)。

## 玩法
- 线索栏与组合推理、人物名册、可点击的场景探索（三楼、古庙）
- 门内时钟：期限是第 4 日黄昏
- 林秋石 / 阮白洁双视角，两人之间有隐藏的信任值
- 「四句提示」规则解读、规则推演板、与木匠对峙
- 6 个结局（原著路线为真结局）、尾声、重读模式、隐藏成就
- 自动存档 / 手动存档（localStorage），环境声开关（默认关闭）
- 桌面端、移动端都能玩；不依赖任何外部资源

直接打开 `index.html` 就能玩。v3：排版优先、纯文字的恐怖小说质感（无插画）。旧版：[v1-hud.html](v1-hud.html)、[v2-lineart.html](v2-lineart.html)。

## v8 资源来源（全部内嵌于 index.html，离线单文件）
- **场景图片**：15 张场景图（雪林、雾林、破庙神像、火、徽派雪村、雾巷、黑影、木楼走廊、客房、庙外、屋顶、暗巷、古井、老树、神像特写）均由 Grok Bot 图像生成工具原创生成，无第三方素材；转为 WebP（1280×720，q66）后以 data URL 嵌入。程序绘制版保留为后备。
- **书法字体**：Ma Shan Zheng（马善政毛笔楷书），Google Fonts，SIL Open Font License 1.1（见 OFL-MaShanZheng.txt）。已用 fonttools 子集化为游戏实际用到的字符，WOFF2 内嵌，字体名改为 ZBrush 引用。
- **配音**：用 edge-tts（微软 Azure 神经语音 zh-CN-YunjianNeural / XiaoxiaoNeural / YunxiNeural）合成，再用 ffmpeg 降调、加混响，编码为单声道 MP3 内嵌。系统朗读（speechSynthesis）只在解码失败时作为后备。
