# 汉界 HanBoundary

Obsidian 中文分词插件，合并了以下功能：

- 编辑模式中的简体中文词语移动与选择；
- Vim 模式中的中文词语移动；
- 预览模式表格中的中文语义换行。

预览表格会优先保持 Jieba 识别出的词块完整，例如：

```text
持续
监控
```

而不是在词语内部拆开。插件设置默认使用 Jieba；首次使用时，原编辑模式分词插件所需的 Jieba WASM 会按原流程加载。

## 安装

将 `main.js`、`manifest.json` 和 `styles.css` 放入：

```text
.obsidian/plugins/han-boundary/
```

然后在 Obsidian 的第三方插件设置中启用 `汉界 HanBoundary`。

表格颜色、表头和第一列样式仍由独立的 `komaki-table` CSS snippet 控制。

## 署名

本插件保留了原 `Word Splitting for Simplified Chinese in Edit Mode and Vim Mode` 插件的核心实现，并在其基础上加入预览表格分词。

- 上游项目：[AidenLx/cm-chs-patch](https://github.com/AidenLx/cm-chs-patch)
- 上游作者：AidenLx
- 上游许可证：MIT

发布时请同时保留上游项目的署名和许可证要求。
