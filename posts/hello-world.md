# Hello, World!

欢迎来到我的极客博客。这是一篇测试文章，用于验证 Markdown 渲染管线是否正常工作。

## 关于本博客

本博客采用 **内容与代码分离** 的架构：

- Markdown 文件独立存放在 `posts/` 目录
- 前端通过 Fetch API 异步加载 `.md` 文件
- 使用 marked.js 将 Markdown 解析为 HTML
- 使用 highlight.js 为代码块提供语法高亮

## 技术栈

以下是构建本博客所使用的一些核心技术：

1. **marked.js** — Markdown 解析器
2. **highlight.js** — 代码语法高亮
3. **Fetch API** — 异步资源加载
4. **原生 JavaScript** — 无框架依赖

## 示例代码

下面是一段 JavaScript 代码示例：

```javascript
async function loadArticle(mdFilePath) {
  try {
    const response = await fetch(mdFilePath);
    if (!response.ok) {
      throw new Error(`HTTP ${response.status}`);
    }
    const markdown = await response.text();
    const html = marked.parse(markdown);
    document.getElementById('content-container').innerHTML = html;
    hljs.highlightAll();
  } catch (error) {
    console.error('文章加载失败:', error);
  }
}
```

再来看一段 Java 代码：

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        
        for (int i = 0; i < 5; i++) {
            System.out.println("Loop iteration: " + i);
        }
    }
}
```

---

> 这就是"真正的极客工作流"——内容归内容，代码归代码。
