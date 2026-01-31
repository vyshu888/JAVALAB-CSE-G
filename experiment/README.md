# experiment 1
## TITLE : 1a.) DISPALY PRIMITIVE DATA TYPES
```java
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
### Output:
![output for Default Primitvie Data Types](https://github.com/vyshu888/JAVALAB-CSE-G/blob/8b915146ba10b36680b44e947c6eea91e6a02754/1a.output.png)

## TITLE : 1b.) Quadratic equation solution
```java
// program code here

import java.util.Scanner;
class QuadraticEquationSolution {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a value of a:");
        double a = sc.nextDouble();
        System.out.println("Enter a value of b:");
        double b = sc.nextDouble();
        System.out.println("Enter a value of c:");
        double c = sc.nextDouble();
        double D = b * b - 4 * a * c;
        if (D > 0) {
            double x1 = (-b + Math.sqrt(D)) / (2 * a);
            double x2 = (-b - Math.sqrt(D)) / (2 * a);
            System.out.println("Roots are real and distinct:");
            System.out.println("x1 = " + x1);
            System.out.println("x2 = " + x2);
        } 
        else if (D == 0) {
            double y = -b / (2 * a);
            System.out.println("The roots are real and equal:");
            System.out.println("y = " + y);
        } 
        else {
            double real = -b / (2 * a);
            double img = Math.sqrt(-D) / (2 * a);
            System.out.println("Roots are complex:");
            System.out.println("x1 = " + real + " + " + img + "i");
            System.out.println("x2 = " + real + " - " + img + "i");
        }
        sc.close();
    }
}
```
### Output:
![output for quadratic equation](https://github.com/vyshu888/JAVALAB-CSE-G/blob/5648c16460a1427b3b2dd7789ca7706d61ddfc30/1boutput.png)
## experiment 2
## TITLE: 2a.) Implement class mechanism in java
```
class Rectangle {
   double length;
   double breadth;
   double area() {
     return length * breadth;
     }
   double perimeter() {
     return 2 * (length + breadth);
   }
 }
 class main {
   public static void main(String args[]) {
     Rectangle rect = new Rectangle();
     rect.length = 10;
     rect.breadth = 5;
     double area = rect.area();
     double perimeter = rect.perimeter();
     System.out.println("Area of given rectangle = " +area);
     System.out.println("perimeter of the given rectangle:" + perimeter);
   }
 }

```
## OUTPUT:
![output for mechanism in java](https://github.com/vyshu888/JAVALAB-CSE-G/blob/39bffddaca4df8c604a743521c0257e2c5428213/2a.output.png)
## TITLE: 2b.) Implementing overloading methods in java
```
 class sum {
    int sum(int a,int b) {
      return a + b;
   }
   int sum(int a,int b,int c) {
      return a + b +c;
   }
   double sum(double a,double b) {
      return a + b;
   }
 }
 class main {
  public static void main(String args[]) {
    sum s = new sum();
    System.out.println("sum of 2 integers:" + s.sum(36,46));
    System.out.println("sum of 3 integers:" + s.sum(20,36,46));
    System.out.println("sum of two real number:" + s.sum(30-465,15-675));
  }
 }
```
## OUTPUT:
![output for overloading methods](https://github.com/vyshu888/JAVALAB-CSE-G/blob/33197d51f6477efa6b2faeabf9b5d3a2b3bb4f59/2b.output.png)
## TITLE : TO IMPLEMENT CUNSTRUCTOR IN JAVA
```
 class Student {
    String Sname;
    int Sage;
    double Smarks;
    Student(String name, int age, double marks) {
         Sname = name;
         Sage = age;
         Smarks = marks;
    }
    void display() {
        System.out.println(" Student Name: " + Sname);
        System.out.println(" Student Age: " + Sage);
        System.out.println(" Student Marks: " + Smarks);
    }
}
 class main {
   public static void main(String args[]) {
     Student  S = new Student("bunny",28,965);
     S.display();
   }
 }
```
## OUTPUT:
![output for constructor](https://github.com/vyshu888/JAVALAB-CSE-G/blob/9ec9a1c9b784d126ef3edcdfb0850941cc1f9d2a/2c.output.png)
# Additional experiment 2
## TITLE : Fibonacis series
```
class Fibonacis {
    int firstNumber;
    int secondNumber;
    int thirdNumber;
    int sum;
    int sizeofFibsequence;
    Fibonacis(int size) {
    firstNumber = 0;
    secondNumber = 1;
    thirdNumber = 0;
    sum = 0;
    sizeofFibsequence = size;
  }
  void generateFibsequence() {
    while(sizeofFibsequence > 0) {
      if(sizeofFibsequence == 1)
    System.out.print(firstNumber + ".");
    else
       System.out.print(firstNumber + ",");
       sizeofFibsequence--;
       sum += firstNumber;
       thirdNumber = firstNumber + secondNumber;
       firstNumber = secondNumber;
       secondNumber = thirdNumber;
    }
  }
  int getFibsum() {
    if(sum > 0) {
     return sum;
    } else {
       generateFibsequence();
         return sum;
    }
  }
 }
import java.util.Scanner;
 class main {
 public static void main(String args[]) {
   System.out.print("enter the size of the sequence:");
      Scanner Sc = new Scanner(System.in);
      int size = Sc.nextInt();
      if(size > 0) {
      Fibonacis fib = new Fibonacis(size);
      System.out.println("Fibonacis series are:");
         fib.generateFibsequence();
         System.out.println("the sum of Fibonacis series:" + fib.getFibsum());
         }
         else
         System.out.println("Fibonacis sequence and cannot be calculated");
      }
 }
```
![output for Fibonacis](https://github.com/vyshu888/JAVALAB-CSE-G/blob/d67dbba7359e805290a629db4716ac951598acb7/additional%20output.png)
# EXPERIMENT 3
## TITLE :3A.)CONSTRUCTOR OVERLOADING IN JAVA
```
 class student {
   String name;
   int age;
   double marks;
   student() {
   }
   student(String name,int age,double marks) {
      this.name = name;
      this.age = age;
      this.marks = marks;
   }
   void display() {
     System.out.println("student name:" + name);
     System.out.println("student age:" + age);
     System.out.println("student marks:" + marks);
   }
 }
class main {
  public static void main(String args[]) {
    student std = new student();
    std.display();
    student std1 = new student("bunny",21,999.9);
    std1.display();
  }
 }
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/156d6c7919c0a57bbd0c2f551a91a7e4e5ff632c/3a%20output.png)
## TITLE :3B.) BINARYSEARCH MECHANISM
```
import java.util.Scanner;

class Binarysearch {
    int list[];
    int size;

    Binarysearch(int size) {
        this.size = size;
        list = new int[size];
    }

    void setlist() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the list items in Ascending order:");
        
        for (int i = 0; i < size; i++) {
            System.out.println("Enter value " + (i + 1) + ": ");
            list[i] = sc.nextInt();
        }
    }

    void getlist() {
        for (int i = 0; i < size; i++)
            System.out.print(list[i] + ",");
        System.out.println("\b\b.");
    }

    int Binarysearch(int key) {
        int low = 0;
        int high = list.length - 1;

        while (low <= high) {
            int mid = (low + high) / 2;

            if (list[mid] == key)
                return mid;

            else if (list[mid] < key)
                low = mid + 1;

            else
                high = mid - 1;
        }

        return -1; 
    }
}
import java.util.Scanner;

class main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        Binarysearch bs = new Binarysearch(10);

        bs.setlist();
        bs.getlist();

        System.out.println("Enter the key to search: ");
        int key = sc.nextInt();

        int index = bs.Binarysearch(key);

        if (index == -1)
            System.out.println("Key item does NOT exist.");
        else
            System.out.println("Key item exists at index: " + index);
    }
}
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/b4dffc9b4771e158f3b71b46a5d27ea143542b08/3b%20output.png)
## TITLE : 3C.) BUBBLE SORTING
```
 import java.util.Scanner;

class BubbleSort {
    void bubbleSort(int arr[]) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }
}
import java.util.Scanner;
 class Main {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the size of the array: ");
        int size = sc.nextInt();

        int arr[] = new int[size];

        for (int i = 0; i < size; i++) {
            System.out.print("Enter element " + (i + 1) + ": ");
            arr[i] = sc.nextInt();
        }

        BubbleSort bs = new BubbleSort();
        bs.bubbleSort(arr);

        System.out.print("Sorted array: ");
        for (int i = 0; i < size; i++) {
            System.out.print(arr[i] + " ");
        }
        System.out.println();
    }
}
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/f8eb0b9104684e55eaf45310c60d33bd91de28a3/3c%20output.png)
#EXPERIMENT -4:
## TITLE : 4a.) SINGLE INHERITANCE:
```
class Person {
    String name;
    int age;

    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayPersonDetails() {
        System.out.println("Name : " + name);
        System.out.println("Age  : " + age);
    }
}
 class Employee extends Person {
    double annualSalary;
    int yearOfJoining;
    String nationalInsuranceNumber;
    Employee(String name, int age, double annualSalary, int yearOfJoining, Stri>
        super(name, age);
        this.annualSalary = annualSalary;
        this.yearOfJoining = yearOfJoining;
        this.nationalInsuranceNumber = nationalInsuranceNumber;
    }
      void displayEmployeeDetails() {
        displayPersonDetails();
        System.out.println("Annual Salary : " + annualSalary);
        System.out.println("Year Of Joining : " + yearOfJoining);
        System.out.println("National Insurance Number : " + nationalInsuranceNu>
    }
}
 public class TestEmployee {
    public static void main(String[] args) {
        Employee emp1 = new Employee(
                "vyshu",
                18,
                700000,
                2028,
                "NI123456A"
        );

        emp1.displayEmployeeDetails();
    }
}
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/a9c23ae3f6f704ee2e93ff0e057f21ca163f66aa/4a.output.png)
## TITLE : 4B.) MULTIPLE INHERITANCE:
```
class Bicycle {
    String pedalType;

    void showBicycleInfo() {
        System.out.println("This is a bicycle with pedals.");
        System.out.println("Pedal Type : " + pedalType);
    }
}
 class Motorbike extends Bicycle {
    int engineCapacity;

    void showMotorbikeInfo() {
        System.out.println("This motorbike has an engine.");
        System.out.println("Engine Capacity : " + engineCapacity + " cc");
    }
}
class ElectricBike extends Motorbike {
    int batteryCapacity;

    void showElectricBikeInfo() {
        System.out.println("This electric bike has an electric motor and battery.");
        System.out.println("Battery Capacity : " + batteryCapacity + " Wh");
    }
}
 public class TestVehicle {
    public static void main(String[] args) {
        ElectricBike eBike = new ElectricBike();
        eBike.pedalType = "Standard Pedals";
        eBike.engineCapacity = 250;
        eBike.batteryCapacity = 500;
        eBike.showBicycleInfo();
        eBike.showMotorbikeInfo();
        eBike.showElectricBikeInfo();
    }
}
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/3b1b440fcfb9fe9e77b668b3763140e0799ac442/4b.output.png)
##TITLE : 4c.) ABSTRACT CLASS IN JAVA TO FIND AREA IN DIFFERENT SHAPES:
```
 abstract class Figure {
     double dim1;
     double dim2;
     Figure(double dim1,double dim2) {
     this.dim1 = dim1;
     this.dim2 = dim2;
     }
  abstract double area();
 }
 class Rectangle extends Figure {
   Rectangle(double length,double breadth) {
            super(length,breadth);
   }
   double area() {
   double result = dim1*dim2;
   return result;
   }
 }
 class Triangle extends Figure {
      Triangle(double base,double height) {
           super(base,height);
      }
      double area() {
             double result = 0.5*dim1*dim2;
             return result;
      }
 }
 class TestFigure {
      public static void main(String args[]) {

      Figure f1 = new Rectangle(23.4,14.5);
      Figure f2 = new Triangle(12.3,15.6);

      System.out.println("Area of Rectangle = " + f1.area());
      System.out.println("Area of Triangle =" + f2.area());
      }
 }
```
![output](https://github.com/vyshu888/JAVALAB-CSE-G/blob/e9784e3296eb6e1c227625e1442d27d6e5a95090/4c.output.png)
# Additional experiment 1
## TITLE : INSERT SUBSTRING
```
import java.util.Scanner;
 class InsertSubstring {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.print("mainString: ");
        String mainString = sc.nextLine();
        System.out.print("subString: ");
        String subString = sc.nextLine();
        System.out.print("position: ");
        int position = sc.nextInt();
        if (position < 0 || position > mainString.length()) {
        System.out.println("Invalid Position");
        } else {
            String firstPart = mainString.substring(0, position);
            String secondPart = mainString.substring(position);
            String resultString = firstPart + subString + secondPart;
            System.out.println("Resultant String: " + resultString);
        }

        sc.close();
    }
}
```
![output]()
# Additional experiment 3
```
import java.util.Scanner;
 class PalindromeCheck {
   public static void main(String args[]) {
     Scanner sc = new Scanner(System.in);
     System.out.print("enter a string:");
     String str = sc.nextLine();
     int start = 0;
     int end = str.length() - 1;
     while(start < end) {
     if(str.charAt(start) != str.charAt(end)) {
     System.out.println("str is  \"" + str + "\" not  Palindrome");
     sc.close();
     return;
     }
     start++;
     end--;
     }
     System.out.println("str \"" + str + "\" is a Palindrome");
     sc.close();
     }
 }
```
![output]()
# ADDITIONAL EXPERIMENT 4
```
 import java.util.Scanner;
class PerfectNumber {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int num = sc.nextInt();
        int sum = 0;
        for (int i = 1; i < num-1; i++) {
            if (num % i == 0) {
                sum = sum + i;
            }
        }

        if (sum == num) {
            System.out.println(num + " is a Perfect Number");
        } else {
            System.out.println(num + " is not a Perfect Number");
        }

        sc.close();
    }
}
```
![OUTPUT]()










