# beam-go

These are recommended - note: instead of installing the example into $GOPATH$, I downloaded a copy of the wordcount.go file - replace the second line of the following 3 commands.


```PowerShell
go get -u github.com/apache/beam/sdks/v2/go/pkg/beam

go install github.com/apache/beam/sdks/v2/go/examples/wordcount@latest

wordcount --input sample.txt --output counts
```

After carefully reading errors, add a missing package and go build a local executable file (rather than install):

```PowerShell
go get github.com/apache/beam/sdks/v2/go/pkg/beam/io/filesystem/gcs@v2.37.0

go build hello.go
go build wordcount.go
.\hello.go
.\wordcount --input sample.txt --output out1
Get-Content out1
```

## Main Errors in VS Code

In general, our GitHub repo would host a Go module.

Go modules typically have one or more Go packages that are then released together. 

A package is a folder that has one or more files. 

To fix "main" issues identified by VS Code, note that all our files are in the root package/folder, and we have two func main() in our main package.  When we install it, what would run?

To fix: move your hello.go to a new GitHub repo/module. 
