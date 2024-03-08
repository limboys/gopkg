## func clear[T ~[]Type | ~map[Type][Type](t T)

参数说明：

* t T类型元素
* T Type类型切片或key为Type,value为Type的map

返回值：

* 无

功能说明：

clear 内置函数将清除slice和map中的值。对于map，会删除所有key-value，使map为空。对于slice，会将所有元素设置为改类型的零值。

clear 内置函数参数仅支持slice和map。

代码实例：

```go
package main

import "fmt"

func main() {
	m1 := map[any]any{
		1: 1,
		2: 2,
		3: 3,
	}
	fmt.Printf("%#v\n", m1)
	clear(m1)
	fmt.Printf("%#v\n", m1)

	m2 := map[int]string{
		1: "a",
		2: "b",
		3: "c",
	}
	fmt.Printf("%#v\n", m2)
	clear(m2)
	fmt.Printf("%#v\n", m2)
	println()

	s1 := []any{
		'a',
		'b',
		'c',
	}
	fmt.Printf("%#v\n", s1)
	clear(s1)
	fmt.Printf("%#v\n", s1)

	s2 := []string{
		"a",
		"b",
		"c",
	}
	fmt.Printf("%#v\n", s2)
	clear(s2)
	fmt.Printf("%#v\n", s2)
}
```

输出：

```
map[interface {}]interface {}{1:1, 2:2, 3:3}
map[interface {}]interface {}{}
map[int]string{1:"a", 2:"b", 3:"c"}
map[int]string{}

[]interface {}{97, 98, 99}
[]interface {}{interface {}(nil), interface {}(nil), interface {}(nil)}
[]string{"a", "b", "c"}
[]string{"", "", ""}
```
