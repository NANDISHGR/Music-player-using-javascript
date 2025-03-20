<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Player</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="music-player">
        <h1>Music Player</h1>
        <div class="track-info">
            <img id="album-art" src="assets/images/album-art.jpg" alt="Album Art">
            <div>
                <p id="track-title">Track Title</p>
                <p id="artist">Artist Name</p>
            </div>
        </div>
        <div class="controls">
            <button id="prev-button" aria-label="Previous Track">⏮️</button>
            <button id="play-pause-button" aria-label="Play/Pause">▶️</button>
            <button id="next-button" aria-label="Next Track">⏭️</button>
        </div>
        <div class="volume-control">
            <label for="volume-slider">Volume:</label>
            <input type="range" id="volume-slider" min="0" max="1" step="0.1" value="1">
        </div>
        <audio id="audio-player" src="assets/audio/sample-track.mp3"></audio>
    </div>

    <script src="script.js"></script>
</body>
</html>
