![TuneFull](img/tunefull-logo.png)

## Summary

The TuneFull music network bundles together fun and discovery to provide its users with a positive and friendly music sharing experience. Tune in to share 20-30 second clips of music that match your mood, and see what music clips your friends are sharing. You can also listen to clips posted by people outside your friend circle to discover new music, or follow those with similar taste.

In today's fast paced, ever-changing world people need to be able to take a break and decouple themselves from their daily stress and concerns. Whether this pause is for a single moment or an hour, TuneFull is designed to fit into everyone's day and provide them that much-needed respite from their worldy concerns. One of the main goals with TuneFull was to fill our user's down time with a positive, musically-charged, social networking experience. Music connects us to our emotions and has the ability to turn these empty moments into daily experiences. Always on hand and easy to use, TuneFull's minimalist layout will provide it's users with a relaxing music sharing experience they can enjoy with their friends. The additional ability for people to be able to share how they are feeling, and constantly discover new music can equip them to handle anything the day throws at them. TuneFull is designed to empower its users to feel, to experience, to uplift their daily lives, and fill their ears with its music.

### Server functionality 

The server hosts the database, and provides data to the client when requested. This includes data such as a list of the user's friends, a feed of clip posts by the user's friends and follows, or a feed of clip posts from non-friend users for use in the discovery feature. The server also saves and updates with client-provided input, including clip posts and friend requests/accepts.

### Client functionality

Once logged in, users are able to perform a variety of actions such as adding or deleting friends and follows. Users have access to a feed of recent clips posted by those on the network. Additionally, they can post 20 to 30 second sound bites of music which are added to their profile. Clicking on a clip allows the user to listen and discover information about the artist, song and album. Users who are not logged in can access this feature to some extent, but are not able to follow and friend other users or post their own music.

## [TuneFull Summary PDF](pdf/tunefull.pdf)

## Current implementation state

The server of TuneFull runs with OAuth 2.0 authentication on all intended endpoints. Endpoints are in use for the procurement of all necessary client-side information. The client-side app is in early stages: the navigation scheme has been chosen and authentication has been set up. Multiple successful round trips have been made between client and server. The server is currently unable to test certain endpoints, such as relationships. Certain other endpoints such as a single put and delete endpoint are not yet working.

## [Team Roster](team-roster.md)

## [Intended users and user personas](intended-users.md)

## Instructions for Building

1. Go to the [TuneFull GitHub repository](https://github.com/tunefull/tunefull)

2. Click on Clone or download

3. Make sure Clone with SSH is selected and click the clipboard icon to copy the SSH key

4. Use the IntelliJ Check out from Version Control/Git (from the welcome screen) or File/New/Project from Version Control/Git (from the workspace) command to clone

5. Once downloaded, build the project by clicking the green hammer icon or Build Project in Build Menu

6. Once finished building, click the green arrow icon or Run app from Run menu

7. Repeat Previous steps for [TuneFull Server](https://github.com/tunefull/tunefull-service)

8. Run the Server side project so that a connection with endpoints can be established, then run the Application

## Instructions for Using

## [Outlines of Technology Stacks](technology-stack.md)

## [Client-side design and implementation](client-design-implementation.md)

## [Server-side design and implementation](server-design-implementation.md)

## [Authentication scheme](authentication.md)