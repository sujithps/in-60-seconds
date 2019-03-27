<span class="menu-title" style="display: none">Intro</span>
## `Golang`
# `Basics`


---
<span class="menu-title" style="display: none">Hello World</span>

### `Hello World!`

<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Sample Code Block</span>

```go
package main

import (
    "fmt"
)


func main() {
    fmt.Println("hello world!!")
}

```

<div class="south span-100 text-06">

</div>

---

### `Exported Names`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">exported and unexported names</span>

```go
package main

import (
  "fmt"
  "math"
)

func main() {
  fmt.Println(math.Pi)
}
```


<div class="south span-100 text-06">

</div>


---

### `Variables`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">declarations, zero values</span>

```go
package main

import "fmt"

var active bool

func main() {
	var i int
	fmt.Println(i, active)
}

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/basics/9">Try Live</a>
</div>


---

### `Types`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">bool, string, byte, rune, float*, int*, complex*, uint*</span>

```go
 bool
 
 string
 
 int  int8  int16  int32  int64
 uint uint8 uint16 uint32 uint64 uintptr
 
 byte // alias for uint8
 
 rune // alias for int32
      // represents a Unicode code point
 
 float32 float64
 
 complex64 complex128

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/basics/12">Try Live</a>
</div>


---

### `Type conversions`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Explicit conversion is mandatory</span>

```go
i := 42
f := float64(i)
u := uint(f)

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/basics/13">Try Live</a>
</div>


---

### `Functions`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Multi params with same type, multiple results, named return type</span>

```go
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func main() {
	fmt.Println(add(1, 2))
}
```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/basics/5">Try Live</a>
</div>

---

### `Constants`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Numeric constants</span>

```go
package main

import "fmt"

const Pi = 3.14

func main() {
	fmt.Println("Happy", Pi, "Day")
}


```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/uMByhzgpRqx">IOTA -1- Try Live</a><br>
<a href="https://play.golang.org/p/RxIbwsErSrS">IOTA -2- Try Live</a>
</div>


---

### `Loop`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">One for for every need</span>

```go
package main

import "fmt"

func main() {
	sum := 0
	for i := 0; i < 10; i++ {
		sum += i
	}
	fmt.Println(sum)
}

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/flowcontrol/3">Try Live</a><br>

</div>


---

### `Conditions`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> if , shorthand, if else, switch , no break</span>

```go
package main

import (
	"fmt"
)

func evenOrOdd(x int) string {
	if x % 2 == 0 {
		return "even"
	}
	return fmt.Sprint("odd")
}

func main() {
	fmt.Println(evenOrOdd(2), evenOrOdd(3))
}


```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/flowcontrol/6">If- Try Live</a><br>
<a href="https://tour.golang.org/flowcontrol/9">Switch- Try Live</a><br>

</div>


---

### `Arrays`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> arrays</span>

```go
package main

import "fmt"

func main() {
	var a [2]string
	a[0] = "Hello"
	a[1] = "World"
	
	fmt.Println(a[0], a[1])
	fmt.Println(a)

	primes := [6]int{2, 3, 5, 7, 11, 13}
	fmt.Println(primes)
}



```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/moretypes/6">Try Live</a><br>

</div>

---

### `Slices`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> slices and internals</span>

```go
package main

import "fmt"

func main() {
	primes := [6]int{2, 3, 5, 7, 11, 13}

	var s []int = primes[1:4]
	fmt.Println(s)
}


```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/moretypes/7">Try Live</a><br>

</div>

---


### `Pointers`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> Pointers , Pass by reference </span>

```go
i := 42
p = &i
fmt.Println(*p)
*p = 21 

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/moretypes/1">Try Live</a><br>

</div>


---


### `Defer`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> Defer an action</span>

```go
package main

import "fmt"

func main() {
	defer fmt.Println("world")
	defer fmt.Println("maha")


	fmt.Println("hello")
}

```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/flowcontrol/13">Try Live</a><br>

</div>


---

### `Struct`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> Custom type</span>

```go
package main

import "fmt"

type Vertex struct {
	X int
	Y int
}

func main() {
	fmt.Println(Vertex{1, 2})
}


```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/moretypes/4">Try Live</a><br>

</div>



---

### `Methods`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> Custom type</span>

```go
package main

import (
	"fmt"
)

type Book struct {
	pageNo int
}

func (b Book) Read() int {
	return b.pageNo+1
}

func main() {
	b := Book{3}
	fmt.Println(b.Read())
}



```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/methods/3">Try Live</a><br>

</div>

---

### `Map`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none"> Custom type</span>

```go
package main

import "fmt"

type age int

var ageMap map[string]age

func main() {
	ageMap = make(map[string]age)
	ageMap["varun"] = 28
	
	fmt.Println(ageMap["varun"])
	fmt.Println(ageMap["maha"])
}


```

<div class="south span-100 text-06">
<a href="https://tour.golang.org/moretypes/19">Try Live</a><br>

</div>


---

### `Interface`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Auto satisfy </span>

```go
package main

import (
	"fmt"
)

type Reader interface {
	Read() int
}

type Book struct {
	pageNo int
}

func (b *Book) Read() int {
	return b.pageNo + 1
}

func main() {
	var r Reader
	
	b := Book{3}

	r = &b

	fmt.Println(r.Read())
}


```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/GuiRwWcCOSH">Try Live</a><br>
<a href="https://play.golang.org/p/yNmoBYpwABh">interface{}- Try Live</a><br>

</div>

---

### `Object composition`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Inheritance in golang </span>

```go

type Animal struct {
	name string
}

type Dog struct {
	Animal
	// …
}

```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/9iIc6vsJdBB">Try Live</a><br>
</div>

---


### `Goroutine`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Goroutine </span>

```go

package main

import (
	"fmt"
	"time"
)

func say(s string) {
	fmt.Println(s)
}

func main() {
   go say("world")
   
   time.Sleep(100 * time.Millisecond)
}


```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/iabDhZcYTk5">Simple- Try Live</a><br>

</div>


---

### `Channel`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Buffered, Unbuffered </span>

```go

ch <- x // a send statement

x = <-ch  // a receive expression in an assignment statement

<- ch    // a receive statement; result is discarded


ch = make(chan int)    // unbuffered channel
ch = make(chan int, 0) // unbuffered channel
ch = make(chan int, 3) // buffered channel with capacity 3

```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/mpTHwwiIFka">Try Live</a><br>
<a href="https://play.golang.org/p/TK1qhgMDNVp">Select - Try Live</a><br>

</div>


---

### `Panic`


<i class="fa fa-arrow-down" aria-hidden="true"> </i>

+++
<!-- .slide: data-background="#272c34" -->

<span class="menu-title" style="display: none">Panic when required </span>

```go

package main


func main() {

    panic("a problem")

    /*
    _, err := os.Create("/tmp/file")
    if err != nil {
        panic(err)
    } */
}


```

<div class="south span-100 text-06">
<a href="https://play.golang.org/p/xdIsshCZ951">Try Live</a><br>

</div>


---

<span class="menu-title" style="display: none">Finally</span>
## `Thank you`
