# Design patterns
Design patterns are used to address common problem in software development,based on nature of the problem,it is divided into 3 types </br>

<b>1. Creational design pattern:</b> It is related to creating new objects</br>
<b>2. Structural Design Pattern:</b></br>
<b>3. Behavioral Design Pattern:</b></br>
## Creational design pattern:
-> Factory Pattern.</br>
-> Abstract Factory Pattern.</br>
-> Builder Pattern.</br>
-> Prototype Pattern.</br>
-> Singleton Pattern.</br>
<h5> Factory Pattern</h5></br>

Factory pattern is commonly used pattern in our code,where there is class in inheritence relationship.Let us see the example </br>

```
package com.designpattern;

interface Document {
	public String getMimeType();
}

class PDFDocument implements Document {

	@Override
	public String getMimeType() {
		return "application/pdf";
	}
}

class TextDocument implements Document {

	@Override
	public String getMimeType() {
		return "text/plain";
	}
}

class WordDocument implements Document {

	@Override
	public String getMimeType() {
		return "application/msword";
	}
}

public class FactoryPattern {

	public static Document getDocument(String mimeType) {
		if (mimeType == null)
			return null;
		if (mimeType.equalsIgnoreCase("application/pdf")) {
			return new PDFDocument();
		} else if (mimeType.equalsIgnoreCase("text/plain")) {
			return new TextDocument();
		} else if (mimeType.equalsIgnoreCase("application/msword")) {
			return new WordDocument();
		}
		return null;
	}
	
	public static void main(String[] args) {
		System.out.println(FactoryPattern.getDocument("application/pdf").getMimeType());
	}
}
```
Note: From the above example all the object are created in one places instead of distributing across the all our codebases
