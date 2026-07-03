# 中国算命术开源数据集

**Chinese Fortune-Telling & Tarot Open Dataset**

一个为「算命/占卜类网页应用」准备的开源数据集，覆盖中国传统命理（八字/紫微/六爻/梅花易数/相术）+ 西方塔罗牌，包含**规则表、算法参考、图片素材、古籍原文**四大类资料。

---

## 🎯 项目目标

给准备做算命/占卜网页的开发者一个「开箱即用」的数据参考库。所有资料要么是**公版古籍/知识**（几百年历史），要么来自**MIT/AGPL 等开源许可**的项目。

**本项目不实现具体算法，只做数据收集和整理。** 需要计算功能时，请引用文末列出的开源库。

---

## 📁 目录结构

```
fortune-telling-research/
│
├── README.md                        # ← 本文件（总入口）
│
├── 01-overview.md                   # 中国算命术整体框架（五术 = 山医命相卜）
├── 02-methods-detail.md             # 10 种算命方法详解 + 网页可行性评级
├── 03-web-design-notes.md           # 网页产品设计参考（4 种定位 + 技术栈 + 合规风险）
│
├── raw/                             # 维基百科原始 HTML（13 条目）
├── text/                            # 提取的纯文本
│
└── 开发资料/                        # ⭐ 核心 · 开发级规则表和数据库
    │
    ├── README.md                    # 开发资料索引
    │
    ├── 1_八字命理/                  # 【自研规则表 6 份】
    │   ├── 排盘规则.md              #   年月日时四柱排法（核心）
    │   ├── 天干地支表.txt           #   10干+12支+60甲子+藏干
    │   ├── 五行生克表.txt           #   相生相克 + 颜色方位季节
    │   ├── 十神关系表.txt           #   比劫食伤财官印枭
    │   ├── 地支六冲六合表.txt       #   冲/合/三合/三会/刑/害/破
    │   └── 真太阳时修正说明.txt     #   经度时差 + 均时差 + 21 城市对照
    │
    ├── 2_梅花易数/                  # 【自研规则表 4 份】
    │   ├── 起卦规则.md              #   时间/数字/字数起卦
    │   ├── 先天八卦序数表.txt       #   乾兑离震巽坎艮坤 = 1-8
    │   ├── 六十四卦卦名与卦象表.txt #   全 64 卦完整对照
    │   └── 体用生克断法.md          #   断卦核心逻辑
    │
    ├── 3_六爻预测/                  # 【自研规则表 4 份】
    │   ├── 摇卦规则.md              #   三枚铜钱 6 次投掷
    │   ├── 纳甲与六亲配置表.txt     #   八宫 + 纳甲 + 六亲判定
    │   ├── 世应定位规则.txt         #   64 卦世应位置
    │   └── 用神取法说明.md          #   不同占事的用神
    │
    ├── 4_塔罗牌/                    # 【核心数据 · 图 + JSON】
    │   ├── 韦特塔罗78张牌意库_原版英文.json  # ⭐ Mark McElroy 完整版
    │   ├── 韦特塔罗78张牌意库_中文.json      #   自研中文精简版
    │   ├── 牌阵说明（单张三张凯尔特十字等）.md  # 10 种牌阵
    │   ├── 正逆位关键词索引.txt      #   78 张牌关键词速查
    │   └── 牌面图片_韦特版/          # ⭐ 78 张塔罗牌图（350×600 JPG，公版）
    │       ├── README.md
    │       ├── m00.jpg - m21.jpg    #   大阿卡纳 22 张
    │       ├── w01.jpg - w14.jpg    #   权杖 14 张
    │       ├── c01.jpg - c14.jpg    #   圣杯 14 张
    │       ├── s01.jpg - s14.jpg    #   宝剑 14 张
    │       └── p01.jpg - p14.jpg    #   星币 14 张
    │
    ├── 古籍原文/                    # 【维基文库原文，公版】
    │   ├── 三命通会_维基文库.html   #   八字命理古典
    │   ├── 渊海子平_维基文库.html   #   八字命理古典（313KB）
    │   └── 麻衣神相_维基文库.html   #   相术古典
    │
    └── 开源库/                      # 【从 GitHub 收集的可直接引用的库/数据】
        │
        ├── lunar-javascript/         # ⭐ 6tail/lunar-javascript（1587⭐）
        │   ├── lunar.js              #   万年历+农历+八字+节气+黄历（435KB）
        │   ├── demo.html
        │   ├── README.md
        │   └── LICENSE               #   MIT
        │
        ├── ziwei-doushu-data/        # ⭐ Renhuai123/ziwei-doushu（2711⭐）
        │   ├── ziwei_algorithm.ts    #   紫微斗数排盘算法
        │   ├── ziwei_patterns.ts     #   格局知识库（54KB）
        │   ├── ziwei_sihua.ts        #   四化系统
        │   ├── ziwei_heming-knowledge.ts  # 何鸣命理知识库
        │   ├── nihai_tianji.ts       #   倪海夏《天纪》天卷（40KB）
        │   ├── nihai_diji.ts         #   倪海夏《天纪》地卷
        │   ├── nihai_renji.ts        #   倪海夏《天纪》人卷（49KB）
        │   └── ...
        │
        ├── liuyao-references/        # ⭐ rgvsp1993/liuyao-divination（12⭐）
        │   ├── gua-ci.md             #   64 卦卦辞（朱熹《周易本义》22KB）
        │   ├── yao-ci.md             #   384 爻爻辞
        │   ├── najia-table.md        #   纳甲表
        │   ├── shiyao-table.md       #   世应表
        │   ├── liuqin-rules.md       #   六亲规则
        │   ├── liushen-rules.md      #   六神规则
        │   ├── duangua-core.md       #   断卦核心
        │   ├── duangua-advanced.md   #   断卦进阶
        │   └── 《小白教程如何复现算卦技能》.md
        │
        └── dreamhunter-divination/   #   dreamhunter2333/chatgpt-tarot-divination（826⭐）
            ├── tarot.py              #   塔罗 prompt
            ├── plum_flower.py        #   梅花易数 prompt
            ├── name.py               #   姓名五格 prompt
            ├── dream.py              #   周公解梦 prompt
            ├── birthday.py           #   生辰八字 prompt
            ├── fate.py               #   综合命理 prompt
            └── new_name.py           #   起名 prompt
```

---

## 🚀 快速开始

**如果你要做算命网页，从这里开始：**

| 你想做的事 | 看哪个文件 |
|-----------|-----------|
| 理解中国算命全貌 | `01-overview.md` |
| 挑选做哪种算命 | `02-methods-detail.md`（含可行性评级）|
| 产品定位/合规 | `03-web-design-notes.md` |
| 开始写代码 | `开发资料/README.md` |
| 直接引用现成算法 | `开发资料/开源库/`（4 个仓库）|

---

## 📊 数据概览

| 类别 | 文件数 | 数据量 |
|------|--------|--------|
| 自研规则表（八字/梅花/六爻/塔罗）| 19 | 130 KB |
| 塔罗牌图片（78 张 JPG）| 79 | 8.6 MB |
| 开源库（6tail/Renhuai/rgvsp/dreamhunter）| 30+ | 830 KB |
| 古籍原文 HTML（渊海子平/三命通会/麻衣神相）| 3 | 408 KB |
| 维基百科原始资料（13 条目）| 26 | 1.3 MB |
| **合计** | **150+** | **12 MB** |

---

## ⚙️ 推荐 MVP 开发顺序

| 优先级 | 方法 | 数据完备度 | 复杂度 | 建议 |
|-------|------|-----------|--------|------|
| 🟢 P0 | 塔罗 | 100%（图+牌意+牌阵齐全）| ★ | 首选，一周可上线 |
| 🟢 P0 | 梅花易数 | 100%（规则+64卦齐全）| ★★ | 免排盘，起卦即断 |
| 🟡 P1 | 八字 | 95%（自研+lunar.js 库）| ★★★ | 需接入 lunar.js |
| 🟡 P1 | 六爻 | 100%（rgvsp1993 库+自研）| ★★★★ | 数据最全 |
| 🔴 P2 | 紫微斗数 | 90%（ziwei-doushu 库）| ★★★★★ | 最复杂 |
| 🔴 P2 | 姓名/星座/黄历 | 部分（lunar.js+prompt）| ★★ | 辅助功能 |

---

## 📚 数据来源与授权

### 自研规则表（19 份）
- **授权**：CC0（公共领域）
- **依据**：几百年历史的传统命理常识，无版权

### 塔罗牌图片
- **来源**：https://github.com/metabismuth/tarot-json
- **原图**：Rider-Waite-Smith 塔罗牌（1909 年出版，已进入公版）
- **可商用**：是（公共领域）

### 塔罗牌意 JSON
- **来源**：Mark McElroy《A Guide to Tarot Meanings》
- **原网址**：http://www.madebymark.com/a-guide-to-tarot-card-meanings/
- **许可**：Corpora Project 公开数据

### 开源库

| 库 | 星标 | 许可 | 用途 |
|----|------|------|------|
| [6tail/lunar-javascript](https://github.com/6tail/lunar-javascript) | 1587⭐ | MIT | 万年历+农历+节气+八字+黄历 |
| [Renhuai123/ziwei-doushu](https://github.com/Renhuai123/ziwei-doushu) | 2711⭐ | 见 LICENSE | 紫微斗数完整排盘+格局 |
| [rgvsp1993-commits/liuyao-divination](https://github.com/rgvsp1993-commits/liuyao-divination) | 12⭐ | 无 LICENSE（引用需注明）| 六爻完整数据（朱熹《周易本义》整理版）|
| [dreamhunter2333/chatgpt-tarot-divination](https://github.com/dreamhunter2333/chatgpt-tarot-divination) | 826⭐ | 见 LICENSE | LLM 占卜 prompt 参考 |
| [metabismuth/tarot-json](https://github.com/metabismuth/tarot-json) | 少量 | 无 LICENSE | 塔罗图片素材 |
| [dariusk/corpora](https://github.com/dariusk/corpora) | 4.5k⭐ | CC0 | 塔罗牌意 JSON |

### 古籍原文
- **来源**：中文维基文库（zh.wikisource.org）
- **抓取时间**：2026-07-03
- **授权**：公共领域

### 维基百科原始条目
- **来源**：zh.wikipedia.org
- **抓取时间**：2026-07-03
- **授权**：CC-BY-SA 3.0

---

## ⚠️ 合规提示（重要）

**中华人民共和国刑法背景下，做算命类产品有明确红线：**

- ❌ **禁止：** 付费"改运"、"化解灾祸"、"消灾解难"等特定人事的确定性预测（有诈骗定罪风险）
- ❌ **禁止：** 销售"开运物"、"符咒"、"化煞物"（涉及封建迷信+虚假宣传）
- ❌ **禁止：** 承诺具体人事的因果预言（"你三年内必有一次牢狱之灾"这类）
- ✅ **建议：** 定位为**娱乐/文化科普/心理暗示工具**
- ✅ **建议：** 界面显眼位置声明"仅供娱乐参考，不构成任何指导意见"
- ✅ **建议：** 若涉及付费，仅收取「工具使用费」而非「预测服务费」

详见 `03-web-design-notes.md` 的合规风险章节。

---

## 🔄 更新历史

| 日期 | 版本 | 说明 |
|------|------|------|
| 2026-07-03 | v0.1 | 初始版本：维基百科 13 条目 + 网页设计参考 |
| 2026-07-03 | v0.2 | 补充自研规则表（19 份，八字/梅花/六爻/塔罗）|
| 2026-07-03 | v0.3 | 补充塔罗牌 78 张公版图片 |
| 2026-07-03 | v0.4 | 补充开源库（lunar.js/ziwei-doushu/liuyao-refs/dreamhunter）+ 古籍原文 |

---

## 🙋 关于本项目

- **维护者**：@luojingwei123 + Claude (Anthropic)
- **性质**：非商业开源资料集
- **欢迎**：Issue / PR / 补充新的开源数据源
- **不接受**：付费开运物销售、算命预测服务对接

---

## 📖 更多阅读

- [中国传统命理学（维基百科）](https://zh.wikipedia.org/wiki/%E4%BC%AA%E7%A7%91%E5%AD%B8)
- [塔罗牌（维基百科）](https://zh.wikipedia.org/wiki/%E5%A1%94%E7%BE%85%E7%89%8C)
- [Rider-Waite Tarot Deck（Wikimedia）](https://commons.wikimedia.org/wiki/Category:Rider-Waite_tarot_deck)
