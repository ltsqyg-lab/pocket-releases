English | [简体中文](README.zh-CN.md)

<p align="center"><img src="images/icon.png" width="88" alt="Pocket icon"></p>

<h1 align="center">Pocket</h1>

<p align="center">A phone remote control for the AI coding tools on your computer:<br>
Claude Code, Codex, pi, Kimi Code and DeepSeek Harness.</p>

<p align="center">
  <a href="#install">Download</a> ·
  <a href="https://pocket.pocketcli.net/en">Website</a> ·
  <a href="https://pocket.pocketcli.net/en/privacy">Privacy</a> ·
  <a href="https://pocket.pocketcli.net/en/support">Support</a>
</p>

The AI tools keep working on your computer. From your phone you follow their sessions, approve commands, answer their
questions, send the next task by text or voice, and open the files they make.

This repository only has the installers, not the source code.

## Install

You need the desktop app on the computer that runs your AI tools, and the phone app.

| | Download | Requirements |
|---|---|---|
| Mac | [Pocket-Mac.pkg](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-Mac.pkg) | Apple silicon (M1 or later), macOS 13 or later |
| Windows | [Pocket-Windows-Setup.exe](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-Windows-Setup.exe) | 64-bit Windows 10 or 11 |
| Android | [Pocket.apk](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket.apk) | |
| iPhone | [Pocket-unsigned.ipa](https://github.com/ltsqyg-lab/pocket-releases/releases/latest/download/Pocket-unsigned.ipa) | Unsigned (see step 2) |

These links always get the latest version. Version numbers, sizes, checksums and older versions are on the
[Releases](https://github.com/ltsqyg-lab/pocket-releases/releases) page. If GitHub is slow or blocked where you are (for
example in mainland China), get the same files from the [website](https://pocket.pocketcli.net/en#download).

1. **Install the desktop app.**
   - **Mac:** open `Pocket-Mac.pkg`. If macOS won't open it, go to System Settings → Privacy & Security and click
     **Open Anyway**. Allow Accessibility and Automation when asked: Pocket needs them to pass your messages,
     approvals and answers to the AI tools in your terminal windows. Pocket then sits in the menu bar.
   - **Windows:** run `Pocket-Windows-Setup.exe`. If SmartScreen stops it, click **More info → Run anyway**. Pocket
     then sits in the system tray. Right-click its icon to pause syncing or quit.
   - Sign in from the Pocket icon. A page opens in your browser where you can sign in or create an account. The
     Mac app follows your system language; the Windows tray is in Chinese for now.
2. **Install the phone app and sign in with the same account.**
   - **Android:** install `Pocket.apk`, allowing apps from unknown sources when asked.
   - **iPhone:** Pocket isn't on the App Store yet and TestFlight is invite-only. Until then, sideload
     `Pocket-unsigned.ipa` with AltStore or Sideloadly, or install it on your own device with Xcode.
   - Accounts use an email address. Sign up in the app or on the sign-in page. Sign-ups are limited for now.
3. **Approve your devices.** The first phone you sign in on turns on end-to-end encryption for your account. Each
   computer or phone you add later must be approved on a device you already use. Both screens show the same six
   words: if they match, approve on one and confirm on the other.

Your sessions then show up on your phone.

## Screenshots

| Waiting for you | Approving a command | Answering a question |
|:---:|:---:|:---:|
| <img src="images/en/home.jpg" width="240" alt="Home screen: two items waiting, a Codex card asking to run a command, a running session"> | <img src="images/en/approve.jpg" width="240" alt="A Codex session waiting for approval to run pnpm prisma migrate deploy"> | <img src="images/en/question.jpg" width="240" alt="Claude Code asking how long users should stay signed in, with three options"> |
| **Today's sessions** | **Outputs** | **Limits and balances** |
| <img src="images/en/sessions.jpg" width="240" alt="Today's sessions from Claude Code, Kimi Code and pi, one failed"> | <img src="images/en/outputs.jpg" width="240" alt="Outputs: screenshots and charts the AI created"> | <img src="images/en/usage.jpg" width="240" alt="Devices: a computer that is online and end-to-end encrypted, with Claude Code and Codex limits and pi and Kimi Code balances"> |

<sub>The iPhone app (0.1.20) signed in to the demo account. The projects and numbers (Acme) are made up.</sub>

## Features

- Sessions from all your computers and all five AIs in one list: running, waiting for you, done or failed.
- Start a session with the AI, model and reasoning effort you pick. Attach files and photos from your phone.
- Search session titles and everything that was said, then jump to the message.
- Hand a session to another AI. Pocket stops the current one, writes handoff notes (the task, the recent conversation,
  the files it changed) and starts the next AI in the same project.
- A lead AI can give parts of the work to helper AIs in the same project.
- Claude Code and Codex usage limits with their reset times, pi and Kimi Code balances.

## End-to-end encryption

Since desktop app 0.1.38 and phone app 0.1.20, sessions, files, commands, and the messages and answers you send are
end-to-end encrypted. The keys exist only on your phones and computers. Pocket's servers and the relay pass on, and
briefly store, encrypted data they can't read. The servers still see your account email, which devices you have
(name, type, public key), when they are online, how much data they exchange, and IP addresses.

A new device can read your content only after you approve it on a device you already use, so whoever runs the server
can't quietly add one.

The parts that handle your data in transit are open source (AGPL-3.0):

- [pocket-relay](https://github.com/ltsqyg-lab/pocket-relay) stores and forwards the encrypted data between your
  devices.
- [pocket-asr](https://github.com/ltsqyg-lab/pocket-asr) turns voice input into text. In the app you choose where that
  happens: Pocket's cloud, your own computer, your phone, or a gateway you run yourself.

You can run either one yourself on a server with a public IP and Docker, no domain needed. It prints a
`pocket-relay://…` or `pocket-asr://…` line that you paste into the app (phone app 0.1.21 or later). The steps are in
each repository.

Apps and desktop apps that haven't been updated keep working the old way (the servers can see their content) until
November 6, 2026. After that, the old plaintext records are deleted from the servers. Details are in the
[privacy policy](https://pocket.pocketcli.net/en/privacy).

## Verify a download

Each release has a `manifest.json` with the SHA-256 checksum of every file. The release notes list the same checksums.

```sh
shasum -a 256 Pocket-Mac.pkg                        # macOS
sha256sum Pocket.apk                                # Linux
certutil -hashfile Pocket-Windows-Setup.exe SHA256  # Windows
```

`manifest.json` also has an Ed25519 signature for each file over the text
`pocket-update/1\n<file>\n<version>\n<sha256>`. The Mac app's updater won't install a package whose signature doesn't
verify. To check the signatures yourself with Node.js, run this next to `manifest.json`:

```sh
node -e '
const c = require("crypto"), m = require("./manifest.json")
const key = c.createPublicKey({ key: { kty: "OKP", crv: "Ed25519", x: "YT0DFmHTooXbK16fan5oiLD9WEq90_6cSEDOUigWlg4" }, format: "jwk" })
for (const p of m.packages)
  console.log(p.file, p.ver, c.verify(null, Buffer.from(`pocket-update/1\n${p.file}\n${p.ver}\n${p.sha256}`), key, Buffer.from(p.sig, "base64")) ? "signature OK" : "BAD SIGNATURE")
'
```

## Privacy and support

- [Privacy policy](https://pocket.pocketcli.net/en/privacy) · [Terms of service](https://pocket.pocketcli.net/en/terms) · [Support](https://pocket.pocketcli.net/en/support)
- Email: [service@pocketcli.net](mailto:service@pocketcli.net)
