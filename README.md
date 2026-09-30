# Interviewtopia Tax API

This is the starter repository for a live pairing exercise. It contains a small Go HTTP service with a health endpoint and no tax implementation.

## Brief

The land of Interviewtopia has a very basic, non-cumulative income-tax system. If someone earns up to $10,000, they pay no income tax. If they earn between $10,000 and $20,000, they pay 10% tax. If they earn above $20,000, they pay 20% tax.

Build an HTTP API that accepts someone's income and returns the amount of tax they will pay.

Interviewtopia expects its policy to grow to as many as 1,000 tax bands. Represent the policy as data rather than writing one branch per band. Tests should exercise observable behaviour through an HTTP handler or test server; focused lower-level tests are also welcome.

Use an AI coding assistant or agent as part of your normal workflow. You remain responsible for the result. Ask the interviewer questions whenever the brief leaves a material decision open. You are not expected to implement every possible refinement; prioritise and explain your decisions.

## Getting started

Requirements:

- Go 1.23 or newer
- Make, optionally

Run the service:

```sh
go run ./cmd/server
```

The server listens on `http://127.0.0.1:8080` by default. Override it with `HTTP_ADDR`.

Check the starter:

```sh
go test ./...
go test -race ./...
go vet ./...
```

Or run all checks with:

```sh
make check
```

The starter health endpoint is:

```sh
curl -i http://127.0.0.1:8080/healthz
```

