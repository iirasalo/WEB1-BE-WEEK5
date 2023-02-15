## Group Activities

> Work in group to solve these tasks.

## Task 1

- Inside the `src` folder:
  - Run `npm install`
  - Run `npm run dev`
  - Visit this address `http://localhost:4000/api/workouts/`
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

- What is MVC?
- Does the code in the `src` folder follow the MVC pattern?
