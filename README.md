# 🚀 HaashLM - AI-Powered Video Learning Platform

**A secure, production-ready AI app that transforms YouTube videos into interactive learning experiences with quizzes, code exercises, and Google Colab integration.**

## 🎯 Key Features

- **Visual Video Analysis**: Upload any coding tutorial and Gemini AI analyzes both audio and visual content to understand what's being taught 🧠
- **Auto-Generated Coding Exercises**: Creates interactive coding challenges based on the tutorial content that you can solve in real-time 💻
- **Built-in Code Compiler**: Test and run generated exercises directly in your browser - no external setup needed 🔥
- **AI Chat Assistant**: Ask questions about the video content and get instant answers from the AI that watched your tutorial ✨
- **Custom Learning Materials**: Generate personalized flashcards, quizzes, and coding exercises tailored to the video content 📓
- **Interactive Learning Hub**: Everything in one place - video player, code editor, AI chat, and learning materials 🎨
- **Real-time Execution**: Run code, get feedback, and iterate instantly while learning ⚡

## 🏷️ Docker Tags

| Tag    | Description        |
| ------ | ------------------ |
| `beta` | Production build   |

## 🚀 Quick Start

```bash
# Pull the image
docker pull imhari14/haash-lm:beta

# Run container
docker run -p 3000:3000 -p 8001:8001 imhari14/haash-lm:beta
```

### Docker Compose

```bash
docker run -d -p 3000:3000 -p 8001:8001 --name haashlm imhari14/haash-lm:beta
```
## 🎥 Demo Walkthrough

[![Watch the Demo](https://img.youtube.com/vi/c3EXpJ3FXUQ/maxresdefault.jpg)](https://youtu.be/msM2Nej8m_M?si=TFtODnY6UOK3jkcs)


## 🌐 Access

- **Frontend**: [http://localhost:3000](http://localhost:3000)
- **Health Check**: [http://localhost:8001/health](http://localhost:8001/health)

## 🔧 Configuration

### API Keys (Through Web UI)

1. Start container
2. Open [http://localhost:3000](http://localhost:3000)
3. Configure API keys in settings

**Required Keys:**

- Gemini API Key ([https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey))
- Judge0 API Key ([https://judge0.com/](https://judge0.com/) or [https://rapidapi.com/judge0-official/api/judge0-ce](https://rapidapi.com/judge0-official/api/judge0-ce))

## 📈 Performance Comparison: HaashLM vs AI Studio

| Feature | **HaashLM** | AI Studio | Improvement |
|---------|-------------|-----------|-------------|
| **Max Video Length** | 90 minutes | 40 minutes | **+125%** |
| **Token Consumption** | ~150K tokens | 700K-800K tokens | **5x Less** |
| **Video Processing Method** | Proprietary Smart Sampling | 1FPS extraction | **10x Efficient** |
| **Initial Processing Time** | 3 minutes (90min video) | 3 minutes (40min video) | **3x Faster** |
| **Consecutive Responses** | 30-40 seconds | 3+ minutes | **5x Faster** |
| **Context Handling** | Maintains low hallucination (fewer tokens) | Hallucinates >500K | **Rock Solid** |

**Why HaashLM handles longer videos:** While AI Studio can technically upload 1-hour videos, it fills up the context window 100%, leaving no space for chat replies - making 40 minutes the practical limit for interactive use. 

🚀 **Here's the game-changer:** HaashLM processes a full 90-minute video using only 150k tokens - that's incredible efficiency! Our advanced video processing algorithms intelligently sample key frames and optimize content analysis, allowing you to learn from feature-length tutorials while maintaining plenty of context space for meaningful conversations.

## 📋 Features

- **Video Processing**: Transcription, summarization, multi-language support
- **AI-Powered Generation**: Quizzes, flashcards, code exercises, Colab notebooks
- **Code Execution**: Multi-language support, real-time execution, Judge0 integration
- **Modern Interface**: Responsive design, dark/light themes, intuitive UX

## 🏗️ Architecture

- Frontend: Next.js 14 + TypeScript + Tailwind CSS
- Backend: FastAPI + Python 3.12
- AI Integration: Google Gemini 2.5 Flash API
- Code Execution: Judge0 CE API
- Video Processing: FFmpeg + yt-dlp
- Security: Obfuscated bytecode, non-root user

## 🔍 Health & Logs

```bash
# Health check
curl http://localhost:8001/health

# Logs
docker logs -f haashlm
```

## 🛠️ Troubleshooting

- **Invalid API key**: Check format, permissions, and quota
- **Port conflicts**: Ensure 3000 & 8001 are free
- **System Config**: Minimum 8-12 core CPUs and 8GB RAM for smooth experience
- **Network issues**: Check connectivity to APIs

## 🔒 Security

- Source code protection (compiled Python)
- Reverse engineering protection
- Production optimization
- Enterprise-ready deployment

## 🚀 Start Using HaashLM

```bash
docker pull imhari14/haash-lm:beta
docker run -p 3000:3000 -p 8001:8001 imhari14/haash-lm:beta
```

**⭐ Star this repo if you find it useful!**
