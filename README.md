# SaveXTube - 智能多媒体下载机器人

SaveXTube 是一个基于 Telegram 的智能多媒体下载工具，支持视频、音乐、磁力链接等多种内容下载，特别针对 NAS 环境进行了优化。

## 🚀 核心功能

### 📱 Telegram 机器人集成

- **简单易用**：用户只需发送链接即可开始下载
- **多平台支持**：支持主流视频、音乐、社交平台
- **智能识别**：自动识别链接类型并选择最佳下载方式
- **实时响应**：机器人实时处理下载请求
- **详细反馈**：提供详细的下载信息和进度显示

### 📊 实时进度显示

- **文件信息**：显示标题、大小、格式等详细信息
- **下载进度**：实时更新的进度条和百分比
- **传输状态**：显示下载速度和剩余时间
- **质量信息**：显示视频分辨率和音频质量

### 🐳 Docker 容器化部署

- **完整容器化**：一键部署，无需复杂配置
- **灵活配置**：支持TOML配置文件和环境变量
- **热重启**：配置更新无需停机
- **资源优化**：针对NAS环境优化资源使用

### 📂 智能分类存储

- **自动分类**：根据内容来源自动分类存储
- **路径自定义**：支持自定义下载目录结构
- **格式识别**：自动识别并分类不同格式文件
- **灵活配置**：支持TOML配置文件和环境变量自定义路径

### 🎵 音乐下载支持

- **网易云音乐**：支持高质量音乐下载，包含歌词和封面
- **QQ音乐**：支持高品质音乐下载
- **Apple Music**：支持无损音乐下载
- **YouTube Music**：支持音频模式下载

### 🎬 视频下载支持

- **YouTube**：支持最高4K分辨率，自动选择最佳质量，支持播放列表、频道视频下载
- **B站 (Bilibili)**：支持大会员内容，包含弹幕下载，支持播放列表、频道视频下载
- **X (Twitter)**：支持NSFW内容，通过Cookies认证
- **抖音/快手/微博视频/头条视频/小红书**：支持短视频下载
- **Instagram/Facebook**：支持社交媒体视频
- **P站/Xvideos**：支持成人内容平台
- **Telegram**：支持Telegram频道内容

### 🖼️ 图片下载支持

- **X (Twitter)**：支持单张及多张图片下载
- **小红书**：支持无水印图片下载
- **Telegraph**：支持Telegraph图片下载

### 🔗 磁力链接与种子下载

- **qBittorrent集成**：支持磁力链接和种子文件下载
- **自动添加**：发送磁力链接自动添加到qBittorrent
- **进度跟踪**：实时显示下载进度和状态
- **智能分类**：自动为下载任务添加标签

### 📚 B站收藏夹订阅

- **自动订阅**：订阅B站收藏夹，自动下载新视频
- **定时检查**：可配置检查间隔，自动发现新内容
- **批量下载**：支持收藏夹内所有视频批量下载
- **智能管理**：支持订阅列表管理和手动下载

### 🔄 格式自动转换

- **智能转换**：YouTube webm格式自动转换为mp4
- **质量保证**：转换过程保持原内容质量
- **可配置**：支持开启/关闭自动转换功能

##  **🔧 Cookies 获取方法**

**说明**：所有平台均采用相同的 Cookies 获取方式。

1. **安装浏览器扩展**

- 安装 **“Get cookies.txt LOCALLY”** 扩展
- 支持 Chrome、Firefox、Edge 等主流浏览器

1. **登录目标平台**

- 在浏览器中登录目标平台账号
- 确保该账号具备所需权限（例如会员权限，如有要求）

1. **导出 Cookies**

- 打开目标平台页面
- 点击浏览器中的 **“Get cookies.txt LOCALLY”** 图标
- 选择 **Copy** 将 Cookies 内容复制出来
- 保存为对应的文件（文件名请参考上文配置表）

1. **Cookies文件格式**

   ```
   # Netscape HTTP Cookie File
   # http://curl.haxx.se/rfc/cookie_spec.html
   # This is a generated file! Do not edit.
   
   .example.com     TRUE     /     TRUE     11111111111     SESSION_ID     XXXXXXXXXXXXXXXXXXXXXXXXXXXXX
   ```

### 🍪 Cookies 配置

### 📋 支持的平台和Cookies文件

| 平台               | 文件名                   | 路径                                   |                                       |
| ------------------ | ------------------------ | -------------------------------------- | ------------------------------------- |
| **X (Twitter)**    | `x_cookies.txt`          | `/app/cookies/x_cookies.txt`           | 用于下载X平台的NSFW内容和受限视频内容 |
| **X (Twitter)**    | x_gallerydl.txt          | `/app/cookies/x_gallerydl.txt `        | 用于下载X平台的NSFW内容和受限图片内容 |
| **B站 (Bilibili)** | `bilibili_cookies.txt`   | `/app/cookies/bilibili_cookies.txt`    | 用于下载B站大会员内容和4K视频         |
| **YouTube**        | `youtube_cookies.txt`    | `/app/cookies/youtube_cookies.txt`     | 用于下载YouTube受限内容和提高下载速度 |
| **抖音 (Douyin)**  | `douyin_cookies.txt`     | `/app/cookies/douyin_cookies.txt`      | 用于下载抖音高质量视频                |
| **Instagram**      | `instagram_cookies.txt`  | `/app/cookies/instagram_cookies.txt`   | 用于下载Instagram内容和图片           |
| **Apple Music**    | `applemusic_cookies.txt` | `/app/cookies/apple_music_cookies.txt` | 用于下载Apple Music无损音乐           |
| **网易云音乐**     | `ncm_cookies.txt`        | `/app/cookies/ncm_cookies.txt`         | 用于下载网易云音乐VIP内容和高质量音乐 |
| **QQ音乐**         | `qqmusic_cookies.txt`    | `/app/cookies/qqmusic_cookies.txt`     | 用于下载QQ音乐VIP内容和高质量音乐     |
| **Telegram**       | `telethon_session.txt`   | `/app/cookies/telethon_session.txt`    | 用于下载TG频道上的视频以及音频        |

## **🔧 开启 Telegram 文件转存功能**

📱 **操作步骤**

1. 打开配置页面

   👉 http://x.x.x.x:8530/setup 或者使用在线的工具https://tools.foxel.cc/

2. 填写必需信息

 - **API ID**

 - **API Hash**

 - **Telegram 手机号**（接收验证码登录）

   ⚡ 成功后，系统会在指定目录自动生成 **会话文件**。

3. 使用方式

   - 将频道或群里的视频 **转发** 到 **savextube 机器人**，即可完成转存。

## 🎵 Apple Music 下载方案

Apple Music 提供 **两种接入方式**：

### 1. ⭐ 默认方案（快速上手）

- 仅需配置 **cookies**
- 下载为 **标准音质**
- 适合想快速使用的用户

### 2. 🚀 增强方案（需引入 Wrapper）

- 先部署 **Wrapper** 服务  
- 在配置文件中指定 **Wrapper 的两个地址**  
- 支持 **更高音质**，并解锁更多功能  

---

### 📊 对比表

| 方案       | 配置方式                | 下载音质 | 备注                      |
| ---------- | ----------------------- | -------- | ------------------------- |
| ⭐ 默认方案 | 配置 cookies            | 普通音质 | 简单快速，适合新手        |
| 🚀 增强方案 | 部署 Wrapper + 配置地址 | 高音质   | 需要额外部署 Wrapper 服务 |

---

### 📌 提示

- 如果只是日常试听，**默认方案**即可满足  
- 如果追求 **高音质 / 完整功能**，推荐使用 **增强方案**

增加方案依赖于第三方开源项目 Wrapper,项目地址为https://github.com/zhaarey/wrapper ，但是该项目没有直接提供 Docker,有动手能力可以自己打包，也可以使用本项目打包好的，地址参考下文配置。

------

## **🔧 Wrapper 使用说明**

### **1️⃣ 初始化配置**

首次使用时，需要先通过 Apple ID 完成登录认证。执行以下命令，并根据提示输入二次验证码：

```
docker run \
  -v ./rootfs/data:/app/rootfs/data \
  -p 10020:10020 \
  -e args="-L username:password -F -H 0.0.0.0" \
  wrapper
```

⚠️ 注意：

- 此命令 **仅在首次初始化时执行一次**
- 成功登录后，后续启动时不再需要重复此步骤
- Apple ID 需求有 VIP 权限，并且不建议使用主力账号下载，下载过多会导致封号，强烈建议单独申请一个小号下载使用！
- 提示Waiting for input...，这时候使用echo-n 114514 > rootfs//data/data/com,apple.android.music/files/2fa.txt 这个命令创建文件，如果你的 NAS支持直接编辑文件，你可以提供在 NAS这个目录中创建好 2fa.txt，当手机收到验证码就填写进去，这样就省去命令行操作不方便问题。

------

### **2️⃣ 启动 Wrapper 服务**

完成初始化后，即可通过 docker-compose 启动 Wrapper 服务。

示例配置如下：

```
services:
  wrapper:
    image: savextube/wrapper:latest
    container_name: wrapper
    restart: unless-stopped
    environment:
      ARGS: "-M 20020 -H 0.0.0.0"
    ports:
      - "10020:10020"
      - "20020:20020"
    volumes:
      - /vol1/1000/docker/wrapper/rootfs/data:/app/rootfs/data
```

------

### **3️⃣ 与 SavexTube 集成（可选）**

Wrapper 可以作为独立服务运行，也可以直接集成到 **SavexTube 项目** 的 docker-compose.yml 中，方便统一管理。

```yaml
services:
  savextube:
    image: savextube/savextube:v0.6.17
    container_name: savextube
    restart: unless-stopped
    environment:
      TZ: Asia/Shanghai
    ports:
      - "8530:8530"
    volumes:
      - /vol1/1000/media/downloads/:/downloads/
      - /var/run/docker.sock:/var/run/docker.sock
      - ./cookies/:/app/cookies
      - ./config/:/app/config/
      - ./db/:/app/db/
      - ./logs/:/app/logs/

  wrapper:
    image: savextube/wrapper:latest
    container_name: wrapper
    restart: unless-stopped
    environment:
      ARGS: "-M 20020 -H 0.0.0.0"
    ports:
      - "10020:10020"
      - "20020:20020"
    volumes:
      - /vol1/1000/docker/wrapper/rootfs/data:/app/rootfs/data
```

## 🤖 创建 Telegram 机器人

1. 在Telegram中搜索**@BotFather**
2. 发送`/newbot`命令创建新机器人
3. 按照提示设置机器人名称和用户名
4. 记录生成的**Bot Token**

## 🚀 Docker Compose 部署

```yaml
services:
  savextube:
    image: savextube/savextube:latest
    container_name: savextube
    restart: unless-stopped
    environment:
      TZ: Asia/Shanghai
    ports:
      - 8530:8530
    volumes:
      # 下载目录
      - /vol1/1000/media/downloads/:/downloads/

      # 重启容器
      - /var/run/docker.sock:/var/run/docker.sock
      
      # Cookies 目录（只读挂载）
      - /vol1/1000/docker/SaveXTube/cookies/:/app/cookies:ro
      
      # 配置文件目录
      - /vol1/1000/docker/SaveXTube/config:/app/config
      
      # 数据库目录
      - /vol1/1000/docker/SaveXTube/db/:/app/db
      
      # 日志目录
      - /vol1/1000/docker/SaveXTube/logs:/app/logs
```

### 🔧 自定义文件目录映射

```yaml
volumes:
  # 统一下载目录
  - /vol1/1000/media/downloads/:/downloads/
  
  # 或者分别映射不同平台到不同目录
  - /vol1/1000/media/videos/youtube:/downloads/YouTube
  - /vol1/1000/media/videos/bilibili:/downloads/Bilibili
  - /vol1/1000/media/music/netease:/downloads/NeteaseCloudMusic
  - /vol1/1000/media/music/qqmusic:/downloads/QQMusic
  - /vol1/1000/media/music/applemusic:/downloads/AppleMusic
 
```

**注意**: 所有路径都可以通过环境变量进行自定义配置。

## 📁 自定义下载路径配置

### 📋 支持的平台和下载路径

| 平台                | 默认下载路径                     | 分类        | 说明                    |
| ------------------- | -------------------------------- | ----------- | ----------------------- |
| **YouTube**         | `/downloads/YouTube/`            | 🎬视频       | YouTube视频和音频       |
| **B站 (Bilibili)**  | `/downloads/Bilibili/`           | 🎬视频       | B站视频，包含收藏夹订阅 |
| **X (Twitter)**     | `/downloads/Pictures/twitter/`   | 📷图片       | X平台图片               |
| **X (Twitter)**     | `/downloads/X/`                  | 🎬视频       | X平台视频和图片         |
| **抖音 (Douyin)**   | `/downloads/Douyin/`             | 🎬视频       | 抖音短视频              |
| **快手 (Kuaishou)** | `/downloads/Kuaishou/`           | 🎬视频       | 快手短视频              |
| **Instagram**       | `/downloads/Instagram/Pic`       | 📷图片       | Instagram图片           |
| **Instagram**       | `/downloads/Instagram/`          | 🎬视频       | Instagram图片和视频     |
| **Facebook**        | `/downloads/Facebook/`           | 🎬视频       | Facebook视频            |
| **小红书 **         | `/downloads/Xiaohongshu/`        | 🎬视频,📷图片 | 小红书视频及图片        |
| **P站 (Pornhub)**   | `/downloads/Pornhub/`            | 🎬视频       | P站视频                 |
| **Xvideos**         | `/downloads/Xvideos/`            | 🎬视频       | Xvideos视频             |
| **Telegram**        | `/downloads/Telegram/`           | 📷图片       | Telegram文件            |
| **Telegraph**       | `/downloads/Pictures/telegraph/` | 📷图片       | Telegraph图片           |
| **网易云音乐**      | `/downloads/NeteaseCloudMusic/`  | 🎵音乐       | 网易云音乐文件          |
| **QQ音乐**          | `/downloads/QQMusic/`            | 🎵音乐       | QQ音乐文件              |
| **Apple Music**     | `/downloads/AppleMusic/`         | 🎵音乐       | Apple Music文件         |
| **YouTube Music**   | `/downloads/YouTubeMusic/`       | 🎵音乐       | YouTube Music文件       |

## 📋 配置文件 (savextube.toml)

按照以下格式填写内容并保存为`savextube.toml`存放在config目录：

```toml
# SaveXTube 完整配置文件
# 创建文件时，若需要保留中文注释，请务必确保本文件编码为 UTF-8，否则会无法读取。

[telegram]
# Telegram Bot 配置
telegram_bot_token = "YOUR_BOT_TOKEN" # 核心配置，必选项
telegram_bot_api_id = "YOUR_API_ID" # 只有需要使用 telegram 保存视频才需要配置
telegram_bot_api_hash = "YOUR_API_HASH" # 只有需要使用 telegram 保存视频才需要配置
telegram_bot_allowed_user_ids = "YOUR_USER_ID" # 允许操作telegram机器人的用户ID

[proxy]
# 代理服务器配置（可选）
# proxy_host = "http://192.168.2.1:7890"

[netease]
# 网易云音乐配置
ncm_quality_level = "无损"
ncm_download_lyrics = true
ncm_dir_format = "{ArtistName}/{AlbumName}"
ncm_album_folder_format = "{AlbumName}({ReleaseDate})"
ncm_song_file_format = "{SongName}"

[apple_music]
# Apple Music 配置
amdp = true
amd_wrapper_decrypt = "192.168.2.134:10020"
amd_wrapper_get = "192.168.2.134:20020"
amd_region = "cn"

[bilibili]
# Bilibili 配置
bilibili_poll_interval = 60

[qbittorrent]
# qBittorrent 连接配置
qb_host = "192.168.2.134"
qb_port = 8988
qb_username = "admin"
qb_password = "YOUR_PASSWORD"

[logging]
# 日志配置
log_level = "INFO"
log_dir = "/app/logs"
log_max_size = 10
log_backup_count = 5
log_to_console = true
log_to_file = true

[youtube]
# YouTube 配置
youtube_convert_to_mp4 = true
```

## 📖 使用方法

### 基本使用

1. 启动SaveXTube容器
2. 在Telegram中找到您的机器人
3. 发送链接或转发视频开始下载

### 支持的命令

- `/start` - 开始使用机器人
- `/help` - 显示帮助信息
- `/status` - 查看系统状态
- `/version ` - 查看版本
- `/favsub ` - 订阅B站收藏夹
- `/setting`  - 功能设置
- `/cleanup ` - 清理文件
- `/cancel ` - 取消下载
- `/reboot ` - 重启容器

### 支持的磁力链接格式

- **磁力链接**: `magnet:?xt=urn:btih:...`
- **种子文件**: 直接发送`.torrent`文件

## 🔧 故障排除

### 常见问题

**Q: 机器人无响应？**

- 检查`telegram_bot_token`是否正确配置
- 确认容器是否正常运行：`docker logs savextube`

**Q: 无法下载VIP内容？**

- 确认已正确配置相应的cookies文件
- 检查cookies文件是否过期，必要时重新导出
- 验证cookies文件格式是否正确

**Q: 磁力链接无法下载？**

- 确认qBittorrent服务正在运行
- 检查qBittorrent配置是否正确
- 验证网络连接和防火墙设置

**Q: 下载的文件找不到？**

- 检查卷映射路径是否正确
- 确认宿主机目录具有适当的读写权限

**Q: 配置文件无法读取？**

- 确认文件编码为UTF-8
- 检查TOML语法是否正确
- 验证文件路径是否正确

## 📝 更新日志

### v0.5 (最新)

- ✅ 简化Docker配置文件
- ✅ 支持TOML配置文件
- ✅ 切换配置文件到SQLite数据库
- ✅ 新增YouTube Music下载支持
- ✅ 新增头条视频下载支持
- ✅ 完善cookies配置系统

### v0.4

- ✅ 新增qBittorrent磁力链接下载支持
- ✅ 新增加Telegraph图片下载功能
- ✅ 新增加Telegram视频转发下载功能
- ✅ 支持/setup生成tg会话文件
- ✅ 新增加X图片下载功能
- ✅ 新增加小红书图片下载功能
- ✅ 新增加Ins视频及图片下载功能
- ✅ 新增加Facebook视频下载功能
- ✅ 新增加快手视频下载功能
- ✅ 新增加抖音视频下载功能
- ✅ 新增加TikTok视频下载功能
- ✅ 新增加微博视频下载功能
- ✅ 新增B站收藏夹订阅、B站播放列表、UP主所有视频下载功能
- ✅ 新增Youtube播放列表、博主所有视频下载功能
- ✅ 新增Apple Music下载支持
- ✅ 新增网易云音乐高质量下载
- ✅ 优化下载进度显示
- ✅ 增强错误处理和日志记录

### v0.3

- ✅ 支持Apple Music下载
- ✅ 新增Instagram和Facebook支持
- ✅ 优化YouTube 4K下载
- ✅ 增强代理功能

### v0.2

- ✅ 支持下载YouTube最高分辨率视频
- ✅ 下载完成后信息汇总支持显示分辨率
- ✅ 支持代理功能

### v0.1

- 🎉 首次发布
- ✅ 支持Telegram机器人集成
- ✅ 支持YouTube和X平台视频下载
- ✅ 实现实时进度显示
- ✅ 添加格式自动转换功能
- ✅ 支持NSFW内容下载

## 🤝 贡献

欢迎提交Issue和Pull Request来帮助改进SaveXTube！


## 💬 交流与支持

### 🔗 社区交流

- **Telegram群组**: (https://t.me/savextube)

⭐ **如果这个项目对您有帮助，请给个Star支持一下！** ⭐

---

**注意**: 请遵守各平台的使用条款和版权法律，仅下载您有权访问的内容。
