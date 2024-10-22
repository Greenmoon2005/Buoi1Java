### 1. Ngôn ngữ Java là gì?
Java là một trong những ngôn ngữ lập trình hướng đối tượng. Ngôn ngữ Java được sử dụng phổ biến trong phát triển phần mềm, trang web, game hay ứng dụng trên các thiết bị di động.

Java được khởi đầu bởi James Gosling và bạn đồng nghiệp ở Sun MicroSystem năm 1991. Ban đầu Java được tạo ra nhằm mục đích viết phần mềm cho các sản phẩm gia dụng, và có tên là Oak. Java được chính thức phát hành năm 1994, đến năm 2010 được Oracle mua lại từ Sun MicroSystem.
### 2. Lí do ra đời của Java
Java ra đời với mục tiêu chính là cung cấp một ngôn ngữ lập trình đơn giản, mạnh mẽ, bảo mật và độc lập với nền tảng. Ban đầu, Java được phát triển cho các thiết bị nhỏ như tivi thông minh, nhưng sau đó đã mở rộng và trở thành một ngôn ngữ phổ biến cho phát triển ứng dụng web, doanh nghiệp, và di động (Android).
### 3. Cách Java hoạt động
Java hoạt động dựa trên một quy trình đặc biệt là “Compile Once, Run Anywhere“, nhờ vào việc sử dụng Máy ảo Java. Cụ thể, khi bạn viết một chương trình Java, quy trình hoạt động của Java có thể được chia làm ba bước chính:

1. Viết mã nguồn: Lập trình viên viết mã nguồn Java trong các tệp .java.
2. Biên dịch mã nguồn: Mã nguồn Java được biên dịch bởi trình biên dịch Java (Java Compiler) thành bytecode (tệp .class). Bytecode này không phải là mã máy mà máy tính có thể hiểu ngay, nhưng nó là dạng trung gian có thể được hiểu bởi bất kỳ hệ điều hành nào có JVM.
3. Chạy chương trình: Bytecode sau đó được JVM thực thi. JVM dịch bytecode này thành mã máy (machine code) để hệ điều hành và phần cứng cụ thể có thể hiểu và thực thi chương trình.

**Quá trình chạy mã Java:**
1. Viết mã nguồn trong file `.java`.
2. Dùng lệnh `javac` để biên dịch mã thành file `.class` (bytecode).
3. JVM tải và chạy bytecode từ file `.class`.
### 4. Cấu trúc một chương trình Java
Một chương trình Java cơ bản sẽ có cấu trúc như sau:
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
Trong đó:
- `public class HelloWorld`: Khai báo lớp (class) tên là `HelloWorld`.
- `public static void main(String[] args)`: Phương thức `main` là điểm bắt đầu của chương trình.
- `System.out.println("Hello, World!");`: Câu lệnh in ra màn hình.
### 5. Package là gì?
Package trong Java là một cách để nhóm các lớp có liên quan lại với nhau, giúp tổ chức mã nguồn tốt hơn và tránh xung đột tên giữa các lớp. Ví dụ, `java.util` chứa các lớp tiện ích như `ArrayList`, `HashMap`. Các package cũng giúp quản lý quyền truy cập giữa các lớp.
```java
package mypackage;
public class MyClass {
    // code
}
```
### 6. Syntax cơ bản
#### a. Khai báo biến nguyên thủy
Java hỗ trợ 8 kiểu dữ liệu nguyên thủy: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`.
Ví dụ:
```java
int age = 25;
float height = 1.75f;
boolean isStudent = true;
```
#### b. Làm quen với vòng lặp
Java có các loại vòng lặp phổ biến như `for`, `while`, và `do-while`.
```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
int i = 0;
while (i < 10) {
    System.out.println(i);
    i++;
}
```
#### c. Câu lệnh rẽ nhánh
Sử dụng các câu lệnh `if`, `else if`, `else` và `switch`.
```java
int age = 20;
if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are a minor.");
}
int day = 3;
switch (day) {
    case 1: System.out.println("Monday"); break;
    case 2: System.out.println("Tuesday"); break;
    case 3: System.out.println("Wednesday"); break;
    default: System.out.println("Invalid day");
}
```
#### d. Mảng trong Java
Mảng (array) là một tập hợp các phần tử có cùng kiểu dữ liệu.
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}
```
### 7. Tổng quan về Class và Object
Java là ngôn ngữ lập trình hướng đối tượng, trong đó lớp (class) là khuôn mẫu để tạo ra các đối tượng (object). Mỗi đối tượng là một thể hiện của một lớp.
```java
class Person {
    String name;
    int age;
    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    // Getter
    public String getName() {
        return name;
    }
    // Setter
    public void setName(String name) {
        this.name = name;
    }
}
```
#### a. Từ khóa `this`
`this` dùng để tham chiếu đến đối tượng hiện tại của lớp.
```java
public class Example {
    private int x;
    public Example(int x) {
        this.x = x;  // this.x là thuộc tính, x là tham số
    }
}
```
#### b. Constructor
Constructor là phương thức đặc biệt được gọi khi khởi tạo đối tượng.
```java
public class Car {
    String model;
    // Constructor
    public Car(String model) {
        this.model = model;
    }
}
```
#### c. Access modifier
Các từ khóa như `public`, `private`, và `protected` dùng để kiểm soát quyền truy cập vào các thành phần trong lớp.
- `public`: Có thể truy cập từ bất kỳ đâu.
- `private`: Chỉ có thể truy cập trong lớp hiện tại.
- `protected`: Truy cập từ lớp con hoặc cùng package.
#### d. Getter và Setter
Getter và Setter được sử dụng để lấy và thay đổi giá trị của các thuộc tính trong lớp, thường kết hợp với `private`.
```java
class Student {
    private String name;
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
}
```
#### e. Từ khóa `static`
`static` được dùng cho các thành phần của lớp mà không liên quan đến đối tượng cụ thể, tức là thuộc về lớp thay vì đối tượng.
```java
class MathUtils {
    public static int square(int x) {
        return x * x;
    }
}
// Gọi phương thức static
int result = MathUtils.square(5);
```