# Go Projects

This repository contains small Go projects for learning and experimenting with
HTTP servers and APIs. Each project is a standalone Go module with its own
dependencies and README.

## Projects

| Project | Description | Documentation |
| --- | --- | --- |
| `01-web-server` | Standard-library HTTP server that serves static pages, handles a form submission, and provides a greeting endpoint. | [01-web-server/README.md](./01-web-server/README.md) |
| `02-movies-crud` | In-memory movie CRUD API using Go's `net/http` and Gorilla Mux. | [02-movies-crud/README.md](./02-movies-crud/README.md) |

## Requirements

- Go 1.27.3 or later

## Run a project

Run each module from its own directory:

```sh
cd 01-web-server
go run .
```

Or run the movies API:

```sh
cd 02-movies-crud
go run .
```

The web server listens on port `8080`; the movies API listens on port `8000`.
See the linked project READMEs for routes, examples, and project-specific
details.
