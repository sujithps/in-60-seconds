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
