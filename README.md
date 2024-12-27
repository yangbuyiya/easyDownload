# EasyDownload - 让微信公众号文章批量下载变得简单

> 一款功能强大的微信公众号文章下载助手，让你轻松保存喜欢的内容

## 🌟 亮点功能

- 📦 一键批量下载公众号文章
- 🎨 多种导出格式：HTML/Markdown/PDF
- 🗃️ MySQL 数据库存储支持
- 🖼️ 图片、音频资源本地化
- 💬 评论数据完整保存
- ⚡ 智能监控，自动下载

## ⬇️ 下载最新版本

> 请前往 [GitHub Releases](https://github.com/yangbuyiya/easyDownload/releases) 下载最新版本以获得最佳体验！

## 📸 软件预览

<div style="display: flex; justify-content: space-between; margin-bottom: 20px;">
  <img src="https://github.com/user-attachments/assets/4c2a4bce-a28c-472f-87b1-18abfcb9564f" width="48%" alt="软件界面预览"/>
  <img src="https://github.com/user-attachments/assets/c430eb7d-7cb4-4889-8489-5da750b1d5a7" width="48%" alt="功能展示"/>
</div>

## 🚀 快速上手

### 单篇文章下载
复制文章链接 → 粘贴到软件 → 点击下载，就是这么简单！

### 批量下载模式
1. **首次配置**
   - Windows 用户：以管理员身份运行，自动安装证书
   - 其他系统：手动安装证书（设置中心 → 证书路径 → 安装 rootCA.crt）

2. **开始使用**
   - 安装电脑版微信
   - 点击"批量下载"按钮
   - 用微信打开目标公众号文章
   - 等待提示框出现，开始下载

### 智能监控模式
1. 启动监控（点击按钮变色）
2. 打开需要下载的文章（支持多篇）
3. 回到软件，再次点击按钮开始下载

## ⚙️ 高级设置

### MySQL 存储
执行 `/doc/mysql.sql` 创建必要数据表

### 下载优化配置
- **时间间隔**：设置下载间隔（毫秒）
- **批量处理**：同时处理文章数量
- **资源选项**：可选择下载图片、音频、评论等

### 智能过滤规则
```json
{
    "title": {
        "include": ["想要的关键词"],
        "exclude": ["不想要的关键词"]
    },
    "auth": {
        "include": ["关注的作者"],
        "exclude": ["屏蔽的作者"]
    }
}
```

## 📢 关于
- 软件仅供学习交流使用
- 请遵守相关法律法规
- 禁止用于商业用途

## 🤝 支持与反馈
欢迎加入我们的技术交流社区：
- 提交 GitHub Issues
- 关注更新动态
- 参与社区讨论

## 📱 关注公众号
> 欢迎关注公众号「程序员不易」，获取更多技术分享和使用教程

![公众号二维码](https://github.com/user-attachments/assets/d35dd840-b16e-47e1-a26e-39643a3eb86d)

