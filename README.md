# Bassline Swarm Music Choice Build

This build keeps **streaming DnB radio as the default** and adds a home/pause menu music selector:

- Stream DnB radio
- Local MP3 loop
- Built-in synth fallback

## Local MP3 Option

To use your own track, put an MP3 here:

```text
assets/music/bassline-loop.mp3
```

Keep that exact filename. Later, if you make a better loop, replace the file with a new MP3 using the same name and the game will use the new song.

The game sets the local MP3 to loop. If the file is missing and the player chooses **Local MP3 loop**, the game shows a warning and falls back to the built-in synth.

## GitHub Notes

This package intentionally does **not** include an MP3, so it is safe to upload to GitHub without committing your music file.

The `assets/music/PUT-MP3-HERE.txt` file is just a placeholder so GitHub keeps the folder.

## PWA Notes

When served from `localhost` or HTTPS, the service worker caches the app shell. The MP3 path is handled network-first so replacing `assets/music/bassline-loop.mp3` can update without code changes.

## Run Locally

Open `index.html` directly for a quick test, or serve the folder for PWA behavior:

```powershell
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```
