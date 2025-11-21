```go
//lib.go
package lib

type BodyRequest struct {
	Name string `json:"name"`
}

type BodyResponse struct {
	Mensaje string `json:"message"`
}

######### OTHER FILE (in same folder)###########

var request lib.BodyRequest
```