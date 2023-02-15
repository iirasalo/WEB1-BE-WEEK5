## Group Activities

> Work in group to solve these tasks.

## Task 1

- Inside the `src` folder:
  - Run `npm install`
  - Run `npm run dev`
- Use POSTMAN to test the endpoints:
  - Alternatively, you can use `REST VS code extension`
  - Examples:

```http
POST http://localhost:4000/api/workouts
{
    "title":"Workout 1",
    "reps":40,
    "load":10
}
```

```http
POST http://localhost:4000/api/user/signup
{
    "email": "sami@sami.fi",
    "password": "45RFgh##@$"
}
```

```http
POST http://localhost:4000/api/user/login
{
    "email": "mirja@mirja.fi",
    "password": "45RFgh##@$"
}
```

## Task 2

- What is Hashing?
- What is the Rainbow Table Attack and how can we protect against it?

## Task 3

- Refer to the file `userModel.js` and discuss how passwords are salted before Hashing.
