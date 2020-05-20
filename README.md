# :rocket: Challenge #2 Node.js concepts

This repository its part of my web studies with Rocketseat bootcamp (GoStack).





## :pushpin: The task ##
It was provide a simple API template with some non functional routes to index repositories.
In this challenge, using __Node.js__ and __express__, I have to implement all the features of the routes making the API
capable create, index and like repositories for example.






## :mag: Implementation details ##

- The API isn't using any persistent data storage (just a simple array by now)
- Each repository are describle like a JSON the follow
formate:
```javascript
{ 
  id: "uuid", 
  title: 'Desafio Node.js', 
  url: 'http://github.com/...',
  techs: ["Node.js", "..."],
  likes: 0 
}
```







## :wrench: Instalation ##
**You need to install [Node.js](https://nodejs.org/en/download/) 
and [Yarn](https://yarnpkg.com/) first, then in order to clone the project via HTTPS, run this command:**

```git clone https://github.com/gustavo-candido/Desafio-02-Conceitos-do-Node.js.git```

**Install dependencies:**

```yarn install```


## :arrow_forward: Running ##

Just type `yarn dev` or `yarn nodemon`.


## :baby_bottle: Get started ##
In order to test the project in your own machine I recommend you to download 
[Insomnia](https://insomnia.rest/download/) or [Postman](https://www.postman.com/downloads/) to run routes that require
other `HTTP` methods besides [![GET](https://img.shields.io/badge/-GET-purple?style=flat-square)]().

#### Create repository ####
[![POST](https://img.shields.io/badge/-POST-green?style=flat-square)]() http://localhost:3333/repositories

Body:
```javascript
{
  "id": "uuid",
  "title": "Node.js",
  "url": "https://github.com/gustavo-candido/Desafio-02-Conceitos-do-Node.js",
  "techs": ["Node.js", "Express"]
}
```


#### List repositories ####
[![GET](https://img.shields.io/badge/-GET-purple?style=flat-square)]() http://localhost:3333/repositories

Output:
```javascript
[
  {
    "id": "dd495cde-cb10-4e30-9591-a4b05326e064",
    "title": "Node.js",
    "url": "https://github.com/gustavo-candido/Desafio-02-Conceitos-do-Node.js",
    "techs": [
      "Node.js",
      "Express"
    ],
    "likes": 0
  }
]
```
<p align="right" >
 <em> Obs: The id its unique to all repositories, remember update </em>
</p>


#### Update repository ####
[![PUT](https://img.shields.io/badge/-PUT-orange?style=flat-square)]() http://localhost:3333/repositories/:id

Body:
```javascript
{
  "techs": ["Node.js", "React Native"]
}
```
<p align="right" >
 <em> Obs: change ':id' for your repository id  </em>
</p>


#### Delete repository ####
[![DELETE](https://img.shields.io/badge/-DELETE-red?style=flat-square)]() http://localhost:3333/repositories/:id

#### Like repository ####
[![POST](https://img.shields.io/badge/-POST-green?style=flat-square)]() http://localhost:3333/repositories/:id/like
