# 塔罗牌图片资源说明

## 图片来源

- **原始仓库**: https://github.com/metabismuth/tarot-json
- **图片规格**: JPEG, 350×600 像素, 每张约 100KB
- **牌组版本**: Rider-Waite-Smith (韦特版)，**公版素材**，可自由商用
- **总计**: 78 张（22 大阿卡纳 + 56 小阿卡纳）
- **下载时间**: 2026-07-03

## 版权说明

Rider-Waite 塔罗牌初次出版于 **1909 年**，作者 A.E. Waite 和 Pamela Colman Smith。根据美国和大多数国家的版权法（作者去世后 70 年），此牌组已进入**公共领域（Public Domain）**，可自由使用于任何用途（包括商业用途）。

## 命名规则

| 前缀 | 花色 | 编号范围 | 数量 |
|------|------|----------|------|
| `m` | 大阿卡纳 (Major Arcana) | m00 - m21 | 22 张 |
| `w` | 权杖 (Wands) | w01 - w14 | 14 张 |
| `c` | 圣杯 (Cups) | c01 - c14 | 14 张 |
| `s` | 宝剑 (Swords) | s01 - s14 | 14 张 |
| `p` | 星币 (Pentacles) | p01 - p14 | 14 张 |

**小阿卡纳编号意义** (适用于 w/c/s/p 前缀)：
- 01 = A（Ace，一）
- 02-10 = 数字 2-10
- 11 = 侍从（Page）
- 12 = 骑士（Knight）
- 13 = 王后（Queen）
- 14 = 国王（King）

## 完整对照表

### 大阿卡纳 22张

| 文件名 | 牌名（英）| 牌名（中）|
|--------|-----------|-----------|
| m00.jpg | The Fool | 愚者 |
| m01.jpg | The Magician | 魔术师 |
| m02.jpg | The High Priestess | 女祭司 |
| m03.jpg | The Empress | 皇后 |
| m04.jpg | The Emperor | 皇帝 |
| m05.jpg | The Hierophant | 教皇 |
| m06.jpg | The Lovers | 恋人 |
| m07.jpg | The Chariot | 战车 |
| m08.jpg | Strength | 力量 |
| m09.jpg | The Hermit | 隐者 |
| m10.jpg | Wheel of Fortune | 命运之轮 |
| m11.jpg | Justice | 正义 |
| m12.jpg | The Hanged Man | 倒吊人 |
| m13.jpg | Death | 死神 |
| m14.jpg | Temperance | 节制 |
| m15.jpg | The Devil | 恶魔 |
| m16.jpg | The Tower | 塔 |
| m17.jpg | The Star | 星星 |
| m18.jpg | The Moon | 月亮 |
| m19.jpg | The Sun | 太阳 |
| m20.jpg | Judgement | 审判 |
| m21.jpg | The World | 世界 |

### 权杖 14张（Wands）

| 文件名 | 牌名（英）| 牌名（中）|
|--------|-----------|-----------|
| w01.jpg | Ace of Wands | 权杖一 |
| w02.jpg | Two of Wands | 权杖二 |
| w03.jpg | Three of Wands | 权杖三 |
| w04.jpg | Four of Wands | 权杖四 |
| w05.jpg | Five of Wands | 权杖五 |
| w06.jpg | Six of Wands | 权杖六 |
| w07.jpg | Seven of Wands | 权杖七 |
| w08.jpg | Eight of Wands | 权杖八 |
| w09.jpg | Nine of Wands | 权杖九 |
| w10.jpg | Ten of Wands | 权杖十 |
| w11.jpg | Page of Wands | 权杖侍从 |
| w12.jpg | Knight of Wands | 权杖骑士 |
| w13.jpg | Queen of Wands | 权杖王后 |
| w14.jpg | King of Wands | 权杖国王 |

### 圣杯 14张（Cups）

| 文件名 | 牌名（英）| 牌名（中）|
|--------|-----------|-----------|
| c01.jpg | Ace of Cups | 圣杯一 |
| c02-c10.jpg | Two-Ten of Cups | 圣杯二 - 圣杯十 |
| c11.jpg | Page of Cups | 圣杯侍从 |
| c12.jpg | Knight of Cups | 圣杯骑士 |
| c13.jpg | Queen of Cups | 圣杯王后 |
| c14.jpg | King of Cups | 圣杯国王 |

### 宝剑 14张（Swords）

| 文件名 | 牌名（英）| 牌名（中）|
|--------|-----------|-----------|
| s01.jpg | Ace of Swords | 宝剑一 |
| s02-s10.jpg | Two-Ten of Swords | 宝剑二 - 宝剑十 |
| s11.jpg | Page of Swords | 宝剑侍从 |
| s12.jpg | Knight of Swords | 宝剑骑士 |
| s13.jpg | Queen of Swords | 宝剑王后 |
| s14.jpg | King of Swords | 宝剑国王 |

### 星币 14张（Pentacles）

| 文件名 | 牌名（英）| 牌名（中）|
|--------|-----------|-----------|
| p01.jpg | Ace of Pentacles | 星币一 |
| p02-p10.jpg | Two-Ten of Pentacles | 星币二 - 星币十 |
| p11.jpg | Page of Pentacles | 星币侍从 |
| p12.jpg | Knight of Pentacles | 星币骑士 |
| p13.jpg | Queen of Pentacles | 星币王后 |
| p14.jpg | King of Pentacles | 星币国王 |

## 使用示例（网页）

```html
<!-- 显示"愚者" -->
<img src="./牌面图片_韦特版/m00.jpg" alt="The Fool 愚者" />

<!-- 显示"权杖国王" -->
<img src="./牌面图片_韦特版/w14.jpg" alt="King of Wands 权杖国王" />
```

## 逆位图片处理

塔罗牌的**逆位**在展示时是把正位图片**旋转180°**。不需要额外准备逆位图片，用 CSS 就能搞定：

```css
.card-reversed {
    transform: rotate(180deg);
}
```

## 高清版本源

如需 1144×1919 高清版本，可从 Wikimedia Commons 下载（每张 1MB+）：
- 命名格式：`https://upload.wikimedia.org/wikipedia/commons/9/90/RWS_Tarot_00_Fool.jpg`
- 全套下载: https://commons.wikimedia.org/wiki/Category:Rider-Waite_tarot_deck
