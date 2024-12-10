# JAVA_learn

## 1，枚举
在方法传递参数的时候，参数大多时候是不受控制的，有整型，字符串，字符等，为限制其传递，可以用枚举类来限定参数的类型
关键字 `enum`
```java
//初始化一个枚举类
public enum Book{
  EngLish,China,Math;
}

//方法中限定参数类型
//传递的参数只能是 Book 类型的，只能是枚举类型中的三个值之一
public void get(Book book){

}

//使用
get(Book.English);

//或者
Book text = Book.English;
get(text);

```

#### 枚举的好处
- 唯一性，限定了参数的范围，传递的参数只能是枚举中的值，否则会报错。
- 代码可读性，安全性都提高

### 携带更多值
```java
public enum Book{
        English("英语","晦涩难懂的语言"),
        China("语文","简单但不会所有人都喜欢"),
        Math("数学","god,神中神！");

        private String name;
        private String jieshao;

        Book(String name,String jieshao){
            this.name = name;
            this.jieshao = jieshao;
        }
       
    }
//调用的时候还是
Book book = Book.China;


//不过在使用的时候可以限定使用的参数, 如
Sysname.out.println(book.name) 或者  Sysname.out.println(book.jieshao)
```
在定义枚举类的时候，代码会自动将构造函数将参数传递给 枚举类，实现参数的使用。
