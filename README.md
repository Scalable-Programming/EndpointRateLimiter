# Run guide

-   `cd into project`
-   `npm install`
-   `docker-compose up -d`
-   `cp .env.template .env`
-   `set .env variables`
-   `npm run start`

### POST /register

|        Name | Required |  Type  | Description                          |
| ----------: | :------: | :----: | ------------------------------------ |
|  `username` | required | string | Username used to login               |
|  `password` | required | string | Password used for successfull login  |
| `rateLimit` | required | number | Rate limit used to validate requests |

**Response**

```
    {
        token: "stringified-jwt-token"
    }
```

### POST /login

**Parameters**

|       Name | Required |  Type  | Description                         |
| ---------: | :------: | :----: | ----------------------------------- |
| `username` | required | string | Username used to login              |
| `password` | required | string | Password used for successfull login |

**Response**

```
    {
        token: "stringified-jwt-token"
    }
```

### GET /rate-limit

**Headers**

|            Name | Required |  Type  | Description                            |
| --------------: | :------: | :----: | -------------------------------------- |
| `Authorization` | required | string | Bearer token used to authenticate user |

**Response**

```
    {
        success: boolean
    }
```
