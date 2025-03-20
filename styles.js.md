/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f9;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: #333;
}

/* Music Player Container */
.music-player {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 300px;
    text-align: center;
}

.music-player h1 {
    font-size: 24px;
    margin-bottom: 20px;
}

/* Track Info Section */
.track-info {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
}

.track-info img {
    width: 80px;
    height: 80px;
    border-radius: 10px;
    margin-right: 15px;
}

.track-info p {
    margin: 5px 0;
    font-size: 16px;
}

#track-title {
    font-weight: bold;
}

#artist {
    color: #777;
}

/* Controls Section */
.controls {
    display: flex;
    justify-content: space-around;
    margin-bottom: 20px;
}

.controls button {
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
    transition: transform 0.2s ease;
}

.controls button:hover {
    transform: scale(1.1);
}

/* Volume Control Section */
.volume-control {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 20px;
}

.volume-control label {
    margin-right: 10px;
    font-size: 14px;
}

.volume-control input[type="range"] {
    width: 100px;
    cursor: pointer;
}

/* Responsive Design */
@media (max-width: 400px) {
    .music-player {
        width: 90%;
    }

    .track-info img {
        width: 60px;
        height: 60px;
    }

    .controls button {
        font-size: 20px;
    }
}
