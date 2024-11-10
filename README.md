<h1>PyLike</h1>

<p>PyLike는 Spring Boot에서 사용할 수 있는 오픈소스 라이브러리입니다.</p>

<p>Java의 Collection Framework은 Python에 비해 사용하기 불편합니다. 상속관계가 복잡하기 때문에 메서드의 소속 객체를 외워야 사용이 가능합니다. Java에서도 Python의 내장함수와 iterable 객체처럼 메서드명으로만 사용하고 싶었습니다.</p>

<h2>1. 설명</h2>

<p><strong>Java를 Pythonic하게!!</strong></p>

<p>Python의 장점을 Java에 이식하여 Java를 보다 간결하고 깔끔한 코드를 작성할 수 있도록 PyLike를 제작하였습니다.</p>

<ul>
    <li>Java에서도 Pythonic한 코드 작성이 가능합니다.</li>
    <li>Python의 직관적이고 간결한 내장함수(Built-in Functions)를 Java에서도 사용 가능합니다.</li>
    <li>Python처럼 Java Collection Framework를 기본 자료형처럼 다룰 수 있습니다.</li>
    <li>Python과 동일한 메서드명으로 Java의 Collection Framework를 사용할 수 있습니다.</li>
    <li>Collection Framework의 상속 구조를 몰라도 됩니다.</li>
</ul>

<h2>2. 설정 방법</h2>

<p>build.gradle 파일에 다음 코드를 추가하고 빌드해주세요:</p>

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
