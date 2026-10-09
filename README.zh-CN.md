[English](README.md) | 简体中文

<p align="center"><img src="images/icon.png" width="88" alt="Pocket 图标"></p>

<h1 align="center">Pocket</h1>

<p align="center"><b>AI 编程助手的手机遥控器</b><br>
Claude Code、Codex、pi、Kimi Code、DeepSeek Harness 在电脑上干活,<br>
你在手机上看进度、替它拍板、看它做出来的东西。</p>

<p align="center">
  <a href="#下载">下载</a> ·
  <a href="https://pocket.pocketcli.net/zh">官网</a> ·
  <a href="https://pocket.pocketcli.net/privacy">隐私政策</a> ·
  <a href="https://pocket.pocketcli.net/support">支持</a>
</p>

| 会话和待处理 | 审批命令 | 回答它的提问 |
|:---:|:---:|:---:|
| <img src="images/zh/home.jpg" width="240" alt="首页:2 件待处理,最前面是 Codex 请求执行命令的卡片,下面是进行中的会话"> | <img src="images/zh/approve.jpg" width="240" alt="Codex 会话在等你审批 pnpm prisma migrate deploy"> | <img src="images/zh/question.jpg" width="240" alt="Claude Code 问登录状态要保持多久,有三个选项"> |
| **几个 AI 在一个列表里** | **AI 做出来的东西** | **额度与余额** |
| <img src="images/zh/sessions.jpg" width="240" alt="今天的会话:Claude Code、Kimi Code、pi,一个出错"> | <img src="images/zh/outputs.jpg" width="240" alt="产物:AI 生成的截图和图表"> | <img src="images/zh/usage.jpg" width="240" alt="设备:在线、已端到端加密的电脑,Claude Code 和 Codex 的额度,pi 和 Kimi Code 的余额"> |

<sub>以上是 iPhone App(0.1.20)登录演示账号时的真实截图;项目和数据(Acme)都是虚构的。</sub>

## 能做什么

- **所有会话一眼看清。** 在跑、等你、做完还是出错,所有电脑上的都在。
- **在手机上拍板。** 允许或拒绝它要跑的命令,替它选答案,批准计划,或者告诉它怎么改。
- **从手机派活。** 打字或按住说话。新开会话时选好用哪个 AI、哪个模型、思考深度。也能从手机发文件和照片给它。
- **看它做出来的东西。** 截图、网页、文档自动传到手机。
- **五个 AI。** Claude Code、Codex、pi、Kimi Code、DeepSeek Harness。
- **搜索。** 搜会话标题,也搜聊过的话;点一下命中的那句,直接跳到那条消息。
- **换个 AI 接着做。** 还在跑就先让它停下,把原来的任务、最近的对话、改过的文件写成交接说明,在同一个项目里开新的 AI 接着做,带上你的交代和选好的模型。
- **多 agent 团队。** 主 AI 可以把一部分活交给在同一个项目里干活的其他 AI。
- **额度与余额。** Claude Code、Codex 的额度和恢复时间,pi、Kimi Code 的余额。
- **夜间模式**,跟着手机的深色外观自动切换。

## 下载

| 平台 | 文件 | 说明 |
|---|---|---|
| Android | [Pocket.apk](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket.apk) | 手机 App。安装时允许安装「未知来源」的应用。 |
| iPhone | [Pocket-unsigned.ipa](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-unsigned.ipa) | 手机 App,未签名。用 AltStore / Sideloadly 自签安装,或用 Xcode 装到自己的设备。 |
| Mac | [Pocket-Mac.pkg](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-Mac.pkg) | 电脑端。Apple 芯片(M1 及以后),macOS 13 或更新。 |
| Windows | [Pocket-Windows-Setup.exe](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-Windows-Setup.exe) | 电脑端。64 位 Windows 10 / 11。 |

以上链接始终指向最新版本。版本号、大小、校验值和历史版本见 [Releases](https://github.com/ltsqyg-lab/pocket-releases/releases)。

国内网络打不开 GitHub 或下载很慢时,到[官网的下载区](https://pocket.pocketcli.net/zh#download)下载:是同样的文件,不经过 GitHub。

## 开始使用

1. **在跑 AI 编程工具的电脑上装电脑端。**
   - **Mac:** 打开 `Pocket-Mac.pkg`,按安装器一步步装。如果系统不让打开:系统设置 → 隐私与安全性 → 点「仍要打开」。装完系统会问「辅助功能」和「自动化」权限,请允许:你在手机上发的话、做的审批和回答,要靠它们交给终端窗口里的 AI。之后 Pocket 在菜单栏里。
   - **Windows:** 双击 `Pocket-Windows-Setup.exe`。被 SmartScreen 拦下时点「更多信息」→「仍要运行」。之后 Pocket 在右下角托盘里,托盘图标也是开关。
   - 在 Pocket 图标里点「登录 / 注册」,会在浏览器里打开登录页,可以登录,也可以注册新账号。
2. **手机装 App,用同一个账号登录。**
   - **Android:** 安装 `Pocket.apk`。
   - **iPhone:** 还没上架 App Store,TestFlight 目前只对受邀用户开放;在那之前可以自签安装 `Pocket-unsigned.ipa`。
   - 账号用邮箱注册,在 App 里或电脑端打开的登录页上都能注册;目前名额有限。
3. **批准你的设备。** 第一部登录的手机会为账号开启端到端加密。之后每加一台电脑或手机,都要在已有的设备上批准:两边会显示同样的 6 个字,一样就在一边批准、另一边确认。

之后电脑上的会话就出现在手机上了。

<p align="center">
  <img src="images/zh/windows-sign-in.png" width="402" alt="Windows 电脑端的登录窗口:登录 / 注册、用密码登录">
  &nbsp;
  <img src="images/zh/windows-tray-menu.png" width="252" alt="Windows 托盘菜单:还没登录、登录 / 注册、暂停同步、退出 Pocket">
</p>
<p align="center"><sub>Windows 电脑端(0.1.38)的登录窗口和托盘菜单,真实截图。</sub></p>

## 端到端加密

从电脑端 0.1.38、App 0.1.20 起,会话、文件、命令,以及你发出的话和回答都做端到端加密。钥匙只在你的手机和电脑上;Pocket 的服务器和中继只转发、暂存加密后的数据,看不到内容。服务器仍然看得到的:你的账号邮箱,你有哪些设备(名称、类型、公钥),它们什么时候在线、互相发了多大的数据,以及 IP 地址。

新设备要在你已有的设备上批准之后才能读到内容,所以运营服务器的人没法悄悄加进一台设备。

经手你数据的这两部分是开源的(AGPL-3.0):

- [pocket-relay](https://github.com/ltsqyg-lab/pocket-relay):中继,在你的设备之间存放、转发加密后的数据。可以自己部署中继,在 App 里切换过去。
- [pocket-asr](https://github.com/ltsqyg-lab/pocket-asr):语音转文字的网关。语音在哪里转成文字由你在 App 里选:Pocket 云端、你自己的电脑、手机本机,或者你自己部署的网关。

还没更新的 App 和电脑端照旧走原来的方式(服务器看得到内容),到 2026 年 11 月 6 日为止;之后服务器上旧的明文记录会全部删除。详见[隐私政策](https://pocket.pocketcli.net/privacy)。

## 校验下载的文件

每个版本都带一个 `manifest.json`,里面有每个文件的 SHA-256 校验值;版本说明里也列着同样的值。

```sh
shasum -a 256 Pocket-Mac.pkg                        # macOS
sha256sum Pocket.apk                                # Linux
certutil -hashfile Pocket-Windows-Setup.exe SHA256  # Windows
```

`manifest.json` 里还有每个文件的 Ed25519 签名,签的是 `pocket-update/1\n<文件名>\n<版本号>\n<sha256>` 这段文字;Mac 电脑端的自动更新验不过签名就不装。想自己用 Node.js 验签名,在 `manifest.json` 所在目录运行:

```sh
node -e '
const c = require("crypto"), m = require("./manifest.json")
const key = c.createPublicKey({ key: { kty: "OKP", crv: "Ed25519", x: "YT0DFmHTooXbK16fan5oiLD9WEq90_6cSEDOUigWlg4" }, format: "jwk" })
for (const p of m.packages)
  console.log(p.file, p.ver, c.verify(null, Buffer.from(`pocket-update/1\n${p.file}\n${p.ver}\n${p.sha256}`), key, Buffer.from(p.sig, "base64")) ? "signature OK" : "BAD SIGNATURE")
'
```

## 隐私与支持

- [隐私政策](https://pocket.pocketcli.net/privacy) · [用户协议](https://pocket.pocketcli.net/terms) · [支持](https://pocket.pocketcli.net/support)
- 邮箱:[service@pocketcli.net](mailto:service@pocketcli.net)

## 关于这个仓库

这里只存放编译好的安装包,不含源代码。安装包挂在每个[版本](https://github.com/ltsqyg-lab/pocket-releases/releases)下面。
