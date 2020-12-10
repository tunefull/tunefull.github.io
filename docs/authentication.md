## Authentication scheme

The authentication scheme used is Google Sign-in ([Documentation](https://developers.google.com/identity/sign-in/android/start-integrating)). Sign-in lets the user log into the app with their Google account. The client app authenticates with Google and passes the authentication token on to the server. Sign-in is required for use of the app.

### [Server-side security configuration class](https://github.com/tunefull/tunefull-service/blob/master/src/main/java/edu/cnm/deepdive/tunefull/configuration/SecurityConfiguration.java)

The client app also uses Spotify Sign-in through OpenId. This allows the user to connect with their Spotify account and get their liked songs. Spotify sign-in is required for use of the app.

>[Return to previous page](index.md#authentication-scheme)