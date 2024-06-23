# This a repo compiling useful commands and snippets for everyday development process with terminal

## Tests

Running tests files in specific directory:

```bash
go test ./tests/
```

Running tests with verbose option, this is useful while debugging code.

```bash
go test -v ./tests/
```

## Formatting code

### Previewing affected files by formatting

```bash
gofmt -s -d .
```

### Formatting al code in directory

```bash
gofmt -w -s .
```

### Formatting go code in specific directories

```bash
gofmt -w -s ./pkg ./cmd
```

### Removing packages installed with `go get`

```bash
go clean -i importpath...
```

*This command deletes the archive files and executable binaries but the source directory we have to remove manually under `$GOPATH/src.`*

## Useful commands for golang projects

### Working with multi module project

You can create a multi module project referencing dependencies, and indicating go compiler where to find types and packages.

In your main directory run `go work init`

```bash
go work init
```

_This will create a `go.work` file._

Create a module under its own directory

```bash
gomod init myAModule
```

Import reference from `myAModule` to `myBModule`

```bash
gomod use ./myAModule
```
