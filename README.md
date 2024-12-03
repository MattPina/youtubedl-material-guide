# YoutubeDL-Material Guide 📺

> A comprehensive guide for YoutubeDL-Material - A powerful self-hosted YouTube downloader built with Material Design

*This repository was created with the assistance of MCP from Claude AI to provide comprehensive documentation and guidance for YoutubeDL-Material.*

## 📋 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Docker Deployment](#docker-deployment)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## 🚀 Introduction

YoutubeDL-Material is a sleek, modern, and feature-rich self-hosted YouTube downloader that provides a beautiful Material Design interface for downloading videos from YouTube and other supported platforms. It's built on top of youtube-dl/yt-dlp and provides an intuitive web interface for managing downloads.

## ✨ Features

- 🎨 Material Design interface
- 📱 Responsive layout for mobile and desktop
- 🎵 Download audio-only formats
- 🎬 Support for multiple video qualities
- 📑 Playlist support
- 🔍 Built-in YouTube search
- 📁 File management system
- 🔄 Queue system for multiple downloads
- 🎯 Custom output templates
- 🔒 Authentication system
- 📱 Progressive Web App (PWA) support
- 🌐 Multi-language support
- 📊 Download activity tracking
- 🎨 Customizable themes
- 🔔 Notifications for download completion

## 💻 Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Python 3
- ffmpeg

### Method 1: Docker (Recommended)
```bash
docker pull tzahi12345/youtubedl-material
docker run -d \
    -p 8998:17442 \
    -v /path/to/downloads:/app/audio \
    tzahi12345/youtubedl-material
```

### Method 2: Manual Installation
```bash
git clone https://github.com/Tzahi12345/YoutubeDL-Material.git
cd YoutubeDL-Material
npm install
npm run build
npm start
```

## ⚙️ Configuration

The configuration file is located at `config/default.json`. Here are the main configuration options:

```json
{
    "Host": {
        "port": 17442,
        "url": "http://example.com"
    },
    "Themes": {
        "default_theme": "default"
    },
    "Downloads": {
        "video_folder": "video",
        "audio_folder": "audio"
    }
}
```

## 🎯 Usage

1. Access the web interface at `http://localhost:8998`
2. Paste a YouTube URL in the download field
3. Select your preferred format and quality
4. Click download and wait for completion
5. Access your downloads in the specified folder

## 🐳 Docker Deployment

### Using Docker Compose
```yaml
version: "3"
services:
  youtubedl-material:
    image: tzahi12345/youtubedl-material
    container_name: youtubedl-material
    volumes:
      - ./downloads:/app/downloads
      - ./config:/app/config
    ports:
      - "8998:17442"
    restart: unless-stopped
```

## 🔧 Troubleshooting

Common issues and solutions:

1. **Download fails**
   - Ensure youtube-dl/yt-dlp is up to date
   - Check network connectivity
   - Verify URL format

2. **Audio extraction fails**
   - Verify ffmpeg installation
   - Check file permissions

3. **Web interface not loading**
   - Confirm port availability
   - Check firewall settings

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📚 Additional Resources

- [Official Documentation](https://github.com/Tzahi12345/YoutubeDL-Material/wiki)
- [Docker Hub](https://hub.docker.com/r/tzahi12345/youtubedl-material)
- [Issue Tracker](https://github.com/Tzahi12345/YoutubeDL-Material/issues)

## 🙏 Acknowledgments

- Built on [youtube-dl](https://github.com/ytdl-org/youtube-dl) / [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- Uses [Material Design](https://material.io/design)
- Documentation assisted by MCP from Claude AI

---

*Note: This is a guide repository and not the official YoutubeDL-Material repository. For the official repository, please visit [Tzahi12345/YoutubeDL-Material](https://github.com/Tzahi12345/YoutubeDL-Material).*