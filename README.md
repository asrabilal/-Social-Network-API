# 18 NoSQL: Social Network API


   

## Table of Contents:  
  - [Description](#description)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Contribution](#contribution)
  - [Testing](#testing)
  - [Questions](#questions)
  - [Additional Info](#additional-info)

## Description:
This is a set of API for a social network that uses a MongoDB database so that the website can handle large amounts of unstructured data, Express.js for routing, Mongoose ODM, and the moment package to format time stamps.

## Installation:
This repo is not to be deployed, if you wanted to, you could by doing the following:  
1. Download the repo files from the link below
2. You must have mongoDB installed
3. Run the following at the command line
```
    - npm init -y
    - npm install express
    - npm install mongoose
```
4. Start the server
```
    $ npm start
```
5. Open Insomnia Core to test API routes

## Usage:

- When you enter the command to invoke the application then the server is started and the Mongoose models are synced to the MongoDB database.  
- Testing API GET routes in Insomnia Core for users and thoughts return the data for each of these routes in a formatted JSON
- Testing API POST, PUT, and DELETE routes in Insomnia Core are able to successfully create, update, and delete users and thoughts

- Testing API POST and DELETE routes in Insomnia Core are able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list.

## Contribution:

All contributions are welcome.

## Testing:  

Testing restful API calls with Insomnia Core  

---
**`/api/users`**
* `GET` all users
* `POST` a new user:
    ```json
    // example data
    {
        "username": "lernantino",
        "email": "lernantino@gmail.com"
    }
    ```
---
**`/api/users/:userid`**
* `GET` a single user by its `_id` 
* `PUT` to update a user by its `_id`
* `DELETE` to remove user by its `_id`
---
**`/api/users/:userId/friends/:friendId`**
* `POST` to add a new friend to a user's friend list
* `DELETE` to remove a friend from a user's friend list
---
**`/api/thoughts`** 
* `GET` to get all thoughts
* `POST` to create a new thought
    ```json
    // example data
    {
    "thoughtText": "Here's a cool thought...",
    "username": "lernantino",
    "userId": "5edff358a0fcb779aa7b118b"
    }
    ```
---
**`/api/thoughts/:thoughtId`**
* `GET` to get a single thought by its `_id`
* `PUT` to update a thought by its `_id`
* `DELETE` to remove a thought by its `_id`
---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` to create a reaction 
    ```json
    // example data
    {
    "reactionBody":"Hell Yeah!!",
    "username":"lernantino"
    }
    ```
---
**`/api/thoughts/:thoughtId/reactions/:reactionId`**
* `DELETE` remove a reaction by the `reactionId` 

## License Details: 

 [![license](https://img.shields.io/badge/license-MIT-blue)](https://shields.io)

 ## Walkthrough Videos
[User Routes](https://drive.google.com/file/d/1WMXQbCPAECIsU78gSpFk8IejF80_jtpW/view)  
[Friend Routes](https://drive.google.com/file/d/1a2o-AOOmOIXz8dgTKsC1FvLIaNRoQJJf/view)  
[Thought Routes](https://drive.google.com/file/d/17ocul_N5VOl4O70y8XEILtf8691lvxEj/view)  
[Reaction Routes](https://drive.google.com/file/d/1gB0kILBgkD4XEpFXOeq6v5YhxP75W27d/view)  




  ## Questions
  [HERE](https://github.com/asrabilal)

   
  
  ## Additional Info:
  - Github: [asrabilal](https://github.com/asrabilal)
  - Email: asra596@gmail.com 


![](https://img.shields.io/badge/Created%20by-Asra%20Bilal%20-blue?style=for-the-badge)  
![](https://img.shields.io/badge/Database-MongoDB-yellow?style=flat-square&logo=mongoDB)  ![](https://img.shields.io/badge/npm%20package-express-orange?style=flat-square&logo=npm) ![](https://img.shields.io/badge/npm%20package-mongoose-cyan?style=flat-square&logo=npm) ![](https://img.shields.io/badge/npm%20package-dotenv-%3CCOLOR%3E?style=flat-square&logo=npm)