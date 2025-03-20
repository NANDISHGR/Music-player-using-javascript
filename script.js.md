// Get DOM elements
const audioPlayer = document.getElementById('audio-player');
const playPauseButton = document.getElementById('play-pause-button');
const prevButton = document.getElementById('prev-button');
const nextButton = document.getElementById('next-button');
const volumeSlider = document.getElementById('volume-slider');
const trackTitle = document.getElementById('track-title');
const artist = document.getElementById('artist');
const albumArt = document.getElementById('album-art');

// Define a list of tracks
const tracks = [
    {
        title: "Song One",
        artist: "Artist One",
        file: "assets/audio/song1.mp3",
        art: "assets/images/album1.jpg"
    },
    {
        title: "Song Two",
        artist: "Artist Two",
        file: "assets/audio/song2.mp3",
        art: "assets/images/album2.jpg"
    },
    {
        title: "Song Three",
        artist: "Artist Three",
        file: "assets/audio/song3.mp3",
        art: "assets/images/album3.jpg"
    }
];

let currentTrackIndex = 0;

// Function to load a track
function loadTrack(index) {
    const track = tracks[index];
    audioPlayer.src = track.file;
    trackTitle.textContent = track.title;
    artist.textContent = track.artist;
    albumArt.src = track.art;
    audioPlayer.play();
    playPauseButton.textContent = '⏸️';
}

// Play/Pause functionality
playPauseButton.addEventListener('click', () => {
    if (audioPlayer.paused) {
        audioPlayer.play();
        playPauseButton.textContent = '⏸️';
    } else {
        audioPlayer.pause();
        playPauseButton.textContent = '▶️';
    }
});

// Previous track functionality
prevButton.addEventListener('click', () => {
    currentTrackIndex = (currentTrackIndex - 1 + tracks.length) % tracks.length;
    loadTrack(currentTrackIndex);
});

// Next track functionality
nextButton.addEventListener('click', () => {
    currentTrackIndex = (currentTrackIndex + 1) % tracks.length;
    loadTrack(currentTrackIndex);
});

// Volume control functionality
volumeSlider.addEventListener('input', () => {
    audioPlayer.volume = volumeSlider.value;
});

// Load the first track when the page loads
window.addEventListener('load', () => {
    loadTrack(currentTrackIndex);
});
