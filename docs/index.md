## Summary

The TuneFull music network bundles together fun and discovery to provide its users with a positive and friendly music sharing experience. Tune in to share 20-30 second clips of music that match your mood, and see what music clips your friends are sharing. You can also listen to clips posted by people outside your friend circle to discover new music, or follow those with similar taste.

[Client Functionality](client-functionality.md)

[Server Functionality](server-functionality.md)

## Intended users and user personas

* People who like social media, except for its negativity.

    > [Bethany Ford](personas/persona.md)
    
* People who want to quickly discover new music.
	
	> [Jackson Riley](personas/persona-2.md)

## Device/external services

* Device audio, accessed through MediaPlayer [(Overview)](https://developer.android.com/guide/topics/media/mediaplayer) [(Documentation)](https://developer.android.com/reference/android/media/MediaPlayer)

    * Audio is used to play the music clips.

    * Audio is critical to the functionality of the app.

* Google Sign-in [(Documentation)](https://developers.google.com/identity/sign-in/android/start-integrating)

    * Sign-in lets the user create and log into their account. The client app will authenticate with Google and pass the authentication token to the server. The server will also need access to Google Sign-In: it will take the token passed by the client and will authenticate with Google. 
                                                                                                                                                                                                                    
    * Sign-in is required for full usage of the app. The discovery feature can be used without sign-in, but these users will not be able to follow accounts, or post music. 
    
* Spotify API [(Android SDK)](https://developer.spotify.com/documentation/android/) [(Web API)](https://developer.spotify.com/documentation/web-api/reference-beta/)

    * Spotify API enables clips to be played through the app, and allows for clips to redirect to the full song on Spotify. The server will likely also need access to Spotify. 

    * Access to Spotify API or some other music API is necessary for the functioning of this app.

## [Entity relationship diagram](erd.md)

## [Data Model Implementation](data-model-implementation.md)

