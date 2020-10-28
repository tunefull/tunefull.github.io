## Summary

TuneFull is a social network designed for fun, discovery, and positivity. Users of this app can share a 20 to 30-second clip of music that matches their mood, and can see and listen to a feed of clips their friends have shared. Additionally, users can listen to clips posted by people outside their friend circle to discover new music or to follow people who have similar musical tastes.

**Client Functionality**

Once the user is logged in, they are able to do a variety of actions. They can add or delete friends and follows, post a 20 to 30-second clip of music to their profile, and see a feed of their friends’ recent clips. They can click to listen, and clips also include information about the artist, song, and album. The user can also discover new music by browsing clips from non-friends. If they like the clip, they can get information about the song and/or follow the person who posted it. Users who are not logged in can access this feature to some extent, but are not able to follow or friend other users. The user can also change settings, such as color themes.
    	
**Server Functionality**

The server will host the database, and will provide data to the client when requested. This data might include a list of the user's friends, a feed of clip posts by the user's friends and follows, or a feed of clip posts from non-friend users for use in the discovery feature. The server will take and store input from the client, including clip posts and friend requests/accepts.

## Intended users

* People who like social media, except for its negativity.

    > I like to keep up with my friends on social media, but recently have become so burnt out with all of the negativity. I need a social network that is positive so I can connect with friends without extra stress, and TuneFull lets me do that.
    
* People who want to quickly discover new music.
	
	> As a music lover, I enjoy discovering new music-—but I’m a busy person, and don’t have time to listen to whole songs. TuneFull allows me to listen to short clips of music, so I can find more new music in less time.

## Device/external services

* Device audio, accessed through MediaPlayer [(Overview)](https://developer.android.com/guide/topics/media/mediaplayer) [(Documentation)](https://developer.android.com/reference/android/media/MediaPlayer)

    * Audio is used to play the music clips.

    * Audio is critical to the functionality of the app.

* Google Sign-in [(Documentation)](https://developers.google.com/identity/sign-in/android/start-integrating)

    * Sign-in lets the user create and log into their account. The client app will authenticate with Google and pass the authentication token to the server. The server will also need access to Google Sign-In. This will help with user authentication and creating accounts. The server will take the token passed by the client, and will authenticate it with Google. 
                                                                                                                                                                                                                    
    * Sign-in is required for full usage of the app. The discovery feature can be used without sign-in, but these users will not be able to follow accounts. 
    
* Spotify API [(Android SDK)](https://developer.spotify.com/documentation/android/) [(Web API)](https://developer.spotify.com/documentation/web-api/reference-beta/)

    * Spotify API allows for clips to be played through the app, and allows for clips to link to the full song on Spotify. The server will also need access to Spotify. 

    * Access to Spotify API or some other music API is necessary for the functioning of this app.

## [Entity relationship diagram](erd.md)

