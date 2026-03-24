# Three-Track Random Mixer

🔗 Live demo: https://s2d01.github.io/three-track-random-mixer/


A lightweight browser-based tool to quickly audition and layer three random audio tracks from your local files.
Designed for producers and sound designers who want fast, no-bullshit experimentation without installing a full plugin.

---

## Features

* **Local-only audio loading**

  * Drag & load multiple audio files from your machine
  * No upload, no backend, no tracking

* **Random 3-track selection**

  * `🎲 Pick 3 Random Tracks` chooses three files from your pool
  * Tracks section appears only after a valid random selection

* **Per-track controls**

  * `▶` **Play** – plays the selected track (respects pause position if resumed)
  * `⬛` **Stop** – stops and resets that track
  * `🔊` **Preview** – 5-second preview from the start (non-destructive)
  * `◀` **Reverse** – toggle reverse playback per track

    * dimmed = OFF, solid red = ON
  * Individual volume slider per track

* **Global controls**

  * `▶️ Play All` – plays all three tracks together
  * `🔄 Loop All` – enables looping:

    * if active, each track restarts automatically when it ends
    * if enabled while nothing is playing, it starts the 3 tracks and keeps them looping
  * `⏸️ Pause All` – pauses all playing tracks and remembers positions
  * `⏹️ Stop All` – stops everything and resets positions

* **Simple preset system (mix memory)**

  * `💾 Save This Mix` – saves current 3-track combo by **file name**
  * Saved mixes are listed with their track names
  * `📤 Export Mixes` – export all saved mixes as JSON
  * `📥 Import Mixes` – re-import previously exported presets
  * `Load` button on each preset:

    * if the corresponding files (same names) are currently loaded, it rebuilds the mix
    * if files are missing, you’re notified and can reload them manually

---

## How It Works

* Built with **plain HTML, CSS and JavaScript** using the **Web Audio API**.
* All audio is processed **client-side in your browser**.
* For security and privacy reasons, browsers don’t expose full filesystem paths:

  * presets store **file names only**, not absolute paths;
  * to reuse a preset, you simply load the same files again.

This project is intentionally minimal:

* no frameworks,
* no build step,
* easy to read, fork, break, improve.

---

## Usage

1. Open `index.html` in a modern browser (Chrome/Chromium recommended).
2. Click **Choose Files** and select multiple audio files.
3. Hit **🎲 Pick 3 Random Tracks**.
4. Use per-track and global controls to audition combinations.
5. Optionally save mixes and export/import your preset list.

Supported formats depend on the browser (commonly: `.wav`, `.mp3`, `.ogg`, `.m4a`, etc.).

---

## Roadmap / Ideas

* Smarter randomization rules (tags, folders, type filtering).
* Better visual feedback (levels, activity, state indicators).
* Desktop app version (Swift- Mac only for now) with persistent libraries.

---

## License

MIT

Feel free to fork, break, and adapt it to your workflow.
