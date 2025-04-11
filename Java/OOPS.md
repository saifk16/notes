## Static var and instance var

static variables share the same copy, no matter how many object you create and try to access it.

```java
package StaticVar;

  

public class Demo {

    static int x = 10;

  

    static void display() {

        System.out.println(x);

    }

}

  

class Test {

    public static void main(String[] args) {

        Demo obj1 = new Demo();

        Demo obj2 = new Demo();

  

        ++obj1.x;

  

        System.out.println("X in object 1");

        obj1.display();

        System.out.println("X in object 2");

        obj2.display();

    }

}
```

instance variable will have different copy for every object created.

```java
package InstanceVar;

  

public class Demo {

    int x = 10;

  

    void display() {

        System.out.println(x);

    }

}

  

class Test {

    public static void main(String[] args) {

        Demo obj1 = new Demo();

        Demo obj2 = new Demo();

  

        ++obj1.x;

  

        System.out.println("X in object 1");

        obj1.display();

        System.out.println("X in obj 2");

        obj2.display();

  

    }

}
```

