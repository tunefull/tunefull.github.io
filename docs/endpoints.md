# TuneFull Endpoints

## Global

### Server context path

`/tunefull`

### Authentication

All endpoints are secured by OAuth 2.0. Any requests not including an `Authorization` header with a valid `Bearer` token will result in a `401 Unauthorized` status.

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

###  GET /users

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

### GET /users/me/clips

* Description

Returns all `Clips` associated with the current `User`.

* Path parameters

(None)

* Query parameters

    * `number` (number of clips to return)
        
        * Any positive integer (default is 20)

    * `index` (allows for getting less recent clips)
        
        * Any positive integer (default is 0)
        
    * If `number` and `index` form an invalid combination, default values are used

* Request body

(None)

* Response body

`Clip[]`

* Response status

`200 OK`

###  GET /users/clips

* Description

Gets all `Clips` for all `Users`.

* Path parameters

(None)

* Query parameters

    * `number` (number of clips to return)
        
        * Any positive integer (default is 100)
    
    * `index` (allows for getting less recent clips)
        
        * Any positive integer (default is 0)
                
    * If `number` and `index` form an invalid combination, default values are used

* Request body

(None)

* Response body

`Clip[]`

* Response status

`200 OK`

### POST /clips

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

### PUT /users/me/genre

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

### POST /user/relationship

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
    
### GET /user/friendships

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
  
### GET /user/follows

* Description

Gets the relationships in which the `User` is following the other `User`

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