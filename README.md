# WEB WHISPER

<p align="center"> <b> 🎶 Convert any audio to text 📝 </b></p>

<br>

A user interface for OpenAI's [Whisper](https://github.com/openai/whisper) right into your browser!

This is a small personal project I am using to learn Golang and Svelte. It is a light web frontend for OpenAI's whisper.

## Contents:

- [Features](#features)
- [Roadmap](#roadmap)
- [Test it!](#test-it)
- [Self Host](https://codeberg.org/pluja/web-whisper/wiki/Self-Hosting)
- [Screenshots](#screenshots)
- [Other information](#other-information)

## ✨ Features:

- [x] Record and transcribe audio right from your browser.
- [x] Upload any media file (video, audio) in any format and transcribe it.
    - [x] Option to cut audio to X seconds before transcription.
    - [x] Option to disable file uploads.
- [x] Select input audio language
- [x] Translate input audio transcription to english.
- [x] Download `.srt` subtitle file generated from audio.
- [x] Choose the Whisper model you want to use (tiny, base, small...)
- [x] Lightweight and beautiful UI.
- [x] Self-hosted. No 3rd parties.
- [x] **Docker compose** for easy self-hosting
- [x] **Privacy respecting**: 
    - All happens locally. No third parties involved.
    - Audio files are deleted immediately after processing.
- [x] Backend written in **Go**
- [x] Frontend written with **Svelte** and **Tailwind CSS**.
- [x] Uses C++ whisper version from [whisper.cpp](https://github.com/ggerganov/whisper.cpp).
    - You don't need a GPU, uses CPU.
    - No need for complex installations.

## 🧭 Roadmap:

- [x] Allow to upload any file (video, audio) in any format and transcribe it.
	- [ ] Limit max file size for server hosting.
    - [x] Allow to cut audio to X seconds before transcription.
    - [x] Option to disable file uploads.
- [ ] Transcription history / save snippets
    - Publish to some **pastebin**-like service.

## 🧪 Test it!

You can easily [**self host**](https://codeberg.org/pluja/web-whisper/wiki/Self-Hosting) your own instance with docker (locally or in a server).

Also, I have made testing instance available at: https://whisper.r3d.red

Note that this instance is limited:
- Maximum of 10 seconds audio recordings 
- File uploads are disabled.
- Uses the `base` model.

## Screenshots

<p align="center"><sub>*Logo generated with Stable Diffusion*</sub></p>

##### Main page
<img width="850" src="https://farside.link/rimgo/GFBHU8V.png" align=center>

##### Recording
<img width="850" src="https://farside.link/rimgo/M5pW2BB.png" align=center>

#### Transcription Options
<img width="850" src="https://farside.link/rimgo/a4yf4hu.png" align=center>

#### Processing
<img width="850" src="https://farside.link/rimgo/SHOTbh8.png" align=center>

#### Result
<img width="850" src="https://farside.link/rimgo/8EodxT9.png" align=center>

## Other information

#### How fast is this?

Whisper.cpp usually provides faster results than the python implementation. Although it will highly depend on your machine resources, the length of the media source and the file size. Here is a little benchmark:

```
CPU: i7
RAM: 16
Input format: webm audio
File size: 7MB
Audio length: 30m

Total elapsed time: 7m 38s
```

## Similar projects

- [Whisper WASM](https://github.com/ggerganov/whisper.cpp/tree/master/examples/whisper.wasm) - If you want to run Whisper directly in your browser without the need of a server, you can use this project. Note that performance for this version is not very good.