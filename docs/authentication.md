## Authentication scheme

The authentication scheme used is Google Sign-in ([Documentation](https://developers.google.com/identity/sign-in/android/start-integrating)). Sign-in lets the user log into the app with their Google account. The client app authenticates with Google and passes the authentication token on to the server. Sign-in is required for full usage of the app, though Discovery mode in its most basic form can be used by a user who has not signed in.   

###[Server-side security configuration](https://github.com/tunefull/tunefull-service/blob/master/src/main/java/edu/cnm/deepdive/tunefull/configuration/SecurityConfiguration.java)

>[Return to previous page](index.md#authentication-scheme)