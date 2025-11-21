	# Steps 
1. Target endpoint that supports `GET`&`HEAD`&`OPTIONS`
2. Find discrepancies in how the server parse URL paths 
	1. URL->resources mapping 
	2. Delimiter characters 
	3. Normalize paths 
3. Craft URL to exploit this discrepancies and make the server cache dynamic responses
	-  Ones the user enters the malicious URL, the attacker can send the same request and get the same response that the user got 
	- Do this without the browser (usually has more security in the middle) 

Cache-Buster 
- Used to add unique query strings to the request so it does not get cached 
# Delimiter characters
## Detecting path mapping discrepancies 
1. For a correct url such as: `/api/orden/123` try `/api/orden/123/foo`
2. If the response is the same =>the origin server path mapping ignores the added segment 
3. If `/api/orden/123.js` gets cached => The DNS path mapping only checks for the last extension file 
## Cache detection
- You can detect whether the response has been cached by looking at:
	- Body content:
		- X-Cache: {hit,miss,dynamic,refresh}
		- max-age:  > 0
	- Reponse time: Big diffrence => Response has been cached previuously 
	
# Static directory cache rules 
- Cache may cache path with prefix: `/static` `/assets` `/scripts` `/images` 

Decoding discrepancies
	ex: `/static/..%2fprofile` 
		Origin decode -> `/static/../profile` and respond with profile page 
		Cache decode ->  `/static/..%2fprofile` and caches it because of prefix /static
	if `/` gets sent not decoded => server may resolver the path and delete /static prefix 

## Origin server detection 
original -> `/profile`
try -> `/aaa/..%2fprofile`

if same response => Origin resolvers `..` and decodes `%2f` -> `/`
if 404 => does not
## Cache server detection 
Use history to detect common cachable path prefixes like `/assets/js/lal.js`
Send before static directory: `/aaa/..%2fassets/js/lal.js` 
	If same cached response => Cache server normalizes the path to original 
	if response not cached => Cache server does not normalize the path /

Send afeter static directory:  `assets/aaa..%2fjs/lal.js`