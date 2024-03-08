## func print(args ...Type)

参数说明：

* args Type类型元素
* ... 更多的Type类型元素

返回值：

* 无

功能说明：

print 内置函数将通过指定格式来格式化输入参数，并将结果输出到标准错误输出。可在代码调试中使用。

```
print("hello Go")
```

代码实例

```go
package main

func main(){
	print("hello Go")
	print("hello ")
	print("Go")
}
```

输出：

```
hello Gohello Go
```

##### 注意：print()与println()的区别

二者同样是输出格式化的参数内容到标准错误输出，println()与print()的区别是参数之间添加空格，末尾会添加换行符(\\n)。

代码实例：

```go
package main

func main() {
	print("hello Go ")
	print("hello ")
	print("Go ")
	println()
	println("hello Go")
	println("hello ")
	println("Go")
}
```

输出：

```
hello Go hello Go 
hello Go
hello
Go
```
