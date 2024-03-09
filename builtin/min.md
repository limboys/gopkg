## func min[T cmp.Ordered](x T, y ...T) T

参数列表：

* x T类型元素
* y T类型元素
* T com.Ordered类型，给类型可以是：~int | ~int8 | ~int16 | ~int32 | ~int64 | ~uint | ~uint8 | ~uint16 | ~uint32 | ~uint64 | ~uintptr | ~float32 | ~float64 | ~string

返回值：

* T类型元素

功能说明：

min 内置函数将返回参数列表中的最小值。当T是浮点类型，并且包含Nan，max()都将返回Nan。

min 参数列表至少要有一个参数。

代码实例：

```go
package main

func main() {
	println("min(0,1):", min(0, 1))
	println("min(0,-1):", min(0, -1))
	println("min(0,-1.1):", min(0, -1.1))
	println("min(0,1.1111):", min(0, 1.1111))
	println("min('a','c'):", string(min('a', 'c')))
}
```

输出：

```
min(0,1): 0
min(0,-1): -1
min(0,-1.1): -1.100000e+000
min(0,1.1111): +0.000000e+000
min('a','c'): a
```
