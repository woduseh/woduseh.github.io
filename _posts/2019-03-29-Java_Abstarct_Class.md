---
layout: posts
title: "Java 추상 클래스"
categories: [Java]
---

Java Abstarct Class

05-8 추상클래스
추상클래스(Abstract Class)는 인터페이스의 역할도 하면서 뭔가 구현체도 가지고 있는 자바의 돌연변이 같은 클래스이다. 혹자는 추상클래스는 인터페이스로 대체하는것이 좋은 디자인이라고도 얘기한다.

추상클래스에 대해서 알아보기 위해 우리가 작성했던 Predator 인터페이스를 추상클래스로 둔갑시켜 보자.

※ 객체지향 프로그래밍 챕터에서 사용되는 예제는 모두 연속되므로 앞에서부터 순서대로 예제를 따라해야 한다.

Predator 인터페이스의 원래의 기능을 그대로 유지하기 위해서는 다음과 같이 변경되어야 한다.

Predator.java

```java
public abstract class Predator extends Animal {
    public abstract String getFood();
}
```
추상클래스를 만들기 위해서는 class 앞에 abstract 라고 표기해야 한다. 또한 인터페이스의 메소드와 같은 역할을 하는 메소드(여기서는 getFood 메소드)에도 역시 abstract 를 붙이도록 한다. abstract 메소드는 인터페이스의 메소드와 마찬가지로 몸통이 없다. 즉 abstract 클래스를 상속하는 클래스에서 해당 abstract 메소드를 구현해야만 하는 것이다.

Predator 인터페이스를 위와 같이 추상클래스로 변경하면 Tiger, Lion 클래스도 다음과 같이 변경되어야 한다.

Tiger.java

```java
public class Tiger extends Predator implements Barkable {
    public String getFood() {
        return "apple";
    }

    public void bark() {
        System.out.println("어흥");
    }
}
```
Lion.java

```java
public class Lion extends Predator implements Barkable {
    public String getFood() {
        return "banana";
    }

    public void bark() {
        System.out.println("으르렁");
    }
}
```
Tiger와 Lion클래스는 이제 Predator 인터페이스를 implements 하던 것에서 Predator 추상클래스를 extends 하도록 변경되었다.

그리고 Predator 추상클래스에서 abstract 메소드로 선언된 getFood 메소드가 위와 같이 구현되었다. 추상클래스에 abstract 로 선언된 메소드(getFood 메소드)는 인터페이스의 메소드와 마찬가지로 추상클래스를 상속하는 클래스에서 반드시 구현해야만 하는 메소드이다.

추상 클래스에는 abstract 메소드 뿐만 아니라 실제 메소드도 추가가 가능하다. 추상클래스에 실제 메소드를 추가하면 Tiger, Lion 등으로 만들어진 객체에서 그 메소드들을 모두 사용할 수 있게 된다.

예를 들어 아래와 같이 isPredator 라는 메소드를 Predator 추상클래스에 추가하면 이 클래스를 상속받은 Tiger, Lion 등에서 사용가능하게 된다.

```java
public abstract class Predator extends Animal {
    public abstract String getFood();

    public boolean isPredator() {
        return true;
    }
}
```


출처: https://wikidocs.net/219
