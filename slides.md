---
theme: default
background: "#e8f7ea"
class: text-center
highlighter: shiki
lineNumbers: false
---

<style>
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin: 0.3rem 0.45rem;
  padding: 0.85rem 1.4rem;
  border-radius: 999px;
  border: 1px solid #6ec68d;
  color: #1f5135;
  background: rgba(118,200,147,0.18);
  text-decoration: none;
  font-weight: 700;
  transition: transform .18s ease, background .18s ease, box-shadow .18s ease;
}
.btn:hover {
  transform: translateY(-2px);
  background: rgba(118,200,147,0.32);
  box-shadow: 0 10px 20px rgba(25,93,48,0.12);
}
.card,
.slide-card {
  margin: 0.1rem auto 0.8rem;
  max-width: 1080px;
  padding: 1.5rem 1.6rem;
  border-radius: 30px;
  background: rgba(255,255,255,0.96);
  border: 1px solid rgba(118,200,147,0.20);
  box-shadow: 0 20px 60px rgba(39, 99, 57, 0.10);
  text-align: left;
  max-height: calc(100vh - 1.4rem);
  overflow-y: auto;
}
html,
body,
section,
.slide,
.page,
.layout,
.theme-default {
  align-items: flex-start !important;
  justify-content: flex-start !important;
  padding-top: 0 !important;
  padding-bottom: 0 !important;
  min-height: 100vh !important;
  height: 100vh !important;
}
.slide,
.page {
  overflow: hidden !important;
}
.slide .slide-card,
.page .slide-card {
  margin-top: -2rem!important;
}
.card-header {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 0.8rem;
  margin-bottom: 0.9rem;
}
.tag {
  display: inline-flex;
  align-items: center;
  padding: 0.5rem 0.95rem;
  border-radius: 999px;
  background: #e5f7e8;
  border: 1px solid rgba(46, 134, 72, 0.16);
  color: #1e593b;
  font-weight: 700;
}
.title {
  font-size: 3rem;
  margin: 0;
  color: #184e34;
}
.subtitle {
  margin: 0.35rem 0 0;
  font-size: 1.15rem;
  color: #3c5c48;
  line-height: 1.6;
}
.summary {
  display: grid;
  grid-template-columns: repeat(2, minmax(200px, 1fr));
  gap: 0.8rem;
  margin-top: 1rem;
}
.meta {
  padding: 0.95rem 1rem;
  border-radius: 22px;
  background: #f6fff4;
  border: 1px solid rgba(118,200,147,0.18);
  color: #1f5135;
}
.meta strong {
  display: block;
  margin-bottom: 0.4rem;
  font-size: 1rem;
}
details {
  margin: 0.8rem 0;
  background: #f8fff9;
  border-radius: 16px;
  padding: 0.6rem 1rem;
  border: 1px solid #d1f0d9;
}
summary {
  font-weight: bold;
  color: #1f5135;
  cursor: pointer;
  user-select: none;
}
details[open] summary {
  margin-bottom: 0.6rem;
}
pre {
  border-radius: 16px !important;
  margin: 0.8rem 0 !important;
}
</style>

<div class="card">
  <h1 class="title">小红书自动化工具</h1>
  <p class="subtitle">MCP 自动化 · 关键词搜索</p>
  <br>
  <div style="font-size:1.1rem;opacity:0.7">软件创新思维训练 · 张霞</div>
</div>

---

<div class="slide-card">
🎯 项目介绍

本项目使用 **MCP 轻量自动化框架**，实现 **小红书笔记搜索评论** 全套流程，无需复杂配置。

<div class="summary">
  <div class="meta"><strong>核心功能</strong>关键词精准搜索、自动批量评论、请求模拟、异常重试</div>
  <div class="meta"><strong>适用人群</strong>自媒体运营、学生作业、自动化爱好者</div>
  <div class="meta"><strong>技术亮点</strong>代码简洁、可扩展、稳定防封、易演示</div>
  <div class="meta"><strong>运行环境</strong>Windows / macOS / Linux 全平台通用</div>
</div>

<details>
<summary>💡 什么是 MCP？ </summary>
MCP 是一套标准化的自动化任务框架，把爬虫、接口调用、自动化操作都统一成"任务"格式，不用写重复的初始化、日志、异常处理代码。
</details>
</div>

---

<div class="slide-card">
 🧰 第一步：必备环境准备


<div class="summary">
  <div class="meta"><strong>1. Python 3.8+</strong>运行自动化脚本的核心环境</div>
  <div class="meta"><strong>2. VS Code</strong>代码编辑 + 运行 Copilot + 播放PPT</div>
  <div class="meta"><strong>3. Node.js 18+</strong>运行 Slidev 幻灯片</div>
  <div class="meta"><strong>4. Chrome 浏览器</strong>Playwright 自动调用进行自动化</div>
</div>
✅ 一键检查是否安装成功（复制到终端运行）

```bash
python --version
node --version
npm --version
```

```bash
📦 项目安装步骤
# 安装 Python 依赖
pip install -r requirements.txt
pip install fastmcp
# 安装 Playwright 浏览器环境
playwright install chromium
```
</div>


---

<div class="slide-card">
⭐ 第二步：MCP 核心配置

这是整个项目最关键的一步，配置完成后，你就可以**在VS Code里用自然语言直接控制小红书自动化**，不需要手动运行任何脚本。

```json
{
  "mcpServers": {
    "xiaohongshu-mcp-server": {
      "command": "python",
      "args": [
        "D:/专业课/软件创新思维训练/Redbook-Search-Comment-MCP2.0-main/xiaohongshu_mcp.py",
        "--stdio"
      ]
    }
  }
}
```
<div class="summary">
<div class="meta"><strong>核心作用</strong>让 VS Code Copilot 直接调用你的小红书工具</div>
<div class="meta"><strong>实现效果</strong>说一句话就能自动完成搜索</div>
</div>
</div>


---

<div class="slide-card">
📁 第三步：项目结构

所有文件功能一目了然，核心代码在 `xiaohongshu_mcp.py`，数据和浏览器状态自动管理，无需手动干预。
  <div class="summary">
    <div class="meta"><strong>📄 xiaohongshu_mcp.py</strong>核心 MCP 服务器代码</div>
    <div class="meta"><strong>📄 requirements.txt</strong>Python 依赖包列表</div>
    <div class="meta"><strong>📄 .vscode/mcp.json</strong>Copilot MCP 服务器配置文件</div>
    <div class="meta"><strong>📁 browser_data/</strong>自动保存浏览器登录状态</div>
    <div class="meta"><strong>📄 slides.md</strong>PPT演示内容</div>
    <div class="meta"><strong>📁 slidev-demo/</strong>PPT 项目文件夹</div>
  </div>
</div>
--- 

<div class="slide-card">
🔧 第四步：MCP 服务器初始化

这是你的代码核心，初始化 FastMCP 服务器和浏览器上下文，自动创建数据目录并持久化浏览器登录状态。

```python
# 初始化 FastMCP 服务器
mcp = FastMCP("xiaohongshu_scraper")

# 全局变量和目录初始化
BROWSER_DATA_DIR = os.path.join(os.getcwd(), "browser_data")
DATA_DIR = os.path.join(os.getcwd(), "data")
os.makedirs(BROWSER_DATA_DIR, exist_ok=True)
os.makedirs(DATA_DIR, exist_ok=True)

async def ensure_browser():
    # 启动或恢复浏览器上下文，保证自动化操作可用
    pass
```
<div class="summary">
<div class="meta"><strong>核心作用</strong>创建MCP服务器实例，初始化全局配置</div>
<div class="meta"><strong>自动功能</strong>创建数据目录，持久化浏览器状态</div>
</div>
</div>
---

 <div class="slide-card">
🔎 第五步：搜索笔记功能

根据关键词自动搜索小红书笔记，返回标题和链接。
```python
@mcp.tool()
async def search_notes(keywords: str, limit: int = 5) -> str:
    login_status = await ensure_browser()
    if not login_status:
        return "请先登录小红书账号"
    search_url = f"https://www.xiaohongshu.com/search_result?keyword={keywords}"
    await main_page.goto(search_url, timeout=60000)
    await asyncio.sleep(5)
    post_cards = await main_page.query_selector_all('section.note-item')
    results = []
    for card in post_cards[:limit]:
        title = await card.inner_text()
        link = await card.get_attribute('href')
        results.append(f"{title} - {link}")
    return "\n".join(results)
```
<div class="summary">
<div class="meta"><strong>输入</strong>任意关键词 + 返回数量</div>
<div class="meta"><strong>输出</strong>笔记标题 + 完整链接</div></div>
</div>
---

<div class="slide-card">
📄 第六步：获取笔记内容

自动提取笔记的标题、作者、发布时间和完整正文。

```python
@mcp.tool()
async def get_note_content(url: str) -> str:
    await main_page.goto(url, timeout=60000)
    await asyncio.sleep(8)
    await main_page.evaluate('''
        () => {
            window.scrollTo(0, document.body.scrollHeight);
        }
    ''')
    await asyncio.sleep(2)
    title = await main_page.text_content('h1')
    author = await main_page.text_content('.nickname')
    publish_time = await main_page.text_content('.publish-time')
    content = await main_page.text_content('.note-content')
    return f"标题：{title}\n作者：{author}\n发布时间：{publish_time}\n内容：{content[:120]}..."
```
<div class="summary">
<div class="meta"><strong>提取信息</strong>标题、作者、发布时间、完整正文</div>
<div class="meta"><strong>特点</strong>自动处理URL、自动滚动加载、错误页面检测</div>
</div>
</div>

--- 

<div class="slide-card">
💬 第七步：获取笔记评论

自动获取笔记的所有评论，包括用户名、内容和时间。
```python
@mcp.tool()
async def get_note_comments(url: str) -> str:
    await main_page.goto(url, timeout=60000)
    for _ in range(5):
        await main_page.evaluate("window.scrollBy(0, 800)")
        more_btn = main_page.locator("text=查看更多评论").first
        if await more_btn.count() > 0:
            await more_btn.click()
    comments = []
    comment_nodes = await main_page.query_selector_all('.comment-item')
    for node in comment_nodes[:10]:
        username = await node.text_content('.user-name')
        text = await node.text_content('.comment-text')
        comments.append(f"{username}: {text}")
    return "\n".join(comments)
```
<div class="summary">
<div class="meta"><strong>自动加载</strong>点击"查看更多"获取全部评论</div>
<div class="meta"><strong>提取字段</strong>用户名、评论内容、发布时间</div>
</div>
</div>




---


🤖 第八步： Copilot 自动化实操步骤

服务器启动后，无需写代码，直接用自然语言控制自动化：
<div class="summary">
<div class="meta"><strong>1. 确认连接</strong><br><code>VS Code 右下角提示 `MCP 服务器连接成功`</code></div>
<div class="meta"><strong>2. 打开 Copilot</strong><br><code>点击侧边栏 Copilot 图标，打开聊天窗口</code></div>
<div class="meta"><strong>3. 发送指令</strong><br><code>直接输入需求，AI 自动调用工具执行</code></div>
<div class="meta"><strong>4. 等待执行</strong><br><code>自动打开浏览器，完成搜索全流程</code></div>

### 💬 指令示例
- 帮我搜索小红书前三条「Python学习」笔记的评论
</div>



---


<div class="slide-card">
🐛 常见问题解决

你可能遇到的问题，这里都有解决方案。
<details><summary>❌ 浏览器启动失败</summary>运行 `playwright install chromium` 重新安装浏览器即可。</details>
<details><summary>❌ 登录状态丢失</summary>删除 `browser_data` 文件夹，重新运行脚本，手动登录一次即可。</details>
<details><summary>❌ 搜索不到笔记 / 返回空数据</summary>
<p>检查Cookie是否正确</p>
<p>换一个关键词试试</p>
<p>确认你的网络能正常访问小红书</p>
</details></div>




---

<div class="slide-card" style="align；center">
✅ 演示成果展示
  <img src="/image1.png" alt="图片描述" style="width: 80%; border-radius: 10px; box-shadow: 0 4px 20px rgba(0,0,0,0.15);" />
</div>
---
theme: default
background: "#9ecaa4"
class: text-center
highlighter: shiki
lineNumbers: false
---



<div class="card" style="align:center">
  <h1 class="title">🎉 演示结束！谢谢观看</h1>
  <p class="subtitle">MCP 自动化 · 关键词搜索</p>
  <br>
  <div style="font-size:1.1rem;opacity:0.7">软件创新思维训练</div>
</div>