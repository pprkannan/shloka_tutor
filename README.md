# Shloka Tutor

A browser-based chanting practice app. Listen to a recording, repeat it aloud, and hear your own repetition played back — for any Sanskrit (or other) chant, organized into named collections (e.g. "Lalitha Sahasranamam", "Vishnu Sahasranamam").

## Features

- **Collections**: create separate named sets (e.g. one per text you're learning), each with its own audio and text.
- **Audio upload**: upload one recording per shloka (name the file with its number, e.g. `shloka4.mp3`). The app automatically splits each recording into per-name segments using silence detection.
- **Listen → Repeat → Hear yourself**: each segment plays once, then gives you three timed pauses to repeat aloud — recording you via the microphone and playing it back so you can hear your own pronunciation.
- **Short segments** (e.g. a standalone "Om") are played once with no repeat cycle.
- **Optional text display**: upload a `.txt`, `.docx`, or `.pdf` file containing the shloka text (numbered), and the matching shloka's Sanskrit/English is shown during practice.
- **Start anywhere**: jump to any shloka number to begin a session.
- **Pace control** and **Pause/Resume**.
- **Local persistence**: audio and text are saved in the browser's IndexedDB so they're available next time without re-uploading.
- **Backup/restore**: export all collections to a JSON file, and import it back — useful for moving between devices/browsers or recovering data.

## Usage

Open `index.html` in a modern browser (Chrome, Safari, Edge, Firefox). For best results — especially reliable local storage — host it via a real URL (e.g. GitHub Pages) rather than opening the file directly from disk, since some mobile browsers restrict storage for `file://` pages.

### Hosting via GitHub Pages

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Set the source to the `main` branch, root folder (`/`).
4. Your app will be available at `https://<your-username>.github.io/<repo-name>/`.

## File naming conventions

- **Audio files**: include the shloka number, e.g. `shloka1.mp3`, `shloka40.m4a`, `sloka4.wav`, `verse12.ogg`. Supported formats: mp3, wav, m4a, ogg, aac, flac, amr, 3gp, opus, wma (anything your browser can decode).
- **Text files**: mark each shloka with its number at the start of a line, e.g. `1.`, `Shloka 4`, `॥ 40 ॥`, `(12)`. Devanagari lines are treated as Sanskrit; other lines as English/transliteration.

## Privacy

All processing (audio segmentation, silence detection, microphone recording/playback, text parsing) happens entirely in your browser. Nothing is uploaded to any server.

## License

MIT
