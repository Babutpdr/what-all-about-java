# what-all-about-java

## What is java class loader and types of loaders
  - The java class loaders are used to load <b>.class</b> files into the JVM at runtime.</br>
<h6> Types of class loaders </h6></br>
There are 3 main types of class loaders</br>
<b>Bootstrap</b>class loader loads all java core classes like java.lang,java.util etc..
<b>Extention</b>class loader loads the class that defines under JAVA_HOME/lib/ext </br>
<b>System</b>class loader that loads the class from CLASSPATH</br>
* All classes that we write in our application and all dependencies imported from JARs file are loaded by System class loader
    
 
