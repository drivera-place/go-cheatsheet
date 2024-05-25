# Useful commands for golang projects

## Running tests

```bash
go test ./tests/
```

## Formating code

### Previewing affected files by formatting

```bash
gofmt -s -d .
```

### Formating al code in directory

```bash
gofmt -w -s .
```

### Formating go code in specific directories

```bash
gofmt -w -s ./pkg ./cmd
```
