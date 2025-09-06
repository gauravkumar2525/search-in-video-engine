# 🔍 Search in Video Engine

**Search in Video Engine** is a powerful tool for students, educators, and content creators. It allows you to **search for words or full sentences in any video**, whether it's a **local file** or a **YouTube video**, and provides **exact timestamps** for each occurrence. It works for **both English and Hindi videos** and handles **partial matches, full sentences, and individual words**. Perfect for quickly finding important moments in lectures, tutorials, or online classes. **It also provides the full transcript of the video**.

---
# 📸 Screenshot Of The Engine
Here are some screenshots of the **Search in Video Engine** in action:

## Hindi Video

<div align="center">
<img width="1088" height="321" alt="image" src="https://github.com/user-attachments/assets/1ed4d348-2e95-48fb-871c-976c8d8a52c5" />
<img width="1026" height="478" alt="image" src="https://github.com/user-attachments/assets/920f77b2-4ac3-48ca-92c1-da5585e67ba9" />
<img width="1022" height="492" alt="image" src="https://github.com/user-attachments/assets/5e900270-e7af-46e5-b19c-c3b918e3b0fe" />
<img width="1043" height="324" alt="image" src="https://github.com/user-attachments/assets/f4298bc8-1b38-4ed0-b4cc-12a6f79e34ec" />
</div>

## English Video

<div align="center">
<img width="983" height="344" alt="image" src="https://github.com/user-attachments/assets/a6eb3f8e-0646-4010-abd9-2fa850a863f7" />
<img width="950" height="482" alt="image" src="https://github.com/user-attachments/assets/d8712bee-ffa7-4575-b983-11595f9adae9" />
</div>

---

## ✨ Features

* 📥 Works with **YouTube URLs** or **local video files**.
* 🗣 **Automatic speech-to-text transcription** using Google Speech Recognition.
* 🕒 Finds **timestamps** for every word, partial phrase, or full sentence in the video.
* 🌐 Supports **English and Hindi**.

  * For **Hindi videos**, search using the **spoken Hindi word** (e.g., type `paani` to search for पानी).
  * For **English videos**, search in English text.
* 🔍 Optional **fuzzy matching** to find approximate or misspoken words.
* ⚡ Works on **Google Colab** or **locally**.

---

### 🎯 How to Use

1. Input **only three things**:

   * Video **path** or **YouTube URL**
   * Video **language** (`en` for English, `hi` for Hindi)
   * **Word(s) or sentence** to search

2. You can enter:

   * **A single word** → finds all occurrences of that word in the video.
   * **A full sentence** → finds the exact sentence, partial phrases, and all individual words.
   * **Multiple words that may occur together or separately** → finds each word individually, as well as any combination of the words appearing together.

3. Examples:

   * **English video**:

     * Search for `color` → finds all mentions of "color".
     * Search for `machine learning basics` → finds the full sentence, partial phrases, and individual words.
   * **Hindi video**:

     * Search for `paani` → finds all mentions of पानी, not "water".
     * Search for `mera naam gautam hai` → finds the full sentence, partial phrases, and individual words.

4. Optional: **Fuzzy Matching**

   * Fuzzy matching finds **similar words** if the exact word isn’t pronounced clearly.
   * **Cutoff values** (0 to 1):

     * `0` → very lenient, matches almost everything similar
     * `1` → strict, matches only exact words
   * Example:

     * Searching `colour` in an English video, fuzzy cutoff `0.8` → matches both `color` and `colour`.
     * Searching `paani` in Hindi video, fuzzy cutoff `0.9` → matches only words very close to `paani`.

5. Output includes:

   * **Timestamps for each word**
   * **Timestamps for full sentences**
   * **Timestamps for partial matches** (all possible combinations)
  
> This ensures you never miss any important part of the video.
---

## 🚀 Run in Google Colab

### Option 1 - Direct Link

Click the badge below to open the project in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/17rl76jkREnAk-cqKkBsB_JJaBGDpl_fl)


### Option 2 - Manual Upload

1. Download the notebook (`.ipynb`) from this repository.
2. Upload it to Google Colab.
3. Double-click the uploaded file to open.
4. Run all cells to execute.

---

## 💻 Run Locally (VS Code)

1. Download the notebook or `.py` file and open it in VS Code.
2. Install dependencies (run the below command in terminal):

```bash
pip install moviepy pydub SpeechRecognition yt-dlp deep-translator
```

3. Install **FFmpeg** (required for video processing):

* **Windows:** Download from [FFmpeg builds](https://www.gyan.dev/ffmpeg/builds/) and add to PATH.
* **macOS:**

```bash
brew install ffmpeg
```

* **Linux:**

```bash
sudo apt-get install ffmpeg
```

4. Comment or Delete the installation line from the code (.py file).
   
```bash
# !pip install moviepy pydub SpeechRecognition yt-dlp deep-translator
```

5. Run the code (.py file) using VS Code’s run button or in the terminal:
```bash
python search-in-video-engine.py
```

---

## 🖥 How It Works

1. Enter a **YouTube video link** or **local video path**.
2. Enter the **language** (`en` or `hi`).
3. Enter the **word or sentence** to search.
4. Optionally enable **fuzzy matching**.
5. Wait for processing — the engine will:

   * Extract audio from video
   * Convert audio to text
   * Search for your word or sentence
   * Return **timestamps** for all occurrences of words, sentences, and partial phrases

---

## 📜 License

This project is **open-source under the MIT License** — feel free to use, modify, and share.



