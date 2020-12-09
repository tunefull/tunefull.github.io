# TuneFull Endpoints

## Global

### Server context path

`/tunefull`

### Authentication

All endpoints are secured by OAuth 2.0, except for one that allows non-logged-in users to use the Discovery feature. Aside from this, any requests not including an `Authorization` header with a valid `Bearer` token will result in a `401 Unauthorized` status.

### Content Types

Except where noted, all endpoints produce and/or consume `application/json`. A property-specific `PUT` endpoint produces and consumes `text/plain`.

## Endpoints

### `GET /users/me`

* Description

Returns the current `User` (profile)

* Path parameters

(None)

* Query parameters

(None)

* Request body

(None)

* Response body

`User`

* Response status

`200 OK`

### `GET /users/{userId}`

* Description

Returns the profile of a selected `User`

* Path parameters

`userId` (user identifier)

* Query parameters

(None)

* Request body

(None)

* Response body

`User`

* Response status

   * `200 OK`

   * `404 Not Found`

###  `GET /users`

* Description

Returns all `User` profiles

* Path parameters

(None)

* Query parameters

    * `limit` (number of users to return)
            
        * Any positive integer (default is 10)
    
    * `offset` (allows for getting more users)
            
        * Any positive integer (default is 0)
            
    * If `limit` and `offset` form an invalid combination, default values are used

* Request body

(None)

* Response body

`User[]`

* Response status

`200 OK`

### `PUT /users/me/genre`

* Description

Replaces the favorite genre of the current `User`.

* Path parameters

(None)

* Query parameters

(None)

* Request body

`Genre` enum (`Content-type: text/plain`)

* Response body

`Genre` enum (`Content-type: text/plain`)

* Response status

    * `200 OK`
    
    * `400 Bad Request` (empty request body or invalid genre)

### `DELETE /users/me`

* Description

Deletes the current user's records.

* Path parameters

(None)

* Query parameters

(None)

* Request body

`User`

* Response body

(None)

* Response status

    * `204 No Content`
    
    * `400 Bad Request` (empty request body or invalid User)

### `GET /clips`

* Description

Returns lists of `Clips`, controlled by parameters.

* Path parameters

(None)

* Query parameters 

    * `limit` (number of clips to return)
        
        * Any positive integer (default is 10)

    * `offset` (allows for getting less recent clips)
        
        * Any positive integer (default is 0)
        
    * If `limit` and `offset` form an invalid combination, default values are used
    
    * `source` 
    
        * Enum: `me`, `friends`, `following`, `all`

* Request body

(None)

* Response body

`Clip[]`

* Response status

`200 OK`

### `GET /clips/discovery`

* Description

Returns a list of `Clips` for use in the Discovery mode.

* Path parameters

(None)

* Query parameters 

    * `limit` (number of clips to return)
        
        * Any positive integer (default is 10)

    * `offset` (allows for getting less recent clips)
        
        * Any positive integer (default is 0)
        
    * If `limit` and `offset` form an invalid combination, default values are used
    
* Request body

(None)

* Response body

`Clip[]`

* Response status

`200 OK`

###  `GET /clips/{clipId}`

* Description

Gets a selected `Clip`.

* Path parameters

`clipId` (clip identifier)

* Query parameters

(None)

* Request body

(None)

* Response body

`Clip`

* Response status

   * `200 OK`

   * `404 Not Found`

### `POST /clips`

* Description

Creates a new clip

* Path parameters

`clipId` (clip identifier)

* Query parameters

(None)

* Request body

`Clip`

* Response body

`Clip`

* Response status

    * `201 Created`
    
    * `400 Bad Request` (one or more invalid `Clip` properties--or an invalid combination of properties--in request)

### `DELETE /clips`

* Description

Deletes a clip posted by the current user

* Path parameters

(None)

* Query parameters

(None)

* Request body

`Clip`

* Response body

(None)

* Response status

    * `204 No Content`
         
### `GET /friendships`

* Description

Gets the relationships in which the `User` is a friend

* Path parameters

(None)

* Query parameters

(None)

* Request body

(None)

* Response body

`Relationship[]`

* Response status

`200 OK`
  
### `GET /follows`

* Description

Gets the relationships in which the `User` is following another `User`

* Path parameters

(None)

* Query parameters

(None)

* Request body

(None)

* Response body

`Relationship[]`

* Response status

`200 OK`

### `GET /pending`

* Description

Gets the relationships in which the `User` has received a friend request and hasn't responded yet

* Path parameters

(None)

* Query parameters

(None)

* Request body

(None)

* Response body

`Relationship[]`

* Response status

`200 OK`

### `POST /friendships`

* Description

Creates a relationship between two `Users` with a friend request.

* Path parameters

(None)

* Query parameters

(None)

* Request body

`User`

* Response body

`Relationship`

* Response status

    * `201 Created`
    
    * `404 Not Found` (The other user does not exist)   

### `POST /follows`

* Description

Allows a `User` to follow a different `User`.

* Path parameters

(None)

* Query parameters

(None)

* Request body

`User`

* Response body

`Relationship`

* Response status

    * `201 Created`
    
    * `404 Not Found` (The other user does not exist)   
   
### `PUT /friendships/{relationshipId}`

* Description

Updates a relationship between two `Users` (i.e. a friend request has been accepted).

* Path parameters

`relationshipId` (relationship identifier)

* Query parameters

(None)

* Request body

boolean

* Response body

`Relationship`

* Response status

    * `200 OK`
    
    * `404 Not Found` (The relationship does not exist)

> [Return to previous page](server-design-implementation.md#server-side-design-and-implementation)