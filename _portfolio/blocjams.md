---
layout: post
title: BlocJams
thumbnail-path: "img/blocflix.png"
short-description: BlocFlix is a Netflix replica for finding the best movies and watching them online.

---


## Explanation

As part of the Foundation Frontend Web Development portion of Bloc's Software Developer Track, we were tasked to develop an application that works similar to Spotify.

## Problem

Users must be able to do the following:

* Play songs, to include adjust volume, seeking, and autoplay next songs
* Have a seekbar to control the player from any page on the application

## Solution

For this project, I used [AngularJS](http://angularjs.org), to develop the single page app with [Grunt](https://gruntjs.com) as the task runner. No persistance of the data was necessary, so it all lives and dies with the session. For controlling the player I used [Buzz](http://buzz.jaysalvat.com/) a small Javascript HTML5 library.

#### A note on routing

I opted to use [AngularUI Router](https://github.com/angular-ui/ui-router) instead of the built in AngularJS system due to it's flexibility and additional features. With Ui-Router, an application can be in different states that determine what to display when a user navigates to a specific route. Ui-Router will take care of replacing the contents with a template when a user navigates to the proper route. Each template can be unique, while the shared code is kept in the global file.

#### Player bar

In order to play songs from an album effectively and without interruption, we created a player bar that is included on the user, collection, album, and search templates. The songs can be selected and played from the album. We serve the data for the album via the Fixtures.js service and manage the state of the song player via SongPlayer.js service.

We manage the seek and volume bars via the seek-bar.js directive. We can customize the seek bars via passing attributes within the HTML.

## Results

Users are able to find and play songs of choice, and jam out!

## Conclusion

While there may be more powerful online music stores, AngularJS, combined with AngularUI router provides a powerful framework to create dynamic, single-page applications.
