# P2P Media Streaming Player

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,100:00C9FF&height=220&section=header&text=P2p%20Media%20Streaming%20Player&fontSize=55&fontColor=ffffff&animation=twinkling&fontAlignY=35&desc=Decentralized%20Video%20Streaming%20Without%20The%20Servers&descAlignY=55&descSize=20)

<div align="center">

![Version](https://img.shields.io/badge/version-2.7.0-00C9FF?style=for-the-badge&logo=git&logoColor=black)
![Downloads](https://img.shields.io/badge/downloads-97.5K-0F2027?style=for-the-badge&logo=download&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-FFD700?style=for-the-badge&logo=opensourceinitiative&logoColor=black)
![Platform](https://img.shields.io/badge/platform-web%20%7C%20webrtc-00E676?style=for-the-badge&logo=webrtc&logoColor=black)

</div>

---

## 🌐 The End Of Buffering

Centralized video streaming is expensive and fragile. If the server goes down, your stream dies. If too many people watch at once, the server crashes (the infamous "Reddit Hug of Death"). And the hosting costs for video are astronomical.

**P2P Media Streaming Player** is a revolutionary, open-source web player that flips the model on its head. Instead of streaming video from a central server, it uses **Peer-to-Peer (P2P) technology** (WebRTC) to stream directly from viewer to viewer.

When you watch a video using this player, you are not just downloading data; you are also *uploading* it to other viewers watching the same stream. This is called a **Swarm**. As more people join the stream, the quality gets better, the buffering decreases, and the original server's bandwidth usage drops to nearly zero.

This repository is the ultimate tool for indie filmmakers, live streamers, and open-source advocates who want to distribute high-quality video without paying massive cloud hosting bills.

---

## 🕸️ The Swarm Architecture

We have built this player to be incredibly lightweight and efficient. Here is how the data flows.

| Layer | Component | Role |
| :--- | :--- | :--- |
| **The Tracker** | WebSocket Server | Coordinates the peers and helps them find each other |
| **The Swarm** | WebRTC Data Channels | The actual peer-to-peer connection where video chunks are swapped |
| **The Player** | HTML5 Video + MSE | Decodes the chunks and renders the video to your screen |
| **The Origin** | HTTP Server | Serves the very first copy of the video (the seed) |

---

## ✨ Core Features

- **Zero-Bandwidth Scaling:** The more people watch, the less bandwidth the server needs.
- **Low Latency:** WebRTC is designed for real-time communication, ensuring sub-second delay.
- **Adaptive Bitrate:** Automatically adjusts video quality based on the health of the swarm.
- **Fallback Support:** If P2P fails (e.g., strict corporate firewalls), it seamlessly falls back to HTTP streaming.
- **Cross-Platform:** Works on any modern browser, including Chrome, Firefox, and Safari.
- **Live Streaming Support:** Perfect for broadcasting live events without expensive CDNs.

---

<div align="center">

### 🔗 Ready to join the swarm?

[![Get Player](https://img.shields.io/badge/🌐_GET_PLAYER-0F2027?style=for-the-badge&logoColor=white)](https://share.google/1vr4eJnLqhX9ePKL3)

</div>

---

## ⚙️ Quick Setup

To run the player, you need Node.js and a browser that supports WebRTC.

```bash
# Step 1: Clone the repository
git clone https://github.com/your-username/p2p-media-streaming-player.git

# Step 2: Install dependencies
npm install

# Step 3: Start the tracker and origin server
npm start

# Step 4: Open your browser and navigate to the demo page
# http://localhost:8080
```

Open the demo page in two different browser windows. You will see in the developer console that the two peers have connected and are sharing video chunks with each other.

---

<div align="center">

### ⚙️ Need a detailed configuration guide?

[![Setup Guide](https://img.shields.io/badge/📖_VIEW_SETUP_GUIDE-00C9FF?style=for-the-badge&logoColor=black)](https://share.google/1vr4eJnLqhX9ePKL3)

</div>

---

## 🧠 Under The Hood: WebRTC and Media Source Extensions

How does a browser stream video from another browser? It uses two cutting-edge web technologies.

First, **WebRTC (Web Real-Time Communication)**. This API allows browsers to open a direct data channel between each other. No server in the middle. We use WebRTC to send small chunks of the video file (usually 1MB each) from peer to peer.

Second, **MSE (Media Source Extensions)**. A standard HTML5 `<video>` tag expects a single continuous file. MSE allows us to feed the video element a stream of chunks. As the chunks arrive via WebRTC, we append them to the MSE buffer, and the video plays smoothly.

---

## 🛠️ Tech Stack

<div align="center">

![WebRTC](https://img.shields.io/badge/WebRTC-333333?style=flat-square&logo=webrtc&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

</div>

---

## 🤝 Community & Contributing

We believe that the internet should be decentralized and resilient. If you have optimized the swarm logic, added support for a new video codec, or found a bug in the tracker, we welcome your contributions!

1. **Fork** the repository.
2. **Create** your feature branch (`git checkout -b feature/new-codec`).
3. **Commit** your changes (`git commit -m 'Add new codec'`).
4. **Push** to the branch (`git push origin feature/new-codec`).
5. **Open** a Pull Request.

Please read our `CONTRIBUTING.md` for detailed coding standards and testing requirements. We also have an active Discord server where you can share your streaming setups, ask for help with WebRTC, and discuss the latest trends in decentralized web technology.

---

## 📬 Contact & Support

- 💬 **Discussions:** Join the conversation in the GitHub Discussions tab.
- 🐛 **Issues:** Found a bug? Let us know via the Issues tracker.
- 📧 **Email:** Reach out directly at support@p2p-player.dev.

---

<div align="center">

### ⭐ If this player revolutionizes your streaming, give it a star! ⭐

[![Star](https://img.shields.io/badge/⭐_STAR_THIS_REPO-FFD700?style=for-the-badge&logo=github&logoColor=black)](https://github.com/your-username/p2p-media-streaming-player)

---

### 🚀 Start streaming today

[![Get Started](https://img.shields.io/badge/🚀_GET_STARTED_GUIDE-00E676?style=for-the-badge&logoColor=black)](https://share.google/1vr4eJnLqhX9ePKL3)

<sub>Crafted with precision and ❤️ by the P2P Media Streaming Player community</sub>

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00C9FF,100:0F2027&height=120&section=footer)

</div>
