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

## 快速加入词典

在编辑模式中选中文本后右键选择「加入 HanBoundary 词典」。菜单会对包含中文、英文或数字的文字选区显示；实际加入时请只选中一个不含空格或换行的词或术语。插件会把它保存到本地 Jieba 用户词典，并在开启「使用结巴分词」时立即加入当前分词器；重复添加不会产生重复条目。这个操作只修改插件设置，不会修改笔记内容。

## 署名

本插件保留了原 `Word Splitting for Simplified Chinese in Edit Mode and Vim Mode` 插件的核心实现，并在其基础上加入预览表格分词。

- 上游项目：[AidenLx/cm-chs-patch](https://github.com/AidenLx/cm-chs-patch)
- 上游作者：AidenLx
- 上游许可证：MIT

发布时请同时保留上游项目的署名和许可证要求。
