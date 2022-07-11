[push express html tutorial](https://medium.com/@ritikkhatri/pusher-js-with-node-js-ede7b7a65ff1)

## WORK

1. Setup Pusher Account

```js
npm init -y
npm install --save express body-parser pusher dotenv
npm install --save-dev nodemon

// package.json
"scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
}

|____node_modules
|____public
|______index.html
|______client.js
|____package-lock.json
|____package.json
|____server.js

// server.js
const express = require('express');
const app = express();
app.use(bodyParser.json());
app.use(bodyParser.urlencoded({ extended: false }));
app.use(express.static('public'));
app.get('/', (request, response) => {

});
app.listen(3000, () => {
  console.log('Express intro running on localhost:3000');
});

// public/index.html
<!DOCTYPE html>
<html>
<head>
   <title>PusherJs Application</title>
</head>
<body>
<h2>Add Book </h2>
   <form id="book-form" >
   Book name: <br>
   <input type="text" id="book-name" name="bookname"     placeholder="Book Name">
<br>
<input type="submit" value="Submit">
</form>
<h1> Books <h1>
<div class="book-list" id="books-list"></div>
<script src='./client.js'></script>
</body>
</html>

npm run dev

// Add to server.js
var Pusher = require('pusher');

//create a instance of pusher using your credentials
var pusher = new Pusher({
  appId: API_ID,
  key: API_KEY,
  secret: API_SECRET,
  cluster: 'ap2',
  encrypted: true
});

// Add to index.html

```

DIDN'T GET THIS FOLDER WORKING. GOT THE ROOT FOLDER WORKING A LONG TIME AGO. THIS FOLDER HAS VIDS PUSHER_KEY
