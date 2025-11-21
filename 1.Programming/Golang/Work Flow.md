# Defer
The function DoAtEnd will be executed ones the function Do **right before** it returns its value 
```go
func Do(){
	defer DoAtEnd()
	...
}
```
## Multiple defers 
When stacking defers, executions behaviour is LIFO (executes from bottom to top)
```go
func Do(){
	defer DoLast()
	defer DoMiddle()
	defer DoFirst()
}
```

