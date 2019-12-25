# Demonstration
 java code Demonstration on encapsulation, inheritance,  polymorphism,Abstraction
Encapsulation Code and discription

package encla;

    public class Student {

		private int age;
		private String name;
		public int getAge() {
			return age;
		}
		public void  setAge(int age) {
			if(age > 20) {
				System.out.print("too old");
			}else {
			this.age=age;
			System.out.println("eligble");
		}
			}
	}
  
  package encla;

     public class encapsulation {
	 
	 public static void main(String[] args) {
        Student obj= new Student();
         obj.setAge(21);
    System.out.println(obj.getAge());
     }

   }

****Encapsulation
Principle: encapsulation in java is a process of Wrapping Code and data in a single unit. In 
encapsulation one class is hidden from another class

Advantages: It can provide the programmer to hide the inner classes and the user to give access only 
to the desired codes. It allows the programmer to not allow the user to know how variables and 
data store.

**polymorphism

package polymorphism;

Run time Polymorphism

            public class Runtime {
      //Run Time polymorphism
     void Print() 
    { 
        System.out.println("parent class"); 
              } 
            } 
  
        class subclass1 extends Runtime { 
  
    void Print() 
    { 
        System.out.println("St1"); 
    } 
} 
  
          class subclass2 extends Runtime { 
  
    void Print() 
    { 
        System.out.println("St2"); 
    } 
          } 
    class TestPolymorphism3 { 
               public static void main(String[] args) 
    { 
  
    	Runtime a; 
  
        a = new subclass1(); 
        a.Print(); 
  
        a = new subclass2(); 
        a.Print(); 
    } 
            } 

Compile Time Polymorphism

          package polymorphism;

             public class polymorphism {

    //Compile Time polymorphism
    static int Multiply(int a, int b) 
    { 
        return a * b; 
    } 
  
    static double Multiply(double a, double b) 
    { 
        return a * b; 
    } 

	public static void main(String[] args) {

        System.out.println(polymorphism.Multiply(3, 2)); 
  
        System.out.println(polymorphism.Multiply(5.5, 6.3));

	}

}

Description on Polymorphism
****polymorphism
It is divided into two parts 1. Compile time Polymorphism  2.Runtime Polymorphism

1. compile time Polymorphism: It is also known as static polymorphism. This type of polymorphism 
is achieved by function overloading.
  overloading is  When there are multiple functions with same name but different parameters then 
these functions are said to be overloaded. Functions can be overloaded by change in number of 
arguments 

2. Runtime Polymorphism: It is also known as Dynamic Method Dispatch. It is a process in which a 
function call to the overridden method is resolved at Runtime. This type of polymorphism is 
achieved by Method Overriding

Advantages: It helps  to reuse the code, classes, methods written once, tested and implemented. 
They may be reused in many way.

disadvantages: It is difficult to implement in the code.

Inheritance

          class Bicycle  
     { 
               public int gear; 
               public int speed; 
          
    public Bicycle(int gear, int speed) 
    { 
        this.gear = gear; 
        this.speed = speed; 
    } 
          
    public void applyBrake(int decrement) 
    { 
        speed -= decrement; 
    } 
          
    public void speedUp(int increment) 
    { 
        speed += increment; 
    } 
      
    public String toString()  
    { 
        return("No of gears are "+gear 
                +"\n"
                + "speed of bicycle is "+speed); 
    }  
} 
  
 
             class MountainBike extends Bicycle  
{ 
      
    public int seatHeight; 
  
    public MountainBike(int gear,int speed, 
                        int startHeight) 
    { 
        super(gear, speed); 
        seatHeight = startHeight; 
    }  
          

    public void setHeight(int newValue) 
    { 
        seatHeight = newValue; 
    }  
      

    @Override
    public String toString() 
    { 
        return (super.toString()+ 
                "\nseat height is "+seatHeight); 
    } 
      
} 
  
             public class Test  
          { 
     public static void main(String args[])  
    { 
          
        MountainBike mb = new MountainBike(3, 100, 25); 
        System.out.println(mb.toString()); 
              
    } 
         } 
Description on inheritance
****Inheritance
Principle: It help to write DRY (Don't repeat Yourself) code. A Child class to extented to another 
Class. And this is called as inheritance.

Advantages: It help to do not write same code multiple times

disadvantages: In there Two classes are depended to each other.

Abstration

    abstract class Type  
    { 
      String color; 
      
    // these are abstract methods 
    abstract double area(); 
    public abstract String toString(); 
      
    // abstract class can have constructor 
    public Shape(String color) { 
        System.out.println("Shape constructor called"); 
        this.color = color; 
    } 
      
    // this is a concrete method 
    public String getColor() { 
        return color; 
    } 
         } 
        class Circle extends Type 
           { 
    double radius; 
      
    public Circle(String color,double radius) { 
  
        // calling Type constructor 
        super(color); 
        System.out.println("Circle constructor called"); 
        this.radius = radius; 
    } 
  
    @Override
    double area() { 
        return Math.PI * Math.pow(radius, 2); 
    } 
  
    @Override
    public String toString() { 
        return "Circle color is " + super.color +  
                       "and area is : " + area(); 
    } 
      
                } 
     class Rectangle extends Type{ 
  
    double length; 
    double width; 
      
    public Rectangle(String color,double length,double width) { 
        // calling Shape constructor 
        super(color); 
        System.out.println("Rectangle constructor called"); 
        this.length = length; 
        this.width = width; 
    } 
      
    @Override
    double area() { 
        return length*width; 
    } 
  
    @Override
    public String toString() { 
        return "Rectangle color is " + super.color +  
                           "and area is : " + area(); 
    } 
  
            } 
      public class Test  
          { 
    public static void main(String[] args) 
    { 
        Shape s1 = new Circle("Red", 2.2); 
        Shape s2 = new Rectangle("Yellow", 2, 4); 
          
        System.out.println(s1.toString()); 
        System.out.println(s2.toString()); 
    } 
              } 
Description on Abstration
****Abstrations
Principle: It select Specific Type Of data And Hide Other Things. 

Advantage: 1. We can do more coding with Writing less code 
           2. Avoids code duplication and increases reusability
