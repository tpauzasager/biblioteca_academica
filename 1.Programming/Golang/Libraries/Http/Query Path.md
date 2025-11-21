# Server-side
```go
func main(){
	// String recieve after helloworld will be saved in variable "name"
	http.HandFunc("GET /helloworld/{name}", HelloWorld)
	http.ListenAndServe(":8080", nil)
}

func HelloWorld(w http.ResponseWriter, r *http.Request){
	name := r.PathValue("name")  // Get access to variable "name"
}
```

# Cliente-side
```go

```
