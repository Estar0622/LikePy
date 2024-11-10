<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PyLike Documentation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #333;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 30px auto;
            padding: 20px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #007bff;
            font-size: 2em;
            margin-bottom: 0.5em;
            text-align: center;
        }
        h2 {
            color: #007bff;
            font-size: 1.5em;
            margin-top: 1em;
            border-bottom: 2px solid #007bff;
            padding-bottom: 5px;
        }
        p, li {
            margin: 0.5em 0;
        }
        code, pre {
            background-color: #e8e8e8;
            padding: 5px;
            border-radius: 5px;
            font-family: monospace;
        }
        ul {
            list-style-type: disc;
            margin-left: 20px;
        }
        .code-block {
            background-color: #f8f9fa;
            padding: 10px;
            border-left: 4px solid #007bff;
            margin: 1em 0;
            overflow-x: auto;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>PyLike</h1>
        <p><strong>PyLike</strong> is an open-source library designed for <strong>Spring Boot</strong>.</p>
        <p>The <strong>Java Collection Framework</strong> can be cumbersome compared to Python’s collections. Due to its complex inheritance structure, you need to remember which object owns each method. <strong>PyLike</strong> was developed to make Java more “Pythonic,” allowing for simpler and more readable code.</p>
        
        <ul>
            <li>Treat Java collections as iterable objects, just like in Python.</li>
            <li>Use Python-style built-in functions in Java for a more intuitive experience.</li>
        </ul>

        <h2>1. Overview</h2>
        <p><strong>Make Java Pythonic!</strong></p>
        <p>PyLike brings the advantages of Python into Java, enabling more concise and clean code.</p>
        
        <ul>
            <li>Write Pythonic code in Java.</li>
            <li>Use intuitive, Python-style built-in functions in Java.</li>
            <li>Handle Java Collection Framework as easily as Python’s built-in data types.</li>
            <li>Use Python-like method names for Java’s Collection Framework.</li>
            <li>No need to memorize the Collection Framework’s inheritance structure.</li>
        </ul>

        <h2>2. Installation</h2>
        <p>To install, add the following code to your <code>build.gradle</code> file and build:</p>
        
        <div class="code-block">
            <pre>
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}

dependencies {
    implementation 'com.github.yjsayya:PyLike:0.0.2'
}
            </pre>
        </div>
        
        <p>For more details, please visit <a href="https://pebble-noise-a5e.notion.site/PyLike-7cb9c7b338fc41e7a1f20794b77c953a?pvs=4" target="_blank">PyLike Documentation</a>.</p>
    </div>
</body>
</html>
