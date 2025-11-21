# Process
1. User makes request 
2. Cache checks if the same response is stored
	1. Yes -> Cache hit => Response is what is stored in the cache (with the same key)
	2. No -> Cache miss => Request gets forwarded to the server 

# Cache Keys
- Used to decide if the response is already cached 
- Based on elements of the http response (header, URL path, query parameters, etc)

# Cache Rules
## URL 

| Type                 | Example                    |
| -------------------- | -------------------------- |
| File extension       | `.css` & `.js`             |
| Static directory<br> | `/static`& `/assets`       |
| File names           | `robots.txt`&`favicon.ico` |
