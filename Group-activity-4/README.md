## Group Activities

> Work in group to solve these tasks.

## Task 1

Inside the `src` directory

1. create a file `.env` and add the following content:

```text
MONGODB_URI=mongodb+srv://tivi:SqZsopHbsRtRDO24@cluster0.1x4ks.mongodb.net/groupnr?retryWrites=true&w=majority
PORT=4000
```

> In `MONGODB_URI`, replace `groupnr` to rfelect your group e.g `group1` , `group2` etc

2. Run:

```sh
npm install
npm run dev
```

## Task 2

1. In `./index.js` replace lines 26-40 with the following:

```js
app.post('/api/persons', async (request, response, next) => {
  const body = request.body;
  const password = body.password;
  const saltRounds = 10;
  const passwordHash = await bcrypt.hash(password, saltRounds);
  if (Object.keys(body).length === 0) {
    return response.status(400).json({
      error: 'content missing',
    });
  }

  const person = new Person({
    email: body.email,
    password: passwordHash,
    name: body.name,
    number: body.number,
  });

  person
    .save()
    .then((savedPerson) => savedPerson.toJSON())
    .then((savedAndFormattedPerson) => {
      response.json(savedAndFormattedPerson);
    })
    .catch((error) => next(error));
});
```

2. Test the endpoints with **POSTMAN** e.g.

```http
POST http://localhost:4000/api/persons
```

```json
{
  "email": "matti7@matti7.com",
  "password": "45RFgh##@$",
  "name": "Matti",
  "number": "09-345-234"
}
```

## Task 3

- What is Hashing?

Hashing turns your password into a short string of letters / numbers using an encryption algorithm. If a website is hacked, cyber criminals don't get access to your password. Instead, they just get access to the encrypted “hash” created by your password. 
    Salting adds random data to the hashed password.

- What is the Rainbow Table Attack and how can we protect against it?

A rainbow table attack is a password cracking method that uses a table (a “rainbow table”) to crack the password hashes in a database.
