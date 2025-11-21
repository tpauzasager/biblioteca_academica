```go
var val1 int = 3  //Global variable

func main() { 
	var add = func(a int, b int) int { ... } //Declaration of a function inside another function 

	go func(id int){ ... } (i) //Nameless function that runs immediately with i value as input
}

func add(a int, b int) int  //return int value 
	{ ... }

func add(...) (int, error) //Returns int and error values 
```

# Syntax
```go
//** This functions are the same
func Do(x int, y int) (string, string){
	return "Hello", "World";
}

func Do(x, y int) (a,b string){
	a := "Hello"
	b := "World"
	return; 
}

func main(){
	a,b := Do(1,2);
}
```
# As a Value
```go
func Execute(fn Do(int, int) string) string{
	return fn(3,4)
}
```
# Closure
A function thar returns another function
```go 
func adder() func(int) int {
	sum := 0
	return func(x int) int {
		sum += x
		return sum
	}
}

func main() {
	pos, neg := adder(), adder()
	for i := 0; i < 10; i++ {
		fmt.Println(
			pos(i),
			neg(-2*i),
		)
	}
}
```
