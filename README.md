# 14 Singleton & Threads

## Singleton
An example of where the singleton pattern is used is in the Spring Framework. If you add the to your code and run your application http://localhost:8080 you can detect that the StudentsController class is only instanciated once.

````    
    private int time = 1;
    
    public StudentsController(){

        System.out.println("I was called " + time + " time(s)");
        time++;
    }
````     


## Threads

### Multithreading and Singleton

## Literature

* [Java - How to Use Singleton Class](https://www.tutorialspoint.com/java/java_using_singleton.htm)

&copy; KEA, clbo 2018
