# FineLine API documentation

## Projects

#### Creating a project

`POST /project`
```
{
  "title": "Your project's title",
  "description": "Brief summary of the project"
}
```

Returns int corresponding to the new project's ID

#### Fetching projects

`GET /project/:id`

```
{
  "id": 1,
  "title": "Your project's title",
  "description": "Brief summary of the project"
}
```

#### Finding participants on a project

`GET /project/:id/users`
```
[
  {
    id: 47,
    email: "lance@qwe.com",
    name: "Lance Stacenko"
  },

  {
    id: 8,
    email: "raf@raf.raf",
    name: "Raf"
  },
]
```


## Users

#### Creating a user

`POST /user`
{
  "name": "Rafael Khan",
  "email": "420@blaze.it"
}

returns int corresponding to the new user's ID

#### Fetching a user

`GET /user/:id`
{
  "id": 2,
  "name": "Rafael Khan",
  "email": "420@blaze.it"
}

