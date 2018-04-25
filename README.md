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
### Example 1

````     
    public class Singleton {

        private static Singleton singleton = new Singleton();

        private Singleton() { }
        
        public static Singleton getInstance( ) {
            return singleton;
        }
 
        protected static void singletonMethod( ) {
            System.out.println("I am a singleton method");
        }
    }
    
    
    public class Main {
        public static void main(String[] args) {
            Singleton.getInstance().demoMethod();
        }
    }
````    
#### Proof

````     
        public static void main(String[] args) {

            Singleton singleton = Singleton.getInstance();
            System.out.println(singleton);

            Singleton singleton2 = Singleton.getInstance();
            System.out.println(singleton2);

            Normal normal = new Normal();
            System.out.println(normal);

            Normal normal2 = new Normal();
            System.out.println(normal2);
        
       }

````     


## Threads

### Multithreading and Singleton

## Literature

* [Java - How to Use Singleton Class](https://www.tutorialspoint.com/java/java_using_singleton.htm)

&copy; KEA, clbo 2018
