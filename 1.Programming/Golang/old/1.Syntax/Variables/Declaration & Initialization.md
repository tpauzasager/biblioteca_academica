# Simple 
```go
//Declaration
var variable int = 123
var variable = 123
variable := 123

var1, var2 := getVariables()
var1, _ := getVariables() //2nd returned var is not used 
```

# Collection
```go
// Map
var name = make(map[int]string){"Tomas":20} //Declaration and initialization
var name map[int]string //Only declaration  
	
	mapa["Juan"] //return 28 (if doesn't exist => return default value)
	mapa["Tomás"] = 32 //adds dupla 
	delete(mapa, "Juan") //deteles dupla


// Array
var name [5]int = [5]int{1,2,3,4,5}

// Slice
var name []int = []int{0,1,2,3,4,...}

	len(slice) //size
	append(slice, 6) //adds element at end
	slice[:2] //fisrt 2 elements from slice
	append(slice[:2], slice[3:]) //slice without element 2
```

# Struct
```go
type StructName struct {
	name string  //private attribute
	age int //public attribute
}

var instance StructName{name: "Tomas", age: 20}
intance //returns {Tomas 10}
intance.name //returns Tomas
instance.age = 21 //Sets age at 21
```

# Cast 
```go
var fValue float
var iValue int = int(fValue)  // fValue cast as an integer 
```