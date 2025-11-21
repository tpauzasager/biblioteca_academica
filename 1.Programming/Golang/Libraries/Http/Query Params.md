# Server-side
```go
import (
	"net/http"
)

func main(){
	http.HandlerFunc("/", handler)
	port := fmt.Spintf("localhost:8080")
	err := http.ListenAndServe(port, nil)
}
//input -> http:localhost//8080?name=Carlos&age=30
func handler(w http.ResposeWriter, r *http.Request){
	query := r.URL.Query()
	name := query.Get("name")
	age := query.Get("age")
}
```

# Client-side
```go
func main(){
	baseURL := "http://localhost:8080"

	u, err := url.Parse(baseURL)

	// Adds parameters to query
	queryParams := url.Values{}
	queryParams.Add("name", "Carlos")
	queryParams.Add("age", "30")
	u.RawQuery = queryParams.Encode()

	// url := fmt.Spintf("localhost:8080?name=%v&age=%v", "Carlos", 30)

	// Send query GET
	resp, err := http.Get(u.String())
	defer resp.Body.Close()
}
```