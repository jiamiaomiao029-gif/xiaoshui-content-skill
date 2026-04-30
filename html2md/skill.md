# html2md

将 HTML 文件转换为 Markdown 格式。

## 使用方式

```
/html2md <html文件路径>
/html2md <html文件路径> <输出md文件路径>
```

## 功能

- 读取 HTML 文件内容
- 转换为干净的 Markdown 格式
- 保留标题、段落、列表、链接、图片等结构
- 自动清理多余的空白和格式
- 可选择输出到指定文件或显示在对话中

## 示例

```bash
# 转换并显示结果
/html2md index.html

# 转换并保存到指定文件
/html2md index.html output.md

# 批量转换当前目录下所有 HTML
/html2md *.html
```

## 转换规则

- `<h1>` → `# 标题`
- `<h2>` → `## 标题`
- `<p>` → 段落文本
- `<a>` → `[文本](链接)`
- `<img>` → `![alt](src)`
- `<ul>/<ol>` → 列表
- `<code>` → 行内代码
- `<pre>` → 代码块
- `<strong>/<b>` → **粗体**
- `<em>/<i>` → *斜体*

---

model: sonnet
