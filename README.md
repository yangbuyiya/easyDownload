# 易下载-微信公众号文章下载工具
 <img src="https://github.com/user-attachments/assets/4c2a4bce-a28c-472f-87b1-18abfcb9564f" width="600" alt="" />
 <img src="https://github.com/user-attachments/assets/c430eb7d-7cb4-4889-8489-5da750b1d5a7" width="600" alt="" />
 
## 关注我
<p style="color:red">需要源码请公众号与我联系！《程序员不易》</p>
<img src="https://github.com/user-attachments/assets/d35dd840-b16e-47e1-a26e-39643a3eb86d" width="600" alt="" />

### 使用


- 单篇文章下载

  直接输入链接，点击下载按钮即可

- 批量下载

  1. 初次使用请安装证书,
     
      - 自动安装（仅限window系统）
      
        需要管理员权限（右击软件图标 -> 以管理员身份运行）
      
        设置中心 → 安装证书
      
      - 手动安装
      
        设置中心 → 打开证书路径 → 打开rootCA.crt文件
      
  2. 需要安装电脑版微信

  3. 点击**批量下载**按钮，开始监听微信公号数据

  4. 在电脑版微信打开一篇需要下载的公号的文章

  5. 回到WechatDownload，会弹框提示

![6721081e569b6569f1717ca8af49407](https://github.com/user-attachments/assets/987e9692-af77-44e8-8100-c62063d31b31)

- 监控下载

  1. 需要安装电脑版微信
  
  2. 在WechatDownload点击**监控下载**按钮（按钮会变颜色）
  
  3. 在电脑版微信打开需要下载的文章（可以打开多篇文章）
  
  4. 回到WechatDownload，再次点击**监控下载**按钮即可开始下载
  
  
- 保存至 MySql

  需要执行 /doc/mysql.sql 文件中的 SQL 语句创建表
  
- 线程配置

  时间间隔：单位是毫秒，假设时间间隔500，单线程是下载完一篇文章，等待500毫秒再继续下载。多线程就是每500毫秒异步下载文章，无需等待上一篇文章下载完成。

  单批数量：假设单批数量10，每次会同时异步下载10篇文章，等待这10篇下载完成，再继续下载10篇。

- 过滤规则

  目前支持对标题和作者进行关键词过滤

  ```json
  {
      "title": {
          "include": ["包含关键词1", "包含关键词2"],
          "exclude": ["排除关键词1","排除关键词2"]
      },
      "auth": {
          "include": ["包含关键词1", "包含关键词2"],
          "exclude": ["排除关键词1", "排除关键词2"]
      }
  }
  ```
  
  举例子，如果需要作者是 张三 并且标题包含 好人，那就是
  
  ```json
  {
      "title": {
          "include": ["好人"]
      },
      "auth": {
          "include": ["张三"]
      }
  }
  ```
  
### 功能

- 支持选择下载范围
- 将网页抓换成HTML、Markdown、PDF
- 将网页源码保存至Mysql（下载来源是网络才有效）
- 下载图片、音频到本地
- 添加原文链接、元数据（作者、时间、公号名）
- 跳过现有文章
- 下载评论
- 下载来源（此选项只影响批量下载）：
- 网络：就是从微信接口获取文章
- 数据库：如果选择了**保存至Mysql**选项，数据库中会保存文章的网页源码，此时如果需要将源码转换成HTML、Markdown ，选择下载来源是数据库即可。（微信接口用得多会被限制）
