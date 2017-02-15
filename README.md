# Jump into developing with Java 8 from developing with Java 7

## Introduction
This is a very quick and practical guide to utilizing Java 8 methodlogies in development for those who are very familliar with Java 7, I will not be explaining much about new concepts of Java 8, so I assume you know Java 8 but don't know how to practically use it with your current existing code.

I will take a step by step method, each step will upgrade a part of the code from Java 7 to Java 8, those steps are not obligatory, but I would really suggest following them cause they will move your in gradial and effective manner

If you have no experience with Java 8 and it's new concepts you can check those books: 

1. [Java SE8 for The Really Impatient](https://www.amazon.com/Java-SE8-Really-Impatient-Course/dp/0321927761): I love this book, it is the fastest and most convient way to learn about Java 8
2. [Java 8 in Action](https://www.amazon.com/Java-Action-Lambdas-functional-style-programming/dp/1617291994/ref=sr_1_1?s=books&ie=UTF8&qid=1487126177&sr=1-1&keywords=java+8+in+action): This is a more comprehensive book about Java 8 and incorporating functional programming into our development style

## Why would you update your code?
There are many reasons why you would consider using Java 8's new features, first and foremost: Your code will be amazingly readable and maintainable. It's not a magic trick, it's simply that your code will now be declarative, which means that your code will represent it's intentions and will much much shorter.

## Upgrade steps:
All the steps I mention and why you should take them are from my opinions and my work, if you feel that one doesn't suit your needs, it's fine, just take another step or suggestion.

### First: Upgrading your interfaces and abstract classes:
Java 8 introduces the concept of **default methods** to interfaces, which are implemented methods in our interfaces, now how to know which interfaces and abstract classes should be changed, I will give you some suggestions:

* If you have abstract class implements default implementations to methods from an interface, but those implementations are not really doing anything, then you might consider moving those to the interface, this way the abstract class will represent a true implementation of the class without any dummy code, for example:
```java
interface A {
  void terminate();
}

abstract class AImpl {
  public void terminate() {
    //nothing here
  }
}
```

You may change that to:
```java
interface A {
  default void terminate(){
    //nothing here, or even better a default termination code
  }
}
```

To be continued..
