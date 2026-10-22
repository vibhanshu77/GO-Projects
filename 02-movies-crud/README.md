# Movies CRUD API

A small in-memory REST API for creating, reading, updating, and deleting movie
records. It uses Go's `net/http` package and the Gorilla Mux router.

## Requirements

- Go 1.27.3 or later

## Run

From this directory:

```sh
go run .
```

The API listens on `http://localhost:8000`. Movie data is stored in memory, so
changes are lost when the server stops. Two sample movies are loaded each time
the server starts.

## Endpoints

| Method | Path | Behavior |
| --- | --- | --- |
| `GET` | `/movies` | Returns all movies as JSON. |
| `GET` | `/movies/{id}` | Returns the movie with the specified ID. |
| `POST` | `/movies` | Adds a movie from a JSON request body. |
| `PUT` | `/movies/{id}` | Replaces the movie with the specified ID using a JSON request body. |
| `DELETE` | `/movies/{id}` | Deletes the movie with the specified ID. |

Each movie has an `id`, `isbn`, `title`, and `director` (with `firstname` and
`lastname`). For example:

```json
{
  "id": "3",
  "isbn": "4234234",
  "title": "Movie Three",
  "director": {
    "firstname": "Alfred",
    "lastname": "Hitchcock"
  }
}
```

Use the included [`movies.http`](./movies.http) file as a starting point for
requests in an HTTP client that supports that format.

## Example

```sh
curl http://localhost:8000/movies
```
