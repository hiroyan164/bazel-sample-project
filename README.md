This is a bazel sample project.

# requirements

- bazel
- skaffold

# How to use

- `make skaffold`
- go `http://localhost`.
- exec the following code on the site:
  ```js
  fetch("/echo", {method: "post", body: "aaa"}).then(res => res.text()).then(text => console.log(text))
  // aaa
  ```


# manual build&run
## gateway
```sh
go run gateway/main.go
```
## echo
```sh
go run echo/main.go
```
# bazel build&run
## gateway
```sh
bazel run //gateway --platforms=@io_bazel_rules_go//go/toolchain:darwin_amd64
```
## echo
```sh
bazel run //echo --platforms=@io_bazel_rules_go//go/toolchain:darwin_amd64
```
