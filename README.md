<p align="center"><img src="https://raw.githubusercontent.com/BezelMedia/Bezel/main/.github/assets/bezel.svg" width="90" height="90" alt="Bezel"></p>

<h1 align="center">Bezel Community</h1>

<p align="center">Themes, TV channel packs and bezel frames for <a href="https://github.com/BezelMedia/Bezel">Bezel</a> — made by the community, installed with one click from the app's <b>🧩 Community</b> tab.</p>

---

## Contribute a pack

Open a pull request that adds **your file(s)** and **one entry in `index.json`**. That's it — once merged, it shows up in everyone's Community tab.

### 🎨 Themes — `themes/<id>.json`

The same JSON you get from **Settings → Appearance → Copy** in Bezel:

```json
{
  "name": "Midnight Purple",
  "base": "dark",
  "vars": {
    "--accent": "#b18cff",
    "--accent-soft": "rgba(177, 140, 255, 0.16)",
    "--accent-line": "rgba(177, 140, 255, 0.5)",
    "--bg": "#0d0a14"
  }
}
```

`base` is `dark` or `light`. `vars` may override any of Bezel's CSS variables — `--accent`, `--accent-soft`, `--accent-line`, `--bg`, `--surface`, `--surface-2`, `--surface-3`, `--line`, `--line-soft`, `--text`, `--text-dim`, `--text-faint`.

### 📺 TV channel packs — `channels/<id>.json`

An array of channels for Bezel's TV tab. Keep them **login-free and DRM-free** (YouTube/Twitch pages, web radio):

```json
[
  { "name": "Games Done Quick", "sub": "Speedrun marathons", "url": "https://www.youtube.com/@gamesdonequick", "color": "#2f80ed", "emoji": "🏁" }
]
```

### 🖼️ Bezel frames — `bezels/<id>.png`

A 1920×1080 PNG with a **transparent centre** where the game shows (4:3 centre ≈ 1400×1050 works well for the in-app player). Keep files under ~2 MB.

### `index.json` entry

```json
{ "id": "theme-midnight-purple", "kind": "theme", "name": "Midnight Purple", "author": "you", "description": "One line about it.", "file": "themes/midnight-purple.json", "accent": "#b18cff" }
```

`kind` is `theme`, `channels`, or `bezel`. `file` must be a relative path inside this repo. For bezels you can add `"preview": "bezels/<id>.png"`.

## Ground rules

- Your own work (or clearly licensed), no copyrighted logos/box art in frames.
- Channels: no login-required, DRM'd, or NSFW destinations.
- One pack per PR keeps review quick.

Questions or ideas → [r/Bezel](https://www.reddit.com/r/Bezel/) · [retrobezel.com](https://retrobezel.com)
