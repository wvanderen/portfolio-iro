---
layout: post
title: BlocJams
feature-img: img/sample_feature_img.png"
thumbnail-path: "img/BlocJamsCrop.png"
short-description: BlocJams is a Spotify replica I build while learning the fundamentals of HTML, CSS, Javascript, and JQuery.
---

# Summary:
BlocJams is a Spotify replica I build while learning the fundamentals of HTML, CSS, Javascript, and JQuery.
# Explanation:
As part of the Bloc curriculum, I was challenged very early on to apply the programming skills I'd learned to build a working application.
# Problem:
The challenge was to build a working music player from the ground up. This included building the page structure of the application as well as scripting to make the player functional.
# Solution:
First, I was guided to build the HTML and CSS of the various pages. Later on, I employed DOM scripting and later JQuery to make the player functional.
# Results:
I successfully completed the project and gained a great deal of experience in the process. As part of the work I did for this project, I was asked to the write the function that plays the next song when the next button is played on my own. Here is the code from that assignment:

{% highlight javascript %}
var nextSong = function() {
  var nextSongNumber = parseInt($(this).attr('data-song-number'));
  //gets number of new song to set. Loops around if last song
  if (trackIndex(currentAlbum, currentSongFromAlbum) < (currentAlbum.songs.length -1)) {
      nextSongNumber = (trackIndex(currentAlbum, currentSongFromAlbum) +2);
  } else {
      nextSongNumber = 1;
  }
  var updatePlayerBarSong = function() {
    //Updates text in player bar based on current song
    $('.currently-playing .song-name').text(currentSongFromAlbum.title);
    $('.currently-playing .artist-song-mobile').text(currentSongFromAlbum.title + currentAlbum.artist);
    $('.currently-playing .artist-name').text(currentAlbum.artist);
    //Updates status of play/pause button in playerbar
    $('.main-controls .play-pause').html(playerBarPauseButton);
    setTotalTimeInPlayerBar(currentSongFromAlbum.duration);
  };

    //Sets previously playing song to a number and sets currentlyPlayingSongNumber to new song
    //Plays next song
    var previouslyPlayingCell = getSongNumberCell(currentlyPlayingSongNumber);
    previouslyPlayingCell.html(currentlyPlayingSongNumber);
    setSong(nextSongNumber);
    currentSoundFile.play();
    updateSeekBarWhileSongPlays();
    //Sets new song to pause button and updates player bar
    var currentlyPlayingCell = getSongNumberCell(currentlyPlayingSongNumber);
    currentlyPlayingCell.html(pauseButtonTemplate);
    updatePlayerBarSong();
};
{% endhighlight %}

# Conclusion:
This project was a great opportunity to get practical experience working with Javascript and JQuery. I was challenged to step back and really think about how the problem should be solved before attempting to implement a solution. Confronted with problems more complex than I'd tackled before, I was forced to learn by doing, sometimes requiring extensive troubleshooting and research. Through this process I learned to persevere through many of the difficulties associated with programming.
