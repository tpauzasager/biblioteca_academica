# Goroutine
```go
go Myfunc(a,b,c)
```

The evaluation of a,b and c happens in the current goroutine, but the execution happens in the new one 
___
# Channels
## Creation
```go
ch := make(chan int)
```
## Send
```go
ch <- v   // Sends v to the channel ch
```
## Recieve
```go
v := <-ch // Recieves from ch and assings the value to v
```
## Buffer
- Send -> only blocks when buffer is full
- Recieve -> only blocks when buffer is empty
```go
ch := make(chan int, 100) //now ch can hold 100 values at the same time
```
## Close
Indicates that no more values to recieve and the channel gets closed
Sending on a closed channel will cause **panic**
```go
c := make(chan int, 10)
...
close(c)
```

```go
v, ok := <- ch
// if ch is closed => ok == flase
```
## Range
Allows you to range from multiple values recieved from the channel
```go
// This will automaticaly finish ones the channel gets closed
for i := range c{ 
	... 
}
```
## Select
Waits for multiple comunications at the same time
When more that one get recieve at the same time => Randomly selects one
**Default** is used when trying a recieve without blocking 
```go
select{
case c <- x:
	...
case <- quit:
	return
default: 
	... 
}
```
## Mutex
```go
import "sync"

var shared_resource int

func AsyncFunction() {
	sync.Lock()
	shared_resource++
	sync.Unlock()
}
```
