# Object Oriented Programming (OOP)
### Definition
It`s a programming paradigm based on the concept of object.

* Programming Paradigm: It is a style of programming, a way of thinking about software construction.
* Programming paradigm doesn`t refer to a specific language.
* Some programming language allow more than one paradigm.

### Programing Paradigms
* Procedural 
    * Basic 
    * Pascal 
* Object-Oriented 
    * C++ 
    * java 
* Evet-driven 
    * Visual Basic 
    * C#
* Functional
    * lisp
    * Scheme
* Declarative 
    * Prolog 

### Object 
It's a thing (student, teacher, course), it has the following:
* Data or Attributes  
* Operations() or behaviors()
#### Example
* Product 
    * Data 
        * Product_Name 
        * Product_Code 
        * product_price
        * Product_Discount

    * Operations()
        * modify_Price()
        * set_discount()
        * get_product_name()

### Class
It's a blueprient, (Class = DataType).
* Class Class_Name
    *Data
    *Operations()

* When program is running it can use class to create objects.
* Each object that is created from the class is called an instance of the class.
* We can create instance of the class by write the class name followed by the class instance.
    * Example: Rectangle box;


#### Example
A rectangle Class will have the following fields:
    * Attributes
        * length 
        * width
    * Operations()
        * setLength()
        * setWidth()
        * getLength()
        * getWidth()
        * getArea()

* Header_File.h
```c++
#ifndef RECTANGLE_H  // Gard Header
#def RECTANGLE_H

Class Rectangle{
    Private:
            float Length;
            float Width;
    Public:
            void setLength(float len);
            void setWidth(float wid);
            float getLength();
            float getWidth();
            float getArea();
}

```
* Implementation_File.cpp
```c++
Rectangle::float Length;
Rectangle::float Width;

Rectangle::void setLength(float len){
        Length = len;
    }
Rectangle::void setWidth(float wid){
         Width = wid;
    }
Rectangle::float getLength(){
        return Length;
    }
Rectangle::float getWidth(){
        return Width;
    }
Rectangle::float getArea(){
        return Width * Length;
    }

```

### Access Modifiers
It is a Keyword that indicates how a field or a method can be accessed 

* Public
    * The member can be accessed by code inside or outside the class
* Private
    * the member can only be accessed by the methods of the same class

### Code Files
The code is separated into three files.
* Header_File.h
    * it Contains the declaration of all class members (attributes & prototypes)
* Implementation_File.cpp
    * it contains the implementations of the class methods
* Client File (main.cpp)
    * it contains the main function and should be stored by name main.cpp

### Constructor 
* It is a special member method that is called automatically when an object is created and it must have the same name as the Class.
* It can initialize object attributes and perform other object initialization.

#### Example 

* Header_File.h
```c++
#ifndef RECTANGLE_H  // Gard Header
#def RECTANGLE_H

Class Rectangle{
    Private:
            float Length;
            float Width;
    Public:
            Rectangle(float len, wid);
            void setLength(float len);
            void setWidth(float wid);
            float getLength();
            float getWidth();
            float getArea();
}

```
* Implementation_File.cpp
```c++
Rectangle::Float Length;
Rectangle::Float Width;

Rectangle::Rectangle(float len, wid):Length{len},Width{wid}{

}
Rectangle::void setLength(float len){
    Length = len;
}
Rectangle::void setWidth(float wid){
    Width = wid;
}
Rectangle::float getLength(){
    return Length;
}
Rectangle::float getWidth(){
    return Width;
}
Rectangle::float getArea(){
    return Width * Length;
}

```

### Destructor
* It is a special member method that is called automatically when an object lifetime is ended and it must have the same name as the Class.

#### Example 

* Header_File.h
```c++
#ifndef RECTANGLE_H  // Gard Header
#def RECTANGLE_H

Class Rectangle{
    Private:
            float Length;
            float Width;
    Public:
            Rectangle(float len, wid); //constructor Declaration
            void setLength(float len);
            void setWidth(float wid);
            float getLength();
            float getWidth();
            float getArea();
            ~Rectangle(); //destructor Declaration
}

```
* Implementation_File.cpp
```c++
Rectangle::Float Length;
Rectangle::Float Width;

Rectangle::Rectangle(float len, wid):Length{len},Width{wid}{ // Constructor Implementation

}
Rectangle::void setLength(float len){
    Length = len;
}
Rectangle::void setWidth(float wid){
    Width = wid;
}
Rectangle::float getLength(){
    return Length;
}
Rectangle::float getWidth(){
    return Width;
}
Rectangle::float getArea(){
    return Width * Length;
}
Rectangle::~Rectangle(){ // Destructor Implementation
    cout<<"GoodBye";
}

```

### Overloading
#### Method Overloading
It is a two or more methods in a class may have the same name as long as the have different signature.

##### Method Signature
* Number of Arguments
* Types of Arguments
* Order of Arguments

###### Example
* int add(int num1, int num2){return num1+num2;}
* int add(int num1,float num2, int num3){return num1+num2+num3;}

#### Constructor Overloading 
We can also include two constructor in one class
```c++
Rectangle();
Rectangle(int l, int w);

```
#### The Default Copy Constructor
Create a new object with the same properties value of another object 
```c++
Rectangle rect1(1,2);
Rectangle rect2(rect1);   // Copy Constructor 
Rectangle rect2 = rect1;  // Copy Constructor 
```
#### Operator Overloading


### Passing Objects as a method arguments
We can use class the same as we use a datatype we just create a function that will return a Rectangle and pass Rectangle objects as arguments.

```c++
Rectangle Merge (Rectangle rect1, Rectangle rect2){

}
```
### Static Class Members
The static fields and static methods d not belong to a single instance of a class (global attributes & methods).
*  A static data item is useful when all items of the same class must share a common information.
* The lifetime of a static member is the entire program, It continuous to exist even there are no objects of the class.
* To invoke a static method or static field we use the Class name rather than instance name.

#### Static Methods
* It may be called at the class level.
* They are typically used to create utility classes.
* Static methods only communicate with static fields.


