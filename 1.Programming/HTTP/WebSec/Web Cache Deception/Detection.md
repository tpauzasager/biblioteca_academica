# Static Extension Cache Rule
## Delimiter Discrepancies 
When Origin and cache have different delimiters for the URLs 
Ex:
	URL -> `/profile;lal.css`
	Origin -> `/profile` 
	Cache -> `/profileL;lal.css`
	Result:
		Origin returns profile data and cache interprets it as a cachable response

Exclude this delimiters:
	{, }, < , >, # 
	They are frecuently processed by the browser before sending the request
## Delimiter Encoding Discrepancies 
When trying to send delimiters as data it is required for those delimiters to be encoded so that the server does nos interprets them as a delimiter and, instead, as data.
Some parcers decode the URL before processing it.

Ex:
	URL -> `/profile%23lal.css`
	Origin -> `/profile`
	Cache -> `/profile%23lal.css`
___
# Static Directory Cache Rule
Cache maigh cached all responses from specific directories

Ex:  `%2f === /`
	URL -> `/static/..%2fprofile`
	Resolved -> `/profile`
	Origin -> `/profile`
	Cache -> Gets cached because the path starts with `/static`
## Detection 
For -> `aaa/..%2fprofile`
If Origin return 202 => Origin resolves paths

For -> `aaa/..%2fstatic/lal`
If gets cached => Cache resolves paths
___
# File Name Cache Rules
Certain file get cached no matter what (See [[File Names]])
