# 哈尔滨工业大学（深圳）概率论与数理统计课程小论文模板

本模板基于 [Typst Universe](https://typst.app/universe) 上的 [全国大学生数学建模竞赛 Typst 模板](https://typst.app/universe/package/cumcm-muban) 进行修改，专门适配哈尔滨工业大学（深圳）概率论与数理统计课程小论文的格式要求。

## 📝 模板说明

本模板主要修改内容：

- **封面设计**：重新设计封面，包含课程小论文标题、题目、班号、学号、姓名、日期和成绩信息表格
- **字体设置**：
  - 封面表格：汉字黑体小二号（18pt），字母和数字 Times New Roman 小二号（18pt）
  - 标题部分：汉字宋体三号加粗（16pt），字母和数字 Times New Roman 三号加粗（16pt）
  - 摘要内容和关键词：汉字宋体小四号（12pt），字母和数字 Times New Roman 小四号（12pt）
  - 正文部分：汉字宋体小四号（12pt），字母和数字 Times New Roman 小四号（12pt）
- **页边距**：默认 2.5cm
- **参数调整**：移除了原模板的 `member` 参数，新增 `name`（姓名）、`student-id`（学号）、`class-id`（班号）参数

## 🚀 快速开始


### 本地使用（推荐）

1. 安装 [Visual Studio Code](https://code.visualstudio.com/)
2. 安装 VSCode 扩展：[Tinymist Typst](https://marketplace.visualstudio.com/items?itemName=myriad-dreamin.tinymist)
3. 克隆或下载本模板
4. 使用 VSCode 打开项目文件夹
5. 编辑 `main.typ` 文件
6. 使用扩展功能进行实时预览和编译
7. 注意，由于 [全国大学生数学建模竞赛 Typst 模板](https://typst.app/universe/package/cumcm-muban)只目前支持到Typst 0.13，在某些情况下Tinymist需要使用历史版本

### 在线使用
1. 访问 [Typst Web App](https://typst.app/)
2. 上传本模板文件
3. 修改 `main.typ` 中的个人信息
4. 开始编写您的论文



## 📁 文件结构

```
probability-typst-template/
├── main.typ          # 主文件（论文内容）
├── lib.typ           # 模板定义文件
├── refs.bib          # 参考文献
├── README.md         # 说明文档
├── fonts/            # 字体文件夹
│   ├── Sim/          # 中易字体（宋体、黑体、楷体）
│   └── TimesNewRoman/
└── figures/          # 图片文件夹
```

## 🔧 使用方法

在 `main.typ` 文件中配置您的论文信息：

```typst
#import "./lib.typ": *
#show: thmrules

#show: probability.with(
  title: "您的论文题目",
  name: "张三",                    // 姓名
  student-id: "23**********",      // 学号
  class-id: "23******",            // 班号
  date: datetime(year: 2024, month: 12, day: 1),
  cover-display: true,             // 是否显示封面
  
  abstract: [
    这里是摘要内容...
  ],
  keywords: ("关键词1", "关键词2", "关键词3"),
)

// 正文内容
= 引言

您的论文内容...

// 参考文献
#bibliography("refs.bib")
```

## 🎨 字体说明

本模板使用以下字体：

- **中文字体**：SimSun（中易宋体）、SimHei（中易黑体）、SimKai（中易楷体）
- **英文字体**：Times New Roman
- **代码字体**：DejaVu Sans Mono



### macOS 字体安装方法

1. 打开 `fonts` 文件夹
2. 双击 `.ttf` 字体文件
3. 在弹出的"字体册"窗口中点击"安装字体"
4. 重启 Typst 或重新编译文档

### 检查字体是否安装

```bash
# macOS/Linux
fc-list | grep -i "simsun"
fc-list | grep -i "simhei"
fc-list | grep -i "times"
```

## 📚 功能特性

### 定理环境

模板提供了多种定理环境：

```typst
#definition[
  这是一个定义。
]

#theorem[
  这是一个定理。
]

#lemma[
  这是一个引理。
]

#corollary[
  这是一个推论。
]

#proposition[
  这是一个命题。
]
```

### 图片插入

```typst
#figure(
  image("figures/example.png", width: 80%),
  caption: [图片标题]
)
```

### 表格插入

```typst
#figure(
  table(
    columns: 3,
    [列1], [列2], [列3],
    [数据1], [数据2], [数据3],
  ),
  caption: [表格标题]
)
```

### 参考文献

在 `refs.bib` 文件中添加文献条目，然后在正文中引用：

```typst
根据文献@citation-key的研究...

#bibliography("refs.bib")
```

## ⚖️ 许可协议

本模板基于 **Apache License 2.0** 开源协议发布。

原始模板来源：[cumcm-muban](https://typst.app/universe/package/cumcm-muban)（全国大学生数学建模竞赛 Typst 模板）


## 🙏 致谢

- 原始模板：[cumcm-muban](https://typst.app/universe/package/cumcm-muban)
- 排版系统：[Typst](https://typst.app/)

## 📮 反馈与贡献

如果您在使用过程中遇到问题或有改进建议，欢迎提交 Issue 或 Pull Request。

## 📖 相关资源

- [Typst 官方文档](https://typst.app/docs/)
- [Typst 中文社区](https://github.com/typst-cn)
- [Typst Universe](https://typst.app/universe) - 模板和包市场

---

**祝您写作顺利！** 📚✨

