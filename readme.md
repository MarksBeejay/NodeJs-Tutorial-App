const express = require('express');
const app = express();

app.get('/users/:name/:age/:sex', (req, res) => {
const { name, age, sex } = req.params;
const user = { name, age, sex };
req.user = user;
res.json(user);
});

app.listen(3000, () => {
console.log('Server listening on port 3000');
});
