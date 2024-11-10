<h1>PyLike</h1>

<p>PyLike is an open-source library designed for use in Spring Boot.</p>

<p>The Java Collection Framework can be cumbersome compared to Python’s collections. Due to the complex inheritance hierarchy, remembering the method’s owner object is necessary for usage. With PyLike, Java can be made more “Pythonic”!</p>

<h2>1. Overview</h2>

<p><strong>Make Java Pythonic!</strong></p>

<p>PyLike was developed to bring Python’s simplicity and elegance to Java, allowing for cleaner and more concise code.</p>

<ul>
    <li>Write Pythonic code in Java.</li>
    <li>Use intuitive, Python-style built-in functions in Java.</li>
    <li>Treat the Java Collection Framework as if it were a primary data type, similar to Python’s approach.</li>
    <li>Use method names consistent with Python for working with Java’s Collection Framework.</li>
    <li>No need to remember the inheritance structure of the Collection Framework.</li>
</ul>

<h2>2. Setup </h2>

<p>To install, add the following code to your build.gradle file and build:</p>

<pre>
<code>
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}

dependencies {
    implementation 'com.github.yjsayya:PyLike:0.0.2'
}
</code>
</pre>

<h2>3. Usage and Examples</h2>
<h3>PyLike - Built-in Functions</h3>

<li>Pl.abs() - Absolute value</li>
<li>Pl.divmod() - Quotient and remainder</li>
<li>Pl.input() - Input</li>
<li>Pl.int() - Convert to integer</li>
<li>Pl.float() - Convert to float</li>
<li>Pl.len() - Get length</li>
<li>Pl.max() - Get maximum value</li>
<li>Pl.min() - Get minimum value</li>
<li>Pl.pow() - Get power value</li>
<li>Pl.range() - Create a list for iteration</li>
<li>Pl.print() - Print output</li>
<li>Pl.sorted() - Sort items</li>
<li>Pl.sum() - Get the total sum</li>
<li>Pl.in() - Check containment (1)</li>
<li>Pl.not_in() - Check containment (2)</li>
For more details, please visit PyLike Documentation.


<h2>4. Examples </h2>
<h3>Example 1</h3>
Python Code:
<pre>
    <code>
        for i in range(1,11):
    print(i)
    </code>
</pre>

Equivalent LikePy Code:
<pre>
    <code>
        for (int i : Pl.range(1,11)) {
    Pl.print(i);
}
    </code>
</pre>

<h3>Example 2 (Programmers) - Smaller Substring</h3>
Python Code:
<pre>
    <code>
        def solution(t, p):
    length = len(p)
    cnt = 0

    for i in range(length, len(t)+1):
        if t[i-length:i] <= p:
            cnt += 1
    
    return cnt
    </code>
</pre>

Equivalent LikePy Code:
<pre>
    <code>
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
    </code>
</pre>

<h3> Example 3 (Programmers) - Fruit Vendor</h3>
Python Code:
<pre>
    <code>
        def solution(k, m, score):
    score.sort()
    price = 0
    length = len(score)

    start_point = length % m

    while start_point < length:
        price += score[start_point] * m
        start_point += m

    return price
    </code>
</pre>

Equivalent LikePy Code:
<pre>
    <code>
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

    </code>
</pre>
