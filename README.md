# Exercise Article REST API Using Sanctum API in Laravel 11
REST API for article using Sanctum API. For now, this project is still in development stage. The implementation results can be seen in the below.


## Features

- CRUD Article


## Screenshots

![App Screenshot](./Documentation/Get%20Articles.png)
![App Screenshot](./Documentation/Post%20Article.png)


## Run Locally

Clone the project

```bash
  git clone https://github.com/brianajiks123/Exercise-Article-API.git
```

Go to the project directory

```bash
  cd Exercise-Article-API
```

Install Dependencies (Laravel)

```bash
  composer install
```

Migrate Database (make sure already setup your environment in the .env file)

```bash
  php artisan migrate
```

Running Development

```bash
  php artisan serve
```


## Testing Using API Client (Such as Postman)

### Routes
- GET http://localhost:8000/api/v1/articles
- POST http://localhost:8000/api/v1/store-article
- GET http://localhost:8000/api/v1/article/{id}
- PUT http://localhost:8000/api/v1/update-article/{id}
- DELETE http://localhost:8000/api/v1/delete-article/{id}


## API Reference

Headers:
- accept: application/json

### Get All Articles

```http
  GET /api/v1/articles
```

### Add Article

```http
  POST /api/v1/store-article
```

| Body                 | Type     | Description                       |
| :------------------- | :------- | :-------------------------------- |
| `title`              | `string` | **Required**                      |
| `content`            | `text`   | **Required**                      |
| `publish_date`       | `date`   | **Required**                      |

### Get Specific Article

```http
  GET /api/v1/article/{id}
```

| Params    | Type      | Description                          |
| :-------- | :-------  | :---------------------------------   |
| `id`      | `integer` | **Required**. Id of article to fetch |

### Update Article

```http
  PUT /api/v1/update-article/{id}
```

| Params    | Type      | Description                          |
| :-------- | :-------  | :---------------------------------   |
| `id`      | `integer` | **Required**. Id of article to fetch |

| Body      | Type      | Description                          |
| :-------- | :-------  | :---------------------------------   |
| `_method` | `PUT`     | **Required**. PUT method             |

### Delete Article

```http
  DELETE /api/v1/delete-article/{id}
```

| Params    | Type      | Description                          |
| :-------- | :-------  | :---------------------------------   |
| `id`      | `integer` | **Required**. Id of article to fetch |

| Body      | Type      | Description                          |
| :-------- | :-------  | :---------------------------------   |
| `_method` | `DELETE`  | **Required**. DELETE method          |


## Tech Stack

**Server:** Laravel 11, Sanctum API, MySQL, Git, Apache Web Server, Postman, VS Code, Windows 11


## Acknowledgements

 - [Laravel](https://laravel.com/docs/11.x)


## Authors

- [@brianajiks123](https://www.github.com/brianajiks123)
