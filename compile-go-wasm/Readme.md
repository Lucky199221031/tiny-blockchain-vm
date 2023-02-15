# Compile go into wasm


## Def
1. compile go into wasm
2. start http server for testing wasm

## Ref
https://binx.io/2022/04/22/golang-webassembly/

## Command
GOOS=js GOARCH=wasm go build -o static/main.wasm cmd/wasm/main.go
cp "$(go env GOROOT)/misc/wasm/wasm_exec.js" ./static
go run ./cmd/server/main.go