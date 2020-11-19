![TuneFull](img/tunefull-logo.png)

## Summary

The TuneFull music network bundles together fun and discovery to provide its users with a positive and friendly music sharing experience. Tune in to share 20-30 second clips of music that match your mood, and see what music clips your friends are sharing. You can also listen to clips posted by people outside your friend circle to discover new music, or follow those with similar taste.

### Server functionality 

The server hosts the database, and provides data to the client when requested. This includes data such as a list of the user's friends, a feed of clip posts by the user's friends and follows, or a feed of clip posts from non-friend users for use in the discovery feature. The server also saves and updates with client-provided input, including clip posts and friend requests/accepts.

### Client functionality

Once logged in, users are able to perform a variety of actions such as adding or deleting friends and follows. Users have access to a feed of recent clips posted by those on the network. Additionally, they can post 20 to 30 second sound bites of music which are added to their profile. Clicking on a clip allows the user to listen and discover information about the artist, song and album. Users who are not logged in can access this feature to some extent, but are not able to follow and friend other users or post their own music.

## Current implementation state

The server of TuneFull runs with OAuth 2.0 authentication on all intended endpoints. It has endpoints to get all the information that is anticipated to be needed on the client-side. The client-side app is in early stages: the navigation scheme has been chosen and authentication has been set up. Multiple successful round trips have been made between client and server. The server is currently unable to test certain endpoints, such as relationships.

## [Team Roster](team-roster.md)

## [Intended users and user personas](intended-users.md)

## [Server-side design and implementation](server-design-implementation.md)

## [Client-side design and implementation](client-design-implementation.md)

## [Authentication scheme](authentication.md)