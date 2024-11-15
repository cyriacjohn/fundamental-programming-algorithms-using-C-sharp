# fundamental-programming-algorithms-using-C-

A collection of C# code snippets demonstrating fundamental programming concepts and common algorithms.

---

## Table of Contents

1. **Basic Arithmetic Operations**
   - [Sum of Two Numbers](#sum-of-two-numbers)
   - [Sum and Product of Digits of a Number](#sum-and-product-of-digits-of-a-number)

2. **String Handling**
   - [Read and Display String Input](#read-and-display-string-input)
   - [Concatenate First and Last Name](#concatenate-first-and-last-name)
   - [Reverse Each Word in a Sentence](#reverse-each-word-in-a-sentence)
   - [Duplicate Characters in a String](#duplicate-characters-in-a-string)

3. **Number Handling**
   - [Read and Display Integer](#read-and-display-integer)
   - [Number of Digits in a Number](#number-of-digits-in-a-number)
   - [Reverse of a Number](#reverse-of-a-number)
   - [Palindrome Check for a Number](#palindrome-check-for-a-number)
   - [Armstrong Number Check](#armstrong-number-check)

4. **Factorials and Combinatorics**
   - [Factorial of a Number (Using for loop)](#factorial-of-a-number-using-for-loop)
   - [Factorial of a Number (Using Recursive Function)](#factorial-of-a-number-using-recursive-function)

5. **Fibonacci Series**
   - [Generate Fibonacci Series](#generate-fibonacci-series)

6. **Prime Numbers**
   - [Check Prime Number](#check-prime-number)
   - [Prime Numbers up to N](#prime-numbers-up-to-n)

7. **Conditional Statements**
   - [Largest of Two Numbers (Using If-Else)](#largest-of-two-numbers-using-if-else)
   - [Largest of Three Numbers (Using Nested If)](#largest-of-three-numbers-using-nested-if)

8. **Loops and Iterations**
   - [Print First N Natural Numbers](#print-first-n-natural-numbers)
   - [Swap Two Variables (Without Third Variable)](#swap-two-variables-without-third-variable)

---

## Code Snippets

### Sum of Two Numbers
Adds two integers and displays the result.
```csharp
class A {
    public static void Main() {
        int x = 10, y = 20, s = 0;
        s = x + y;
        Console.WriteLine("Sum: " + s);
        Console.ReadKey();
    }
}
```

### Sum and Product of Digits of a Number
Calculates and displays the sum and product of digits of a number.

```csharp
class A {
    public static void Main() {
        int num = 1234, sum = 0, product = 1;
        while (num > 0) {
            int digit = num % 10;
            sum += digit;
            product *= digit;
            num /= 10;
        }
        Console.WriteLine("Sum: " + sum + ", Product: " + product);
        Console.ReadKey();
    }
}
```

### Read and Display String Input
Reads a string input from the user and displays it.

```csharp
class A {
    public static void Main() {
        Console.WriteLine("Enter a string: ");
        string s = Console.ReadLine();
        Console.WriteLine("The string is: " + s);
        Console.ReadKey();
    }
}
```

### Concatenate First and Last Name
Reads first and last name and concatenates them.

```csharp
class A {
    public static void Main() {
        Console.WriteLine("Enter first name: ");
        string firstName = Console.ReadLine();
        Console.WriteLine("Enter last name: ");
        string lastName = Console.ReadLine();
        Console.WriteLine("Full Name: " + firstName + " " + lastName);
        Console.ReadKey();
    }
}
```

### Reverse Each Word in a Sentence
Reverses the characters in each word of a sentence.

```csharp
class A {
    public static void Main() {
        string sentence = "Hello World";
        string[] words = sentence.Split(' ');
        for (int i = 0; i < words.Length; i++) {
            char[] charArray = words[i].ToCharArray();
            Array.Reverse(charArray);
            words[i] = new string(charArray);
        }
        Console.WriteLine(String.Join(" ", words));
        Console.ReadKey();
    }
}
```

### Duplicate Characters in a String
Identifies and displays duplicate characters in a string.

```csharp
class A {
    public static void Main() {
        string s = "programming";
        var duplicates = new HashSet<char>();
        var seen = new HashSet<char>();
        foreach (char c in s) {
            if (!seen.Add(c)) duplicates.Add(c);
        }
        Console.WriteLine("Duplicate characters: " + string.Join(", ", duplicates));
        Console.ReadKey();
    }
}
```

### Read and Display Integer
Reads an integer input and displays it.

```csharp
class A {
    public static void Main() {
        Console.WriteLine("Enter an integer: ");
        int number = int.Parse(Console.ReadLine());
        Console.WriteLine("The integer is: " + number);
        Console.ReadKey();
    }
}
```

### Number of Digits in a Number
Counts the digits in an integer.

```csharp
class A {
    public static void Main() {
        int num = 12345;
        int count = 0;
        while (num != 0) {
            num /= 10;
            count++;
        }
        Console.WriteLine("Number of digits: " + count);
        Console.ReadKey();
    }
}
```

### Reverse of a Number
Reverses the digits of a number.

```csharp
class A {
    public static void Main() {
        int num = 12345, reversed = 0;
        while (num != 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }
        Console.WriteLine("Reversed number: " + reversed);
        Console.ReadKey();
    }
}
```

### Palindrome Check for a Number
Checks if a number is a palindrome.

```csharp
class A {
    public static void Main() {
        int num = 121, temp = num, reversed = 0;
        while (temp != 0) {
            int digit = temp % 10;
            reversed = reversed * 10 + digit;
            temp /= 10;
        }
        Console.WriteLine(num == reversed ? "Palindrome" : "Not a palindrome");
        Console.ReadKey();
    }
}
```

### Armstrong Number Check
Verifies if a number is an Armstrong number.

```csharp
class A {
    public static void Main() {
        int num = 153, sum = 0, temp = num;
        while (temp != 0) {
            int digit = temp % 10;
            sum += digit * digit * digit;
            temp /= 10;
        }
        Console.WriteLine(num == sum ? "Armstrong number" : "Not an Armstrong number");
        Console.ReadKey();
    }
}
```

### Factorial of a Number (Using for loop)
Calculates the factorial using a loop.

```csharp
class A {
    public static void Main() {
        int num = 5, fact = 1;
        for (int i = 1; i <= num; i++) fact *= i;
        Console.WriteLine("Factorial: " + fact);
        Console.ReadKey();
    }
}
```

### Factorial of a Number (Using Recursive Function)
Calculates the factorial using a recursive function.

```csharp
class A {
    static int Factorial(int num) {
        return (num == 1) ? 1 : num * Factorial(num - 1);
    }
    public static void Main() {
        Console.WriteLine("Factorial: " + Factorial(5));
        Console.ReadKey();
    }
}
```

### Generate Fibonacci Series
Generates the Fibonacci sequence up to a given limit.

```csharp
class A {
    public static void Main() {
        int limit = 10, a = 0, b = 1, temp;
        Console.Write("Fibonacci series: " + a + " " + b);
        for (int i = 2; i < limit; i++) {
            temp = a + b;
            Console.Write(" " + temp);
            a = b;
            b = temp;
        }
        Console.ReadKey();
    }
}
```

### Check Prime Number
Determines if a number is prime.

```csharp
class A {
    public static void Main() {
        int num = 29;
        bool isPrime = true;
        for (int i = 2; i <= Math.Sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        Console.WriteLine(isPrime ? "Prime number" : "Not a prime number");
        Console.ReadKey();
    }
}
```

### Prime Numbers up to N
Displays all prime numbers up to a specified limit.

```csharp
class A {
    public static void Main() {
        int limit = 20;
        Console.Write("Prime numbers up to " + limit + ": ");
        for (int num = 2; num <= limit; num++) {
            bool isPrime = true;
            for (int i = 2; i <= Math.Sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
            if (isPrime) Console.Write(num + " ");
        }
        Console.ReadKey();
    }
}
```

### Largest of Two Numbers (Using If-Else)
Determines the larger of two numbers using if-else.

```csharp
class A {
    public static void Main() {
        int a = 10, b = 20;
        Console.WriteLine(a > b ? "A is larger" : "B is larger");
        Console.ReadKey();
    }
}
```

### Largest of Three Numbers (Using Nested If)
Determines the largest of three numbers using nested if statements.

```csharp
class A {
    public static void Main() {
        int a = 10, b = 20, c = 30;
        if (a > b && a > c) Console.WriteLine("A is the largest");
        else if (b > a && b > c) Console.WriteLine("B is the largest");
        else Console.WriteLine("C is the largest");
        Console.ReadKey();
    }
}
```

### Print First N Natural Numbers
Prints the first N natural numbers.

```csharp
class A {
    public static void Main() {
        int n = 10;
        for (int i = 1; i <= n; i++) Console.Write(i + " ");
        Console.ReadKey();
    }
}
```

### Swap Two Variables (Without Third Variable)
Swaps two variables without using a third variable.

```csharp
class A {
    public static void Main() {
        int a = 5, b = 10;
        a = a + b;
        b = a - b;
        a = a - b;
        Console.WriteLine("After swap, a = " + a + ", b = " + b);
        Console.ReadKey();
    }
}
```

