# myc115

一个表白祝福网页：开场后打字机逐字打出句子，随后爱心形状的弹窗依次浮现，展示留言文案。

## 文件说明

| 文件 | 说明 |
|------|------|
| `index.html` | 网页主文件（样式与脚本都已内嵌在里面） |
| `music/` | 背景音乐目录，把音乐文件放到这里 |
| `.github/workflows/static.yml` | GitHub Pages 静态部署工作流 |

## 在线访问

https://shi-diqi.github.io/myc115/

## 怎么换背景音乐

1. 把音乐文件（推荐 `.mp3`）放到 `music/` 目录，默认文件名 `bgm.mp3`。
2. 打开 `index.html`，找到 `<audio>` 标签里的：

   ```html
   <source src="music/bgm.mp3" type="audio/mpeg">
   ```

3. 如果文件名或格式不同，同步修改 `src` 和 `type`：

   | 格式 | type 写法 |
   |------|-----------|
   | MP3  | `audio/mpeg` |
   | WAV  | `audio/wav` |
   | OGG  | `audio/ogg` |
   | M4A  | `audio/mp4` |

- `loop` 表示循环播放；删掉则只播一遍。
- 浏览器通常禁止页面一打开就自动出声，首次点击或触摸页面后音乐才会响起，这是正常现象。

## 怎么改弹窗文案

在 `index.html` 的 `<script>` 里找到 `const texts = [...]` 数组，直接修改里面的句子即可。

## 关于自定义域名

仓库里原有的 `CNAME`（blog.myc7510.com）因域名未解析已移除。如需绑定自己的域名，先在域名服务商处配置好 DNS 解析（指向 GitHub Pages），再在仓库 Settings → Pages → Custom domain 中填写。
