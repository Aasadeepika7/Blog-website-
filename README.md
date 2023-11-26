<title>Your Blog - Post</title>
body {
font-family: Arial, sans-serif;
margin: 20px;
}

h1 {
color: #333;
}

const express = require('express');
const app = express();
const port = 3000;

// Set up MongoDB connection here

app.use(express.static('public'));
app.set('views', './views');
app.set('view engine', 'html');

app.get('/', (req, res) => {
// Fetch and render list of posts
res.render('index');
});

app.get('/post/:id', (req, res) => {
const postId = req.params.id;
// Fetch and render the selected post
res.render('post');
});

app.listen(port, () => {
console.log(Server is running at http://localhost:${port});
});

{
"name": "your-blog",
"version": "1.0.0",
"main": "app.js",
"dependencies": {
"express": "^4.17.1",
// Add other dependencies as needed
},
"scripts": {
"start": "node app.js"
}
}
