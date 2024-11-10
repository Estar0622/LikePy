<h1>PyLike</h1>
PyLike is an open-source library designed for use in Spring Boot.

The Java Collection Framework can be cumbersome compared to Python’s collections. Due to the complex inheritance hierarchy, remembering the method’s owner object is necessary for usage. With PyLike, Java can be made more “Pythonic”!

1. Overview
Make Java Pythonic!

PyLike was developed to bring Python’s simplicity and elegance to Java, allowing for cleaner and more concise code.

Write Pythonic code in Java.
Use intuitive, Python-style built-in functions in Java.
Treat the Java Collection Framework as if it were a primary data type, similar to Python’s approach.
Use method names consistent with Python for working with Java’s Collection Framework.
No need to remember the inheritance structure of the Collection Framework.
2. Setup
To install, add the following code to your build.gradle file and build:

groovy

allprojects {
  repositories {
      ...
      maven { url 'https://jitpack.io' }
  }
}

dependencies {
    implementation 'com.github.yjsayya:PyLike:0.0.2'
}
3. Usage and Examples
PyLike - Built-in Functions
Pl.abs() - Absolute value
Pl.divmod() - Quotient and remainder
Pl.input() - Input
Pl.int() - Convert to integer
Pl.float() - Convert to float
Pl.len() - Get length
Pl.max() - Get maximum value
Pl.min() - Get minimum value
Pl.pow() - Get power value
Pl.range() - Create a list for iteration
Pl.print() - Print output
Pl.sorted() - Sort items
Pl.sum() - Get the total sum
Pl.in() - Check containment (1)
Pl.not_in() - Check containment (2)
For more details, please visit PyLike Documentation.

Examples
Example 1
Python Code:

python
코드 복사
for i in range(1,11):
    print(i)
Equivalent PyLike Code:

java
코드 복사
for (int i : Pl.range(1,11)) {
    Pl.print(i);
}
Example 2 (Programmers) - Smaller Substring
Python Code:

python
코드 복사
def solution(t, p):
    length = len(p)
    cnt = 0

    for i in range(length, len(t)+1):
        if t[i-length:i] <= p:
            cnt += 1
    
    return cnt
Equivalent PyLike Code:

java
코드 복사
public static int solution(String t, String p) {
    int length = Pl.len(p);
    int cnt = 0;

    for (int i : Pl.range(length, Pl.len(t)+1)) {
        String str = Pl.slicing(t, i - length, i);
        if (str.compareTo(p) <= 0)
            cnt += 1;
    }
    return cnt;
}
Example 3 (Programmers) - Fruit Vendor
Python Code:

python
코드 복사
def solution(k, m, score):
    score.sort()
    price = 0
    length = len(score)

    start_point = length % m

    while start_point < length:
        price += score[start_point] * m
        start_point += m

    return price
Equivalent PyLike Code:

java
코드 복사
public int solution2(int k, int m, int[] score) {
    List<Integer> li = Pl.list(score);
    Pl.sort(li);
    int price = 0;
    int length = Pl.len(li);

    int start_point = length % m;

    while (start_point < length) {
        price += Pl.get(li, start_point) * m;
        start_point += m;
    }
    return price;
}
