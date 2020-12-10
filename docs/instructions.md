## Instructions for Building and Using

### Instructions for Building

1. Go to the [TuneFull GitHub repository](https://github.com/tunefull/tunefull)

2. Click on Clone or download

3. Make sure Clone with SSH is selected and click the clipboard icon to copy the SSH key

4. Use the IntelliJ Check out from Version Control/Git (from the welcome screen) or File/New/Project from Version Control/Git (from the workspace) command to clone

5. Once downloaded, build the project by clicking the green hammer icon or Build Project in Build Menu

6. If desired, repeat Previous steps to run the [TuneFull Server](https://github.com/tunefull/tunefull-service) locally. The server is currently running in the cloud as well.

7. Make sure tunefullproperties.properties is configured to direct to either your local server or to the cloud. This file should be stored in a services directory in this location: (projectDir/../../../services/tunefullproperties.properties).  

8. Once finished building, run the Server side project if desired so that a connection with endpoints can be established, then run the Client Application by clicking the green arrow icon or Run app from Run menu

### Instructions for Using

* TuneFull will first ask you to log in with Google sign-in.

* After that, TuneFull will ask you to sign into Spotify, which can also be done with a Google Account or through Facebook.

* To complete signin, the user will accept a prompt requesting various permissions for conrolling the Spotify App Remote.

* The application will then take you to the "Discovery" screen where you can begin to browse clips of music TuneFull users have posted.

* In the "TuneFull Feed" tab users can listen to music clips from all their friends and those they have followed.

* The "My clips" tab shows the music clips you have posted. 

* The "My liked songs" tab shows the songs you have liked/saved on Spotify. Here you can listen and create clips. This screen can also be reached by a floating action button on any of the other tabs.

* The "User Profile" tab allows users to:
    * Set their genre mood
    * View a friend request
    * View a list of friends
    * View a list of follows
    * Logout for Google sign-in

> [Return to previous page](index.md#instructions-for-building-and-using)