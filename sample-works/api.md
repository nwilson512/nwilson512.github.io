---
title: API
layout: api
toc: true

type: Concept, Reference

api_url: http://api.test:5656/api/v1

#parseMe
api_calls:
- data:
    - description: The root endpoint, returns connection info
      example: curl -X GET http://techwriting.io/rpsapi/v1/
      method: GET
      parameters: NONE
  endpoint: /
- data:
    - description: Returns this documentation
      example: curl -X GET http://techwriting.io/rpsapi/v1/docs
      method: GET
      parameters: NONE
  endpoint: /docs
- data:
  - description: Fetch a list of all players stored in the database.
    example: curl -X GET http://techwriting.io/rpsapi/v1/players
    method: GET
    parameters: NONE
  - description: create a new player
    example: curl -X POST -d "name=Steve" http://techwriting.io/rpsapi/v1/players
    method: POST
    parameters: name (string)
  endpoint: /players
- data:
  - description: Fetch a specific player's name
    example: curl -X GET http://techwriting.io/rpsapi/v1/players/5c5cc956608ab82cb789da6b
    method: GET
    parameters: NONE
  - description: Update a specific player's name or play a new hand. Use only one
      parameter at a time.
    example: curl -X PUT -d "played=rock" http://techwriting.io/rpsapi/v1/players/5c5cc956608ab82cb789da6b
    method: PUT
    parameters: 'name (string), played (enumerated string: rock, paper, scissors)'
  - description: Delete a specific player's name
    example: curl -X DELETE http://techwriting.io/rpsapi/v1/players/5c5cc956608ab82cb789da6b
    method: DELETE
    parameters: NONE
  endpoint: /players/PLAYERID
#parseStop
---

## The Rock Paper Scissors API

the Rock Paper Scissors API (RPSAPI) is a REST API that allows users to play rock paper scissors against a computer player. This allows users to revisit a proven and universal method of dispute resolution from their childhoods. Although, I don't recommend using this to make any important life decisions.

Within the API, you can do the following:

* Play a hand against the computer
* Add and remove players
* View a list of all players
* View a player's scores
* Update player names and delete players

## Requirements

To interact with the API and play Rock Paper Scissors, you need an http client that can send requests using the `GET`, `PUT`, `POST`, and `DELETE` methods, such as [cURL](https://curl.haxx.se). You also need an internet connection, but you do not need an account.

## Getting started

The most immediate way you can get started with rock paper scissors is to submit a request using form data. This button sends a form request to get all of the players:

<form class="getPlayers" action="http://techwriting.io/rpsapi/v1/players/" method="get">
  <input class="getPlayersButton" type="submit" name="submit" value="Get all players"/>
</form>

The next-easiest way, and the way all examples are provided, is to use cURL. The following cURL command performs the same `GET` request as the form above:

    curl -X GET http://techwriting.io/rpsapi/v1/players

Using cURL, you can manually call all of the endpoints in the Rock Paper Scissors API and play the game. See the [Reference Section](#api_reference) for all of the available endpoints and example cURL commands for each.

## How it works

The Rock Paper Scissors API is written in Javascript, and uses Express to handle requests and a Mongoose database to store player and game data.

The following diagram illustrates the general architecture of this API:

![Diagram showing API traffic flow](/assets/img/traffic.png)

* **Request** A player makes an API request
* **Reverse Proxy** The webserver routes traffic to the Express server
* **server.js** Javascript code handles the request using the Express framework and Mongoose library
* **Response** Responses are returned to the user

The following sections describe some of the more noteworthy details of how the API functions:

### Computer hand generation

The computer's hand is generated using a pseudorandom (in a generous sense of the term) algorithm based on the current time in seconds.

```
// use time for psuedorandom hand generation, take the modulus of 3 to select one of 3 hands
              var notRandom = time.getSeconds() % 3;
              <...>
```

### Documentation endpoint

Documentation for this API is written into the server.js source code and can be accessed at its own endpoint. The following code snippet shows the router get function, the endpoint string, and response JSON:

```
router.get('/v1/docs', function(req, res) {
    res.json(
      {
        api_calls: [{
          endpoint: '/',
          data: {
            method: 'GET',
            parameters: 'NONE',
            description: 'The root endpoint, returns connection info',
            example: 'curl -X GET http://techwriting.io/rpsapi/v1/'
          }
        },
        <...>
```

The reference documentation for this site is automatically retrieved from this endpoint, parsed, and written into this page's YAML frontmatter using an automation script I wrote. For more information about that, including the full code, see the [API Documentation Automation](/samples/code/api-documentation-automation) section of my sample work.

### API versioning

This API features rudimentary versioning support through manually prepended strings prepared for the router. This allows me to develop more sophisticated versioning code at a later date, while not impacting the end user experience.

```
router.get('/v1/docs' <...>
```

### Database

Database access is handled through the mongoose library. The database itself is hosted by the mlab cloud storage provider. This reduces the complexity of administration, and allows me to query the same database from both development and production versions of my API.

```
// open a connection with mongoose DB at mLab. This is not a production solution.
mongoose.connect('mongodb://XXXXXX:yyyYYYyy@zzzZZZZz.mlab.com:55555/api', { useNewUrlParser: true });
<...>
```

{{# API reference is currently parked on the template #}}

### More information

For more information, see the Rock Paper Scissors API's full code in the [Samples](/samples/code/rock-paper-scissors-api) section.

## API reference