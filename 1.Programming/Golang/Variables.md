```go
//These are the same
var i int
i = 1
---
i := 1
---
var i int = 1
//---------------------------------
//Mutiple variables 
var i,j int = 1, 2
var i,j = 1, 2
//(type can be omited if variable has initializer)
i, j := 1, 2
```
# Type conversion
```go
var i int = 255
var f float32 = float32(i)
f := float32(i)
```
# Constants
```go
const Pi = 3.14
```
# Untype constant
? 
___
# Pointers
There is no pointer arithmetic
## Initializer 
```go
var p *int
i := 1
p = &i
```
## Dereference
```go
//Changes the value of i
*p = 2 
//Prints the value of i
Print(*p) 
```
## To structs
There is no need to dereference 
```go
//Instead of using (*p).X
p = &MyStruct{1, 2}
p.X = 123

```
___
# Struct 
## Definition
```go
type MyStruct struct{
	X int
	Y int
}
```
## Initializer
```go
v := struct{
	X int
	Y int
}{1, 2}

v = MyStruct{1, 2}

v = MyStruct{X:1, Y:2}

v = MyStruct{Y:2, X:1}

v = MyStruct{}             // X = Y = 0

```
### For Array/Slice
```go
s := []struct{
	X int
	Y int
}{
	{1, 2},
	{3, 4},
	...
}
```
## Access
```go
v := MyStruct{1,2}
v.X 
```
---
# Array
Cant be resized
```go
var a [4]int
a[0] = 1
a[1] = 2
...
```

```go
a := [2]int{1, 2}
```

```go
b := [3][3]int{ {1,2,3} , {4,5,6} }
```
---
# Slice
```go
//This includes element from a[1] to a[2] (it excludes a[3])
var s []int = a[1:3]
```
Defaults
```go
a := s[:2]   // == {s[0],s[1]}
b := s[1:]   // == {s[1], ..., s[n]}
c := s[:]    // == s
```
## Behaviour
Slices are a reference to an existing array (space memory)
```go
	names := [4]string{
		"John",
		"Paul",
		"George",
		"Ringo",
	}

	a := names[0:2]
	b := names[1:3]

	// This will affect (change) names[1] and a[1]
	b[0] = "XXX"
```
## Atributes
Length and Capacity
```go
s := []int{0,1,2,3}
len(s) // == 4
cap(s) // == 4
```

```go 
// Decrease length
a := s[:2]
len(a) // == 2
cap(a) // == 4
```

```go
// Decrease size (capacity)
b := s[1:]
len(b) // == 3
cap(b) // == 3
```
Manually changing capacity:
```go
s := s[a:b:c]
/*
 * start at index a
 * end at index b  (length b-a)
 * set capacity = c-a
 */
```
**Append** creates a new allocated array
```go
// Increase size (capacity)
s = append(s, 4, 5)    // s = [0 1 2 3 4 5]
	// or
s = append(s, make([]int, 2)...) // s = [0 1 2 3 0 0]
```
**Make** function
	- Used to make a slice with dynamic size
```go
a := make([]<type>, <lenght>, <capacity>)
```
___
# Map
Just by declaring it, you can not access the map, it will always return **nil** unless you initialize it with **make**
```go
var m = map[string]int
m = make(map[string]int)
```

```go
m := make(map[string]int)
```

```go
var m = map[string]int{
	"Cero" : 0,
	"Uno" : 1,
}
```

``` go
m["Cero"] = 0
```
## Methods
Insert/Update
```go
m[<Key>] = <Element>
```
Get
```go
elem = m[<Key>]
```
Delete
```go
delete(m, <Key>)
```
Test presence
```go
elem, ok := m[<Key>]
// if <Key> exists in m  =>  ok = true
// if not  =>  ok = false & elem = default value
```
___
# Generics 
## Type parameters
Declares that MyFunction can recieve any data type that implements all the constraints
```go
func MyFunc[T <constraint>, S <constraint>](s []T, x S) int
```
### Personalized contraints
```go
type Numeric interface{
	int|int32|int64|float32|float64
}

func Do[T Numeric](a T){...}
```
## Type variables 
List that holds any type of value
```go
type List[T any] struct {
	next *List[T]
	val  T
}
```
