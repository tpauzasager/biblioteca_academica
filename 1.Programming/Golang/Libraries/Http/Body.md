# Server-side
```go
import (
	"net/http"
)

func main(){
	http.HandlerFunc("POST /", handler)
	port := fmt.Spintf("localhost:8080")
	err := http.ListenAndServe(port, nil)
}

func handler(w http.ResposeWriter, r *http.Request){
	body, err := io.ReadAll(r.Body)	

	defer r.Body.Close()

	var data Data
	err = json.Unmarshal(body, &data)
}
```

# Clien-side
```go
	url := "http://localhost:8080/"

	data = Data{
		name: "Pablo"	
		age: "32"
	}

	encodeData, err := json.MarshalIndent(data, "", "  ")

	response, err := http.Post(url, "appication/json", bytes.NewBuffer(encodeData))
```