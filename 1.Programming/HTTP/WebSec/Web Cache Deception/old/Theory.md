Servers usually cached some copies of web pages with public access (without personal information).
There are ways to cheat the server to make it cached sensitive information.

Cache key:
	- Used to identify if the response to the request has to be cached 
	- Depends on the URL, queryparams and other things from the request 

Steps
1. Attacker sends a URL to fool the server 
	Original page with sensitive info: `https://example.com/setting.php` 
	Attackers URL: `https://example.com/setting.php/stylsheet.css`
2. The server response the same way for both URL
3. The 2nd url gets cached, because server thinks it has only public information 
4. The attacker can access the response from the original URL via the 2nd URL (witch has all the personas information from the attacked user)

Clarifications:
- All the data that the client receives after the 1st loadout of the page is not cached. Only the fist response from the server get cached. 

vs Cache Poisoning 
	- This methos injects malicious content into the users cached response (witch is then delivered to the user)
	- Directly modyfies the cache key 

Delimiters:
- Are used to separate the url path from, for example, the queryparams 
- Examples:
	- `http://example.com/setting.php?id=1234.js`
	- Server gets `http://example.com/setting.php?
	- Cache gets the full url and may detect it as a cachable response
- Encoding
	- Some delimiters get encoded before getting sent to the origin server 
	- If the origin server decodes this delimiters, it is possible to use the encoded version of the delimiter (i.e. # -> %23)
	- Discrepancies
		- Some times the decode can vary between chace an orign server 
		- Other times, the cache first applies cache rules and then decodes and forwards the request to the origin 
		- ex: `%23` -> `#` ; gets decoded in the orgin server but not in the cache, so the server will detect it as a delimiter, but not for the cache 

 Static Directory Rule:
 - Such as: `/static` `/assets` `/scripts` `/images` 
- There prefix may be interpreted by cache and meke it cache the response
 - More info in `Path traversal academy`
 
Normalization by Cache Server
	
