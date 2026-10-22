# Web Server

A small HTTP server built with Go's standard library. It serves static pages
and demonstrates handling a form submission and a simple GET endpoint.

## Requirements

- Go 1.27.3 or later

## Run

From this directory:

```sh
go run .
```

The server listens on `http://localhost:8080`. Keep the working directory at
the project root so the server can find the `static/` directory.

## Routes

| Method | Path | Behavior |
| --- | --- | --- |
| `GET` | `/` | Serves files from `static/`, including `index.html` and `form.html`. |
| `POST` | `/form` | Parses form values and responds with the submitted `name` and `address`. |
| `GET` | `/hello` | Responds with `Hello!`. |

Open [http://localhost:8080](http://localhost:8080) for the index page, or
[http://localhost:8080/form.html](http://localhost:8080/form.html) to submit
the example form.

To try the greeting endpoint:

```sh
curl http://localhost:8080/hello
```
