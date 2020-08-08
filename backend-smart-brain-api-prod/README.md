# SmartBrain-api - v2
Final project for Udemy course

1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. You must add your own API key in the `controllers/image.js` file to connect to Clarifai API.

You can grab Clarifai API key [here](https://www.clarifai.com/)

** Make sure you use postgreSQL instead of mySQL for this code base.

1. Run Redis locally:

```bash
$ cd
$ cd redis-6.0.6
$ src/redis-server
```

2. Run redis CLI

```bash
$ cd
$ cd redis-6.0.6
$ src/redis-cli
```

3. Add redis on heroku

```bash
$ heroku addons:create heroku-redis:hobby-dev
```

4. Using Redis from Node.js

```js
const redis = require('redis');
const client = redis.createClient(process.env.REDISCLOUD_URL, {no_ready_check: true});
```

- local redis
```js
const redis = require('redis');
const redisClient = redis.createClient());
```

- docker redis
```js
const redis = require('redis');
const redisClient = redis.createClient(process.env.REDIS_URI);
```