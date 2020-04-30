# 学习 Java 的笔记

## Day 1

2020-4-29

开始 [HackerRank](https://www.hackerrank.com) 的 30 Days of Code

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

`scanner.next()`（包括`scanner.nextInt()`、`scanner.nextDouble`）与`scanner.nextLine()`不同，
在`scanner.next`之后使用`scanner.nextLine()`，可能会读取到空字符。



