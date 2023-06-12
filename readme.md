# Music Player Project

This is a simple music player project implemented in JavaScript. It allows you to play, pause, skip to the previous or next song, and track the progress of the currently playing song. The project consists of HTML, CSS, and JavaScript code.

## Prerequisites

To run this project, you need a web browser that supports JavaScript.

## Usage

To use the music player, follow these steps:

1. Open the project in a web browser.
2. The music player will load with the first song selected and ready to play.
3. Click the "Play" button (represented by a play icon) to start playing the song. The button will change to a "Pause" button (represented by a pause icon) once the song starts playing.
4. To pause the song, click the "Pause" button. It will change back to the "Play" button.
5. To skip to the previous song, click the "Previous" button.
6. To skip to the next song, click the "Next" button.
7. The progress bar at the bottom of the player displays the progress of the currently playing song. You can click on the progress bar to skip to a specific position in the song.

## Code Explanation

The JavaScript code controls the functionality of the music player. Here's a breakdown of the different components and their purpose:

### Variables

- `image`, `title`, `artist`, `music`, `progressContainer`, `progress`, `currentTimeEl`, `durationEl`, `prevBtn`, `playBtn`, and `nextBtn`: These variables store references to various elements in the HTML document using JavaScript's `querySelector` or `getElementById` methods.
- `songs`: This array contains objects representing different songs. Each object has properties such as the song name, display name, and artist.
- `isPlaying`: This variable keeps track of whether a song is currently playing or paused.
- `songIndex`: This variable stores the index of the currently selected song in the `songs` array.

### Functions

- `playSong`: This function is called when the "Play" button is clicked. It sets the `isPlaying` variable to `true`, updates the button's appearance, and plays the music.
- `pauseSong`: This function is called when the "Pause" button is clicked. It sets the `isPlaying` variable to `false`, updates the button's appearance, and pauses the music.
- `loadSong`: This function takes a song object as a parameter and updates the player's UI elements with the corresponding song information. It also sets the source of the audio element and the image source for the album cover.
- `prevSong` and `nextSong`: These functions handle the logic for skipping to the previous and next songs, respectively. They update the `songIndex` variable, load the new song, and play it.
- `updateProgressBar`: This function is called during playback to update the progress bar and display the current time and duration of the song.
- `setProgressBar`: This function is called when the progress bar is clicked. It calculates the position within the song based on the click position and sets the current time of the music accordingly.

### Event Listeners

The project includes several event listeners to respond to user actions:

- The "Play/Pause" button has a click event listener that toggles between playing and pausing the song based on the `isPlaying` variable.
- The "Previous" and "Next" buttons have click event listeners that call the `prevSong` and `nextSong` functions, respectively.
- The `music` element has an "ended" event listener that automatically moves to the next song when the current song finishes.
- The `music` element also has a "timeupdate" event listener that triggers the `updateProgressBar` function to update the progress bar and time display during playback.
- The progress bar container has a click event listener that calls the `setProgressBar` function when clicked.

## Conclusion

This music player project demonstrates the basic functionality of playing and managing songs using JavaScript. You can customize it by adding more songs to the `songs` array or modifying the UI elements to suit your needs. Have fun exploring and enhancing the project!