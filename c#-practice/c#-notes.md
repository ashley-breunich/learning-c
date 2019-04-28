# C# Notes 

## The Basics

### Console.WriteLine()
Is a command that prints text to a console. Whatever is in between the parentheses will be printed to the console!

### Accepting User Input

```
Console.WriteLine("How old are you?");
string input = Console.ReadLine();
Console.WriteLine($"You are {input} years old!");
```
* Console.ReadLine() - The computer waits for the user to type something in the console.

##### The word input represents a variable 

##### dotnet run (how to run a program in dotnet tutorial)

### Why C#?

* C# technologies are FAST 
* the C# community is large
* C# is employable 

## Data Types

* C# is _strongly-typed_, meaning it requires the developer to specify the data types they are using. 
    * It is also _statically-typed_, meaning it will check that we used the correct types before the program even runs. 
    * These features are important because they allow us to write scalable code with FEWER bugs. 

* Common data types:
    1. int - whole numbers
    2. double - decimal numbers
    3. char - single characters
    4. string - string of characters
    5. bool - booleans

_Everytime you declare a variable, you have to specify what kind of data type that variable is going to hold._

### Converting Data Types 
* Data Type Conversion - Because variables have to be strictly typed, there may be some circumstances where we want to change the type of data a variable is storing. 
    * Implicit Conversion - This happens automatically if no data will be lost in the conversion. That’s why it’s possible to convert an int (which can hold less data) to a double (which can hold more), but not the other way around.
    * Explicit Conversion - This requires a cast operator to convert a data type into another one. So if we do want to convert a double to an int, we could use the operator (int).

    ```
    double myDouble = 3.2;

    // Round myDouble to the nearest whole number
    int myInt = (int)myDouble;
    ```

    _You can also use built-in methods like, Convert.ToString or Convert.ToDouble. Read documentation on built-in methods [here](https://docs.microsoft.com/en-us/dotnet/api/system.convert?view=netframework-4.7.2)._

    * One example of when we have to use conversions is when we ask a user to input a numerical value. Even if that value is an integer or a decimal, Console.ReadLine() will always return a string.
        * NOTE: It is not possible to implicitly convert a string into an int (or vice versa) in C#.
        * Convert.ToInt32(String) method - Converts an input string to an int.

How to tell which type a variable is:
```
  Type type = 123.45.GetType();
  // Outputs: The type associated with the variable.
  Console.WriteLine(type);
```

#### Write() vs WriteLine() Methods:

* The Write () method outputs one or more values to the screen without a new line character.

* The WriteLine() always appends a new line character to the end of the string. this means any subsequent output will start on a new line.

#### PRACTICE:

```
// converts boolean to string 
bool isFalse = false;
Console.WriteLine(isFalse.ToString());
      
// converts a string to a list of chars
string sentence = "My name is Ashley";  
char[] array = sentence.ToCharArray();  
for(int i = 0; i < array.Length; i++) {
    char letter = array[i];
    Console.Write("Letter: ");
    Console.WriteLine(letter);
}
```
