# KrakenD Plugin Versions Validator

In this repository, you'll find the krakend plugin validator codebase.
Validator is able to run command shell and UI mode.

### Build
```go
go build -o validator ./main.go
```

### How to Run

### CLI Mode
```shell
Usage:
   validate [flags]

Flags:
  -s, --gosum string       path to the plugin go.sum file
  -g, --goversion string   golang version to be compared
  -h, --help               help for validate
  -k, --krakendv string    krakend version to be validate against
```
##### Example
```shell
./validator validate --krakendv v1.3.0 --goversion 1.15 --gosum ./go.sum
```

##### Output
If there is no difference between go plugin dependencies and krakend version,the application will return the exit code '0'.
else application will print all the differences to the stdout and return the exit code '1'

### UI Mode
```shell
Usage:
   serve [flags]

Flags:
  -h, --help       help for serve
  -p, --port int   server host port while running the ui mode (default 8080)

```
