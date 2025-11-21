Go does not have clases but you can add methods on types and create interfaces 
# Methods 
You can only add methos to the data type declared inside the same package 
```go
type MyInt int

func (i MyInt) GiveNext() MyInt{
	return i++;
}
```
## Pointer recievers
Used to chenge the variable called 
You should not mix value and pointer recievers methods for the same data type
```go
func (i *MyInt) Step(){
	*i += 1; 
} 

v := MyInt(0)

v.Step() // == (&v).Step()

Print(v) // Prints 1
```
___
# Interfaces 
The convinience of pointer recievers syntax suggar does not work for interfaces
There are no explicit **implement**. A type implements an interfaces by implementing its methods 
Interface is a dupla of: Value and Type 
A variable is only nill when both (value and type) are nill
```go
type MyInt interface{
	GiveNext() MyInt,
	Step()
}
```

```go
//Do the same for Step()
func (f Myfloat) GiveNext(){
	...
}

func (s *MyString) GiveNext(){
	...
}

f := MyFloat(0) 
s := *MyString("Cero")
z := MyString("Cero")

f.GiveNext()    // Works
s.GiveNext()    // Works
z.GiveNext()    // Does not Work
```
## Errors
Calling a method to a nill interface 
```go
type I interface{
	M()
}

func Do (i I){...}

func main(){
	var i
	Do(i)  // Works
	i.M()  // Doesnt Works
}
```
## Type assertion
Checks if the value of i has the type T
Assings the underlying value to t
If the value is of type T => ok == true
If not => **panic**
```go
t, ok := i.(T)
```
## Type switches
```go
switch v := i.(type) {
case T:
    // here v has type T
case S:
    // here v has type S
default:
    // no match; here v has the same type as i
}
```
