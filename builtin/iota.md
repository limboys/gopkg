## const iota = 0

iota是一个特殊的内置标识符，用于简化常量定义，特别是需要序列递增时。

功能说明：

* iota作为一个常量值，在const块中每次新的常量声明时都会自动递增
* iota从块中的第一个常量0值开始，后续每个常量依次怎加1

代码实例：

```go
package main

import "fmt"

const (
	c0 = iota //iota=0
	c1        //iota=1
	c2        //iota=2
	c3        //iota=3
)
const (
	s0 = iota
	s1
	_ //舍弃iota值
	s3
)

func main() {
	fmt.Printf("c0:%d c1:%d c2:%d c3:%d\n", c0, c1, c2, c3)
	fmt.Printf("s0:%d s1:%d s2:舍弃 s3:%d", s0, s1, s3)
}

```

输出：

```
c0:0 c1:1 c2:2 c3:3
s0:0 s1:1 s2:舍弃 s3:3
```
