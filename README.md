
# Java Journey, 06: Methods

In Java, methods are reusable blocks of code that perform specific tasks. They are an essential part of Java programming and help to reduce code duplication and improve code maintainability. Methods can be called from anywhere in the program and can take in parameters, and return values.

## Learn the syntax for creating methods in Java.

In Java, a method is a block of code that performs a specific task and can be reused throughout the program. A method is a subroutine or a function, which may or may not return a value.

To create a method in Java, the syntax is as follows:

```bash
access_modifier return_type method_name (parameter_list) {
   // method body
}
```

- Access modifiers specify the level of access to the method. It can be public, private, protected, or default.
- Return type indicates the type of value the method returns. If the method does not return any value, the return type is void.
- Method name is the name that is used to refer to the method throughout the program.
- Parameter list contains the input parameters that the method can accept. It can be empty if the method does not take any input.

Example:

```bash
public int sum(int a, int b) {
   int result = a + b;
   return result;
}
```

This method takes two integer parameters, a and b, and returns the sum of these two integers as an integer value.

Methods help in organizing code and improve code readability, reusability, and maintenance. They allow us to break down the program into smaller, manageable parts that can be easily tested and debugged.

## Study method parameters and their use.

In Java, a method can take zero or more parameters when it is called. Parameters are used to pass values or reference types to a method. Method parameters are declared within the parentheses of the method signature.

A method can have multiple parameters, and each parameter is separated by a comma. Parameters can have any data type, including primitives, objects, or arrays. When a method is called, the arguments provided to the method must match the parameter types and order of the method declaration.

For example, the following method takes two integer parameters and returns their sum:

```bash
public static int add(int a, int b) {
    return a + b;
}
```

This method can be called with two integer arguments like this:

```bash
int result = add(2, 3); // result is 5
```

In addition to traditional parameters, Java also supports varargs (variable-length arguments) that allow methods to take a variable number of arguments of the same type. The syntax for varargs is to use three dots (...) after the type of the last parameter, like this:

```bash
public static int sum(int... numbers) {
    int total = 0;
    for (int n : numbers) {
        total += n;
    }
    return total;
}
```

This method can be called with any number of integer arguments, like this:

```bash
int result = sum(1, 2, 3); // result is 6
result = sum(4, 5, 6, 7); // result is 22
```

Method parameters are an essential concept in Java, as they allow methods to take inputs and produce results based on those inputs.

## Get an understanding of method scope.

In Java, method scope refers to the visibility and accessibility of variables defined within a method. The scope of a variable determines where it can be accessed and manipulated within a program.

A variable declared within a method has local scope and is only accessible within that method. It cannot be accessed or manipulated from outside the method. This means that if you define a variable within a method, it will not be visible or accessible in other methods or in the main program.

On the other hand, variables declared outside of a method have a wider scope and are accessible throughout the program. These are known as instance variables or class variables.

It is important to be aware of the scope of your variables, as accessing variables outside of their scope can result in errors and unpredictable behavior. In addition, using variables with a narrower scope can help to prevent naming conflicts and improve the readability of your code.

Here is an example of method scope in Java:

```bash
public class Example {
   public void myMethod() {
      int x = 10; // local variable with method scope
      System.out.println(x);
   }

   public static void main(String[] args) {
      Example e = new Example();
      e.myMethod();
   }
}
```

In this example, the variable x is declared within the method myMethod() and has a local scope. It can only be accessed within the method and is not visible or accessible in the main() method. When the myMethod() is called, it prints the value of x, which is 10, to the console.

## Study method overloading and overriding.

In Java, it is possible to have multiple methods with the same name, but with different parameters or return types. This is known as method overloading.

Method overriding occurs when a subclass provides a specific implementation for a method that is already defined in its superclass.

Both method overloading and overriding allow for more flexibility in designing programs and can improve code readability and maintainability.

When a method is called, the Java Virtual Machine determines which method to execute based on the number, types, and order of the parameters passed to it.

For example, we can have two methods with the same name, one that takes an integer parameter and another that takes a string parameter. When we call the method with an integer argument, the first method will be executed, and when we call it with a string argument, the second method will be executed.

Overriding allows subclasses to provide their own implementation of methods inherited from their parent class. This is useful when we want to customize the behavior of a method in a subclass.

In summary, method overloading allows us to define multiple methods with the same name but different parameters, while method overriding allows us to provide a specific implementation for a method that is already defined in a superclass.

## Learn the difference between parameters and arguments.

In Java, the terms "parameters" and "arguments" are often used interchangeably, but they have different meanings.

A parameter is a variable defined in a method's signature. It is a placeholder for the actual value that will be passed into the method when it is called.

An argument is the actual value that is passed to the method when it is called. It is the value that will be assigned to the parameter in the method.

For example, consider the following method:

```bash
public void printName(String name) {
    System.out.println("Hello, " + name + "!");
}
```

In this method, name is a parameter. It is a variable that will hold the value of the argument passed to the method.

When we call the method, we pass an argument for the name parameter:

```bash
printName("Alice");
```

In this case, the argument is the String "Alice". It is passed to the printName method and assigned to the name parameter.

In summary, parameters are the placeholders for values that will be passed to a method, while arguments are the actual values that are passed to the method.
