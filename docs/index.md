## Summary

The TuneFull music network bundles together fun and discovery to provide its users with a positive and friendly music sharing experience. Tune in to share 20-30 second clips of music that match your mood, and see what music clips your friends are sharing. You can also listen to clips posted by people outside your friend circle to discover new music, or follow those with similar taste.

**Client Functionality**

Once logged in users are able to perform a variety of actions such as adding or deleting friends and follows. Users have access to a feed of recent clips posted by those on the network. They too can post 20 to 30 second sound bytes of music which are added to their profile. Just click on a clip to listen and discover information about the artist, song and album. Users who are not logged in can access this feature to some extent, but are not able to follow or friend other users. The app also includes settings such as color themes.
    	
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

    * Sign-in lets the user create and log into their account. The client app will authenticate with Google and pass the authentication token to the server. The server will also need access to Google Sign-In: it will take the token passed by the client, and will authenticate it with Google. 
                                                                                                                                                                                                                    
    * Sign-in is required for full usage of the app. The discovery feature can be used without sign-in, but these users will not be able to follow accounts. 
    
* Spotify API [(Android SDK)](https://developer.spotify.com/documentation/android/) [(Web API)](https://developer.spotify.com/documentation/web-api/reference-beta/)

    * Spotify API allows for clips to be played through the app, and allows for clips to link to the full song on Spotify. The server will likely also need access to Spotify. 

    * Access to Spotify API or some other music API is necessary for the functioning of this app.

## [Entity relationship diagram](erd.md)

