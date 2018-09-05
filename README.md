# doc
文档和书籍

### 方法即为有接受者的函数，接受者可以是类型的实例变量或者是类型的实例指针变量。
#### https://blog.csdn.net/huwh_/article/details/77879970

## 指针
#### 在函数操作方面，任何参数都是值传递,指针也不列外。指针传值的时候,对指针指向的内容(**int)修改之后,外部可以体现,但是直接修改指针,外部是不会有变化的.
```go
func TestT2(t *testing.T) {
	var a int
	a = 20
	fmt.Printf("%v\n",a)
	str(&a)
	fmt.Printf("%v\n",a)
	str1(&a)
	fmt.Printf("%v\n",a)
}

func str(a *int) {
	x := 100
	a = &x //这里只是修改了传来的指针,因为指针也是值传递,所以外部a不会有任何变化
}

func str1(a *int) {
	x := 100
	*a = x //这里是修改了传来的指针指向的内容,所以外部a就变成100了
}
```
