# ✈️ 极客硬核技术考据集：民航 ADS-B 航迹、TeX 排版 Bug 与版权页

> **来源**：[Issue #12](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/issues/12)、#57、#229、#317、[PR #182](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/pull/182)、#387

---

## 一、民航 ADS-B 雷达数据实锤（[Issue #12](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/issues/12)）

针对原著中提及的包机行程，专业极客调取了 FlightRadar24 与全球 ADS-B 开源无线电抓取网络数据：
- **执飞日期**：2025-12-21
- **起降航线**：香港国际机场 (HKG) ✈️ 西班牙特内里费南部机场 (TFS)
- **机型**：空中客车 A330-200 (VIP 豪华宽体构型，带独立卧室)
- **航程耗时**：约 15.5 小时
- **真实性印证**：机身编号与停坪照片完全吻合，直接证实了小说中飞往海岛修指甲与贴遮光胶带的真实历史背景。

---

## 二、A330 超载放油与配平物理考据（[Issue #229](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/issues/229) / Kelly 勘误）

原著助理解释：*“A330 是按两百人设计的，我们只有三十个人，太轻了，起飞配平不对，所以要多加油加到够重，到了地方再放掉。”*

### 航空工程师严谨指正：
1. **配平（Weight & Balance）看重心，不看总重**：飞机偏轻不会导致配平失效，只需根据重心调整水平安定面配平轮角度即可；
2. **常规放油违规**：空中放油（Fuel Dumping）是民航遇险紧急迫降时的特情程序，常规航行不能为了减重随意放油；
3. **正确解释**：属于“超重着陆限制下的 Tankering（携油转场）”或“空机配平压舱”。但无论如何，燃油消耗成本 > 100 万美元的结论是绝对精准的。

---

## 三、XeLaTeX 2.37 倍双重行距排版 Bug 修复（[Issue #317](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/issues/317)）

专业 TeX 工程师在阅读源码时抓出的技术瑕疵：
- **Bug 根因**：`main.tex` 中 `\BodySingleLeading` 已经硬编码定义为 17.3pt，但正文宏 `\StoryParagraph` 在调用时又叠加了 `\setstretch{1.3}`；
- **排版后果**：导致实际行距被双重放大到 **22.5pt（相当于 2.37 倍行距溢出）**，严重破坏了 5×8 英寸出版级小开本的紧凑美感；
- **极客 PR**：社区已提交修复补丁，将行距严格校准回经典文学小册子比例。

---

## 四、出版级 GB/T 12451-2006 CIP 版权页（[PR #182](https://github.com/HEJustinSun/my-girlfriend-jingtian-latex/pull/182)）

社区为《我的女友景甜》定制的标准图书在版编目版权页：
- **书名**：《我的女友景甜》
- **著者**：孙宇晨 著
- **出版者**：蒙太奇拉古纳海滩出版社
- **书号**：ISBN 978-7-TRON-2026-X
- **定价**：$50,000,000 USD 或 3.5 μg 卵子（支持 TRX / USDT）
