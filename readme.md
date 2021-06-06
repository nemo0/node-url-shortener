# Node.js URL Shortener API

This is an URL shortener service like bit.ly or cutt.ly. The front-end is not covered here. The API service can take a long URL and convert it to a shorter URL. MongoDB is used as the database. The long URL, short URL, and other details are stored in the database. When a long URL that is already stored in the database is passed again, it returns the older shortened URL.

## Screenshots

![Working](https://i.ibb.co/y82hQq2/ezgif-com-video-to-gif.gif)

## Run Locally

Clone the project

```bash
  git clone https://github.com/nemo0/node-url-shortener
```

Go to the project directory

```bash
  cd urlShortenerMongo
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```

## API Reference

### Shorten URL

```http
  POST /api/short
```

| Field | Type   | Description  |
| :---- | :----- | :----------- |
| Body  | `json` | Original Url |

**Example:**

```http
POST http://localhost:3333/api/short
Content-Type: application/json

{
    "origUrl": "https://nemo.hashnode.dev/an-introduction-to-recursion-using-javascript-ckfgx2nrq001xols17h787f87"
}

```

### Get item

```http
  GET /:id
```

| Parameter | Type     | Description     |
| :-------- | :------- | :-------------- |
| `id`      | `string` | Unique URL Code |

**Example:**

```http
GET http://localhost:3333/SLiCKEXdn
```

## Environment Variables

To run this project, you will need to add the following environment variables to your `.env` file

| Variable    | Description             |
| :---------- | :---------------------- |
| `MONGO_URI` | MongoDB URI             |
| `BASE`      | Base URL for Shortening |
