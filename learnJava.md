# Java 学习笔记

## Day 1

2020-4-29

开始 [HackerRank](https://www.hackerrank.com) 的 [30 Days of Code](https://www.hackerrank.com/domains/tutorials/30-days-of-code)。

### Scanner 的用法

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in); // 创建Scanner对象
        System.out.print("Input your name: "); // 打印提示
        String name = scanner.nextLine(); // 读取一行输入并获取字符串
        System.out.print("Input your age: "); // 打印提示
        int age = scanner.nextInt(); // 读取一行输入并获取整数
        System.out.printf("Hi, %s, you are %d\n", name, age); // 格式化输出
    }
}

//代码示例来自廖雪峰的官方网站

```

**注意**

`scanner.next()`（包括`scanner.nextInt()`、`scanner.nextDouble`等）与`scanner.nextLine()`不同，
在`scanner.next`之后使用`scanner.nextLine()`，可能会读取到空字符。

可以用`scanner.skip()`跳过换行符、空格等，例如：

```
scanner.skip("(\r\n|[\n\r\u2028\u2029\u0085])?");
```

## Day 2

2020-5-1

### Double to Int

Use the `Math.round()` method.

## Day 3

2020-5-12

### 获取当前时间

```java
import java.text.SimpleDateFormat;
import java.util.Date;
 
public class Main{
    public static void main(String[] args){
        
        SimpleDateFormat sdf = new SimpleDateFormat();// 格式化时间 
        sdf.applyPattern("yyyy-MM-dd HH:mm:ss a");// a为am/pm的标记  
        Date date = new Date();// 获取当前时间 
        System.out.println("现在时间：" + sdf.format(date)); // 输出已经格式化的现在时间（24小时制） 
    } 
}
```

[来源](https://www.runoob.com/java/date-time-datetime.html)
 
