## Current implementation state

### Current state

The client application includes multiple screens, some of which share the same fragment to display different content. Navigation is performed through tab/swipe navigation; in addition, buttons on certain screen redirect to dialogs or other screens. The client communicates with a server application running on a droplet configured with Ubuntu. Commuication follows REST principles and primarily uses JSON to transport data. The server hosts a database of users, clips, and relationships, and this data is used to provide the content for the client to populate lists in various screens. The client app also connects with the Spotify API to get information about the user's liked tracks, and can play music through Spotify using the Spotify App Remote SDK. Authentication is performed both through Google sign-in and through Spotify OpenId OAuth 2.0 sign-in. The app also contains many custom vector icons, as well as some standard vector icons from the built-in clip-art library.

### Deficiencies/bugs

* The Spotify App Remote does not connect correctly on some devices.

* Tracks played are not always the correct tracks.

* Clips do not automatically pause the Spotify player as intended.

* Relationship feeds currently are blank, with no useable content.

* The set genre dialog/spinner does not update the server database.

* Content and buttons on different feeds are not always tied to the particular feed type.

* The logout button does not yet work to log out from Google sign-in. Spotify authentication prompts the user to log in frequently enough that this is not much of an issue. 

### Aesthetic stretch goals

* Custom font

### Functional stretch goals

* If the user doesn't have Spotify installed on their phone, link them to the Google Play Store page for the Spotify app.

* Genre updates show in the TuneFull feed (friends and follows).

> [Return to previous page](index.md#current-implementation-state)