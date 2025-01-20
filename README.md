# Protobuf file for SSO. Writen in go

## Begin
- Install `go utils`
```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
export PATH="$PATH:$(go env GOPATH)/bin"
```
- install `task`
- isntall `protoc`

Example (for MacOS)
```bash
brew install go-task/tap/go-task
brew isntall protoc
```
## Usage
```bash
task generate
```
## Command
```bash
protoc -I proto proto/sso/sso.proto --go_out=./gen/go --go_opt=paths=source_relative --go-grpc_out=./gen/go/ --go-grpc_opt=paths=source_relative
```
