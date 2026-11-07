# pet-videos 🐾

收集、整理并批量下载各类宠物/萌宠的**等级图片、喂养视频与毕业视频**，附带一套可复用的 Python 下载脚本。

## 📁 目录结构

```
pet-videos/
├── scripts/          # 下载脚本
│   ├── download_level_pictures.py   # 各等级图片（PNG）
│   ├── download_feed_videos.py      # 喂养视频（mp4 / webm）
│   └── download_graduate_videos.py  # 毕业视频（webm）
├── 各等级图片/        # 每个宠物 8 个等级的图片
├── 喂养视频/          # 喂养视频 + 文件列表.txt
└── 毕业视频/          # 毕业视频 + 文件列表.txt
```

## 🐶 宠物分类

共 7 个系列：

| 系列 | 宠物 |
|------|------|
| 山海灵宠 | 毕方、凤凰、蛊雕、精卫、九尾狐、天狗 |
| 国风神兽 | 白虎、独角兽、多肉精灵、貔貅、青龙、狻猊、朱雀 |
| 生肖萌宝 | 十二生肖（辰龙、卯兔、寅虎……） |
| 萌犬天团 | 比熊、边牧、柴犬、哈士奇、柯基犬…… |
| 软萌喵星 | 波斯猫、布偶猫、虎斑猫、橘猫…… |
| 绿野部落 | 大熊猫、考拉、浣熊、羊驼…… |
| 水中伙伴 | 海豹、海马、企鹅、水獭…… |

## 🚀 使用方法

三个脚本都依赖 `requests`：

```bash
pip install requests
```

### 1. 下载各等级图片

每个宠物下载 1~8 级图片，保存到 `animal-pet-images/系列名/宠物名/`：

```bash
python scripts/download_level_pictures.py
```

### 2. 下载喂养视频

优先尝试 `mp4`，失败则回退到 `webm`，保存到 `animal-video-feeding/`：

```bash
python scripts/download_feed_videos.py
```

### 3. 下载毕业视频

下载 `webm` 格式，保存到 `animal-video/`：

```bash
python scripts/download_graduate_videos.py
```

> 脚本会自动跳过已存在的文件，支持断点续传（重复运行即可补全缺失文件）。
>
> 可选：安装 `tqdm` 可获得进度条（毕业视频脚本支持）：
> ```bash
> pip install tqdm
> ```

## 📝 说明

- 资源来源于公开的宠物素材站，脚本仅供学习与个人整理使用，请遵守源站的使用条款。
- 各目录下的 `文件列表.txt` 记录了当前已收录的文件清单。
