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

```
