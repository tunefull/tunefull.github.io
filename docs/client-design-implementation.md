## Client-side design and implementation

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
    
### [Wireframe](wireframe.md)

> [Return to previous page](index.md#client-side-design-and-implementation)