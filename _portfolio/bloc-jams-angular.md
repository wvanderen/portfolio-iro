---
layout: post
title: BlocJams Angular
feature-img: "img/sample_feature_img.png"
thumbnail-path: "img/blocjamsfront.png"
short-description: I refactored my earlier BlocJams project to use an AngularJS framework.

---

# Summary:
I refactored my earlier BlocJams project to use an AngularJS framework.

# Explanation:
This project was my first introduction to Angular, I learned how to use it while implementing it on the BlocJams project, which I had already completed.

# Problem:
The challenge here was comprehending and learning how to use Angular.
# Solution:
Through my work on this project, I gained a working understanding of templates, controllers, services, directives, and filters and the relationship between them. I now have the experience to take forward into future projects where I work with Angular.

# Results:
At first, I had difficulty understanding Angular and how the various pieces fit together. However, gradually over the course of the project, these concepts clicked and I gained confidence and competence with this framework. For reference, I've included my Next Song function from this project, which can compared to the function from the other BlocJams project which has similar functionality:

{% highlight javascript %}
/**
* @function Songplayer.next
* @desc Increments currentSongIndex and navigates to next song
*/
SongPlayer.next = function() {
  song = song || SongPlayer.currentSong;
  var currentSongIndex = getSongIndex(SongPlayer.currentSong);
  currentSongIndex++;

  if (currentSongIndex >= currentAlbum.songs.length) {
    stopSong(song);
  } else {
    var song = currentAlbum.songs[currentSongIndex];
    setSong(song);
    playSong(song);
  }
};
{% endhighlight %}

# Conclusion:
This project was a helpful introduction to the Angular framework and gave me practical experience working with it. I see much value in Angular, especially in its ability to work with declarations right in the template, as well as keeping the application highly organized.
