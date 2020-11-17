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

    * `number`
    
        * Any positive integer
        
        * ALL (default)

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

    * `200 OK`
    
    * `400 Bad Request` (empty request body or invalid genre)

### `GET /clips`

* Description

Returns all `Clips`, controlled by parameters.

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

###  `GET /clips/{clipId}`

* Description

Gets a selected `Clip`. Might not be needed?

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

(None)

* Query parameters

(None)

* Request body

`Clip`

* Response body

`Clip`

* Response status

    * `201 Created`
    
    * `400 Bad Request` (one or more invalid `Clip` properties--or an invalid combination of properties--in request)
    
### `GET /relationships/friendships`

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
  
### `GET relationships/follows`

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

### `GET relationships/unaccepted`

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

### `POST /relationships`

* Description

Creates a relationship between two `Users`.

* Path parameters

(None)

* Query parameters

(None)

* Request body

`Relationship`

* Response body

`Relationship`

* Response status

    * `201 Created`
    
    * `400 Bad Request` (one or more invalid properties--or an invalid combination of properties--in request)   
   
### `PUT /relationships`

* Description

Updates a relationship between two `Users` (i.e. a friend request has been accepted).

* Path parameters

(None)

* Query parameters

(None)

* Request body

`Relationship`

* Response body

`Relationship`

* Response status

    * `200 OK`
    
    * `400 Bad Request` (one or more invalid properties--or an invalid combination of properties--in request)
