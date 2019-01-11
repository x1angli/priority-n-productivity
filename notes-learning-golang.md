This article contains random, unorganized notes about Golang

### Slices are like references to arrays
Unlike Python, where slices are clones of the original arrays, Golang's slices are array references Changing the elements of a slice modifies the corresponding elements of its underlying array.

```
package main
import "fmt"

func main() {
	names := [4]string{
		"John",
		"Paul",
		"George",
		"Ringo",
	}

	a := names[0:2]
	b := names[1:3]

	b[0] = "XXX"
	fmt.Println(a, b)
}
```

### Structure references
It's tricky. The special prefix & returns a pointer to the struct value. But, To access the field X of a struct when we have the struct pointer p we could write (*p).X. However, that notation is cumbersome, so the language permits us instead to write just p.X, without the explicit dereference.

```
package main
import "fmt"

type Vertex struct {
	X, Y int
}

var (
	v = Vertex{1, 2}
	p1 = &v
	p2  = &Vertex{1, 2} // has type *Vertex
)

func main() {
	fmt.Println(v)
  p1.X = 1e9  // note here
	fmt.Println(p1)
  fmt.Println(p2)
}
```

### Stacking defers
Deferred function calls are pushed onto a stack. When a function returns, its deferred calls are executed in last-in-first-out(LIFO) order.

### Switch
* Switch cases evaluate cases from top to bottom, stopping when a case succeeds.
* Equivalently, Go's switch cases need not be constants, and the values involved need not be integers.
* Golang does NOT need to "break" cases. In effect, the break statement that is needed at the end of each case in those languages is provided automatically in Golang.

### "for" is Go's "while"
C's while is spelled for in Go.

```
	sum := 1
	for sum < 1000 {
		sum += sum
	}
	fmt.Println(sum)
```

### Named return falues for function
```
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}
```

### Exported names
In Go, a name is exported if it begins with a capital letter
