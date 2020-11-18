![TuneFull](img/tunefull-logo.png)

## Client-side design and implementation

### Client functionality

Once logged in, users are able to perform a variety of actions such as adding or deleting friends and follows. Users have access to a feed of recent clips posted by those on the network. Additionally, they can post 20 to 30 second sound bites of music which are added to their profile. Clicking on a clip allows the user to listen and discover information about the artist, song and album. Users who are not logged in can access this feature to some extent, but are not able to follow and friend other users or post their own music.

### [Wireframe](wireframe.md)

### Device and external services used:

* Device audio, accessed through MediaPlayer [(Overview)](https://developer.android.com/guide/topics/media/mediaplayer) [(Documentation)](https://developer.android.com/reference/android/media/MediaPlayer)

    * Audio is used to play the music clips on the client side of the app.

    * Audio is critical to meaningful functionality of the app.

* Google Sign-in [(Documentation)](https://developers.google.com/identity/sign-in/android/start-integrating)

    * Sign-in lets the user create and log into their account. The client app will authenticate with Google and pass the authentication token to the server. 
                                                                                                                                                                                                                    
    * Sign-in is required for full usage of the app. The discovery feature can be used without sign-in, but these users will not be able to follow accounts, or post music. 
    
* Spotify API [(Android SDK)](https://developer.spotify.com/documentation/android/) [(Web API)](https://developer.spotify.com/documentation/web-api/reference-beta/)

    * Spotify API enables clips to be played through the app, and allows for clips to redirect to the full song on Spotify. The server will likely also need access to Spotify. 

    * Access to Spotify API or some other music API is necessary for the functioning of this app.
    
> [Return to previous page](index.md)