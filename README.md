<div align="center">

<img src="assets/banner.svg" alt="LAN Viewer: stream files from your computer to phone and TV" width="100%" />

<br/>

**Watch your videos, music, photos and documents on any screen at home, straight from the computer they're stored on.**

No cloud. No account. No uploads. Your files stay on your network.

[![Download](https://img.shields.io/github/v/release/OWNER/REPO?label=Download&style=for-the-badge&color=8ab4ff&labelColor=0d0d10)](https://github.com/OWNER/REPO/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-3ddc84?style=for-the-badge&labelColor=0d0d10)](#license)

![Windows](https://img.shields.io/badge/Windows-0078D4?style=flat-square&logo=windows&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)
![Android TV](https://img.shields.io/badge/Android_TV-4285F4?style=flat-square&logo=googletv&logoColor=white)

</div>

---

## What is it?

LAN Viewer turns the files on your computer into a media library you can open on your **phone, tablet, TV or another PC**, as long as they share the same Wi-Fi or network.

Pick a folder on one device, enter a short code on another, and start watching. There is nothing to upload and nothing to sign up for.

## Highlights

- 🎬 **Plays your media:** videos, music and photos, with fast seeking even in large files
- 📄 **Opens documents:** PDF, Word (`.docx`), Markdown, text and code files, right in the app
- 📺 **Made for the couch:** a TV mode with big text and full remote-control (D-pad) support on Android TV
- 🔢 **Easy connect:** enter a 6-digit code, no IP address needed
- 🔍 **Find things fast:** search and filter by Video, Images, Audio or Documents
- 🎧 **Keep listening:** music keeps playing while you browse other folders
- 🎨 **Looks good:** Dark, Light and Velvet themes
- 🤖 **Optional AI helper:** ask questions about a file, or get help with connection problems (you bring your own key)
- 🔒 **Private:** everything stays on your local network

## Download

Get the latest version from the **[Releases page](https://github.com/OWNER/REPO/releases/latest)**.

| Your device | Download |
|---|---|
| 🪟 Windows | `.exe` installer |
| 🐧 Linux | `.deb` or `.AppImage` |
| 📱 Android phone / tablet | `.apk` |
| 📺 Android TV / Google TV | the same `.apk` |

<details>
<summary><b>How to install the Android app (phone or TV)</b></summary>

1. Download the `.apk` file.
2. Open it. If Android asks, allow **Install unknown apps** for your browser or file manager.
3. On **Android TV**, the easiest way is to put the APK on a USB drive, or use a file-transfer app such as *Send Files to TV*, then open it with a file manager.
4. Launch **LAN Viewer** from your app list. It also appears on the Android TV home screen.
</details>

## How to use it

<div align="center">
<img src="assets/flow.svg" alt="Share a folder, get a code, enter the code, browse and play" width="100%" />
</div>

Prefer the full picture? This is what happens behind the scenes, including what to check if something goes wrong:

```mermaid
flowchart TD
    A([🚀 Start]) --> B[💻 Open LAN Host and choose a folder]
    B --> C[▶️ Press Start hosting]
    C --> D[🔢 Host shows a 6-digit code, a link and a QR]
    D --> E[📱 Open LAN Viewer on your phone, TV or PC]
    E --> F{Same Wi-Fi<br/>or network?}
    F -- No --> G[📶 Join the same network] --> E
    F -- Yes --> H{How do you<br/>want to connect?}
    H -- Code --> I[Enter the 6-digit code]
    H -- IP and port --> J[Enter e.g. 192.168.1.20 and 8000]
    I --> K{Connected?}
    J --> K
    K -- No --> L[🛡️ Allow the app through the firewall<br/>and check the host is running] --> H
    K -- Yes --> M[📂 Browse folders, search and filter]
    M --> N([🎬 Tap a file to play or preview])

    classDef start fill:#1d3a73,stroke:#8ab4ff,color:#fff
    classDef ok fill:#14532d,stroke:#3ddc84,color:#fff
    classDef warn fill:#5a3b00,stroke:#ffb74d,color:#fff
    class A,N start
    class M ok
    class G,L warn
```

### Step 1: Share a folder from your computer

Use the **LAN Host** app, then choose a folder and press **Start hosting**. It shows a **6-digit code**, a link and a QR code.

Already have Python? You can share a folder with one command instead:

```bash
python -m http.server 8000
```

### Step 2: Open LAN Viewer on another device

1. Tap the **Connect** button at the top.
2. Enter the **6-digit code**, or switch to **IP & port** (for example `192.168.1.20` and `8000`).
3. Browse your files and tap anything to play or preview it.

### TV remote controls

Turn on **TV mode** from the side menu. Use the arrow keys to move, **OK/Enter** to open and **Back** to go up a folder.

## Troubleshooting

<details>
<summary><b>I can't connect</b></summary>

- Make sure both devices are on the **same Wi-Fi or network**, not a guest network.
- Make sure the host is still running ("Start hosting" is on).
- Allow the host app through your **firewall** when your computer asks.
- Try **IP & port** instead of the code. Your computer's IP is usually shown in the host app.
- Still stuck? Tap the **AI assistant** and choose *Can't connect* for step-by-step help.
</details>

<details>
<summary><b>A video won't play</b></summary>

Playback depends on what your device supports. MP4 (H.264) plays almost everywhere. Some formats such as MKV or AVI may not play on every device. Try another device, or convert the file to MP4.
</details>

<details>
<summary><b>Can I watch away from home?</b></summary>

LAN Viewer is built for your local network. For sharing between devices that are not on the same network, the host app also offers a direct peer-to-peer mode.
</details>

## Privacy

- Your files are shared only **while hosting is on**, and only on **your local network** (or directly device-to-device).
- No account, no tracking, no cloud storage.
- The AI helper is **off by default**. If you turn it on, your questions go only to the provider you choose (Google Gemini, Groq or OpenRouter), using your own key, which is stored only on your device.

## Feedback & support

Found a bug or have an idea? Please [open an issue](https://github.com/OWNER/REPO/issues). Tell us your device, your Android or OS version, and what happened.

## License

Released under the [MIT License](LICENSE).

<div align="center">
<sub>Made for the couch, the desk and everything in between. 🛋️</sub>
</div>
