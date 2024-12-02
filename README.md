Here’s a list of **50 programming questions** ranging from basic to intermediate level. These questions focus on developing programming logic, data structures, algorithms, and problem-solving skills, suitable for most programming tests:

---

### **Basic Level**
1. Write a program to check if a number is even or odd.
2. Print the Fibonacci sequence up to `n` terms.
3. Reverse a given string.
4. Find the largest and smallest numbers in a list.
5. Check if a given string is a palindrome.
6. Implement a program to calculate the factorial of a number.
7. Write a program to count vowels and consonants in a string.
8. Calculate the sum of digits of a number.
9. Write a program to check if a number is prime.
10. Swap two variables without using a third variable.
11. Write a program to find the greatest of three numbers.
12. Print the multiplication table for a given number.
13. Find the second largest number in a list.
14. Write a program to sort an array of integers in ascending order.
15. Check if a number is an Armstrong number.
16. Write a program to count the number of words in a sentence.
17. Implement a program to merge two sorted arrays.
18. Write a program to find the GCD of two numbers.
19. Write a program to convert decimal to binary.
20. Generate a pattern of stars (`*`) in a pyramid shape.

---

### **Intermediate Level**
21. Write a program to implement binary search.
22. Implement a basic calculator supporting addition, subtraction, multiplication, and division.
23. Write a program to remove duplicates from a list.
24. Implement the insertion sort algorithm.
25. Write a program to find the maximum sum of a contiguous subarray (Kadane's Algorithm).
26. Implement a function to check if two strings are anagrams.
27. Write a program to find the frequency of each character in a string.
28. Reverse a linked list (iteratively or recursively).
29. Implement a stack using arrays or linked lists.
30. Implement a queue using stacks.
31. Write a program to find the missing number in an array of size `n` containing numbers from `1` to `n`.
32. Check if a matrix is symmetric.
33. Write a program to calculate the power of a number using recursion.
34. Implement a program to find the first non-repeating character in a string.
35. Write a program to rotate an array by `k` positions.
36. Implement a function to find the longest common prefix in an array of strings.
37. Write a program to implement a basic LRU Cache.
38. Flatten a nested list into a single-level list.
39. Write a program to find the intersection of two arrays.
40. Implement a binary tree and perform in-order, pre-order, and post-order traversal.

---

### **Advanced Intermediate Logic**
41. Write a program to determine if a given Sudoku solution is valid.
42. Solve the N-Queens problem.
43. Implement Dijkstra's algorithm for shortest path.
44. Write a program to check if a graph is bipartite.
45. Implement depth-first search (DFS) and breadth-first search (BFS) for a graph.
46. Write a program to find all permutations of a string.
47. Implement a function to find the longest palindromic substring in a string.
48. Write a program to solve the "Coin Change Problem" using dynamic programming.
49. Implement the Merge Sort algorithm.
50. Write a program to detect and remove a cycle in a linked list.

---


### **1. Check if a Number is Even or Odd**
**Algorithm:**
1. Input the number.
2. Use the modulus operator `%` to check divisibility by 2.
3. If `num % 2 == 0`, it's even; otherwise, it's odd.

**Time Complexity:**  
O(1) (constant time) because it involves only a single modulus operation.

**Code:**
```java
public class EvenOdd {
    public static void main(String[] args) {
        int num = 5; // Example input
        if (num % 2 == 0) {
            System.out.println(num + " is Even");
        } else {
            System.out.println(num + " is Odd");
        }
    }
}
```

**Output:**  
`5 is Odd`

---

### **2. Print Fibonacci Sequence**
**Algorithm:**
1. Input `n` (number of terms).
2. Start with `a = 0` and `b = 1`.
3. Print `a` and `b`, then calculate the next term as `c = a + b`.
4. Update `a = b` and `b = c`, and repeat for `n-2` iterations.

**Time Complexity:**  
O(n) (linear time) because we iterate `n` times.

**Code:**
```java
public class Fibonacci {
    public static void main(String[] args) {
        int n = 7; // Example input
        int a = 0, b = 1, c;
        System.out.print(a + " " + b);
        for (int i = 2; i < n; i++) {
            c = a + b;
            System.out.print(" " + c);
            a = b;
            b = c;
        }
    }
}
```

**Output:**  
`0 1 1 2 3 5 8`

---

### **3. Reverse a String**
**Algorithm:**
1. Input the string.
2. Traverse the string from end to start.
3. Append each character to a new string.

**Time Complexity:**  
O(n) (linear time) because we traverse the string once.

**Code:**
```java
public class ReverseString {
    public static void main(String[] args) {
        String str = "Hello"; // Example input
        String reversed = "";
        for (int i = str.length() - 1; i >= 0; i--) {
            reversed += str.charAt(i);
        }
        System.out.println("Reversed String: " + reversed);
    }
}
```

**Output:**  
`Reversed String: olleH`

---

### **4. Find Largest and Smallest in an Array**
**Algorithm:**
1. Initialize `max` and `min` to the first element.
2. Traverse the array.
3. Update `max` if the current element is greater.
4. Update `min` if the current element is smaller.

**Time Complexity:**  
O(n) because we traverse the array once.

**Code:**
```java
public class MinMaxArray {
    public static void main(String[] args) {
        int[] arr = {3, 5, 7, 2, 8}; // Example input
        int max = arr[0], min = arr[0];
        for (int num : arr) {
            if (num > max) max = num;
            if (num < min) min = num;
        }
        System.out.println("Max: " + max + ", Min: " + min);
    }
}
```

**Output:**  
`Max: 8, Min: 2`

---

### **5. Check if a String is a Palindrome**
**Algorithm:**
1. Convert the string to lowercase.
2. Compare the string with its reverse.

**Time Complexity:**  
O(n) because we traverse the string once.

**Code:**
```java
public class Palindrome {
    public static void main(String[] args) {
        String str = "Madam"; // Example input
        String lowerStr = str.toLowerCase();
        String reversed = new StringBuilder(lowerStr).reverse().toString();
        if (lowerStr.equals(reversed)) {
            System.out.println(str + " is a Palindrome");
        } else {
            System.out.println(str + " is not a Palindrome");
        }
    }
}
```

**Output:**  
`Madam is a Palindrome`

---

### **6. Calculate the Factorial of a Number**
**Algorithm:**
1. Input the number.
2. Initialize `fact = 1`.
3. Multiply `fact` by numbers from 1 to `n`.

**Time Complexity:**  
O(n) because we iterate `n` times.

**Code:**
```java
public class Factorial {
    public static void main(String[] args) {
        int n = 5; // Example input
        int fact = 1;
        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        System.out.println("Factorial of " + n + " is " + fact);
    }
}
```

**Output:**  
`Factorial of 5 is 120`

---

### **7. Count Vowels and Consonants**
**Algorithm:**
1. Traverse the string.
2. Check each character; if it’s a vowel, increment the vowel count, otherwise increment the consonant count.

**Time Complexity:**  
O(n) because we traverse the string once.

**Code:**
```java
public class VowelConsonant {
    public static void main(String[] args) {
        String str = "HelloWorld"; // Example input
        int vowels = 0, consonants = 0;
        str = str.toLowerCase();
        for (char c : str.toCharArray()) {
            if ("aeiou".indexOf(c) != -1) vowels++;
            else if (Character.isLetter(c)) consonants++;
        }
        System.out.println("Vowels: " + vowels + ", Consonants: " + consonants);
    }
}
```

**Output:**  
`Vowels: 3, Consonants: 7`

---

### **8. Sum of Digits of a Number**
**Algorithm:**
1. Input the number.
2. Extract each digit using `% 10`.
3. Add the digit to the sum and divide the number by 10.

**Time Complexity:**  
O(d) (where `d` is the number of digits).

**Code:**
```java
public class SumOfDigits {
    public static void main(String[] args) {
        int num = 1234; // Example input
        int sum = 0;
        while (num > 0) {
            sum += num % 10;
            num /= 10;
        }
        System.out.println("Sum of Digits: " + sum);
    }
}
```

**Output:**  
`Sum of Digits: 10`

---

### **9. Check if a Number is Prime**
**Algorithm:**
1. If `n <= 1`, it's not prime.
2. Check divisibility from `2` to `sqrt(n)`.

**Time Complexity:**  
O(√n) because we only check up to `sqrt(n)`.

**Code:**
```java
public class PrimeCheck {
    public static void main(String[] args) {
        int num = 29; // Example input
        boolean isPrime = true;
        if (num <= 1) isPrime = false;
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                isPrime = false;
                break;
            }
        }
        System.out.println(num + " is Prime: " + isPrime);
    }
}
```

**Output:**  
`29 is Prime: true`

---

### **10. Swap Two Numbers Without a Temp Variable**
**Algorithm:**
1. Use arithmetic operations (addition and subtraction).

**Time Complexity:**  
O(1) because it’s a constant-time operation.

**Code:**
```java
public class SwapNumbers {
    public static void main(String[] args) {
        int a = 5, b = 3; // Example inputs
        a = a + b;
        b = a - b;
        a = a - b;
        System.out.println("After Swap: a = " + a + ", b = " + b);
    }
}
```

**Output:**  
`After Swap: a = 3, b = 5`

---


### **11. Find the Greatest of Three Numbers**
**Algorithm:**
1. Input the three numbers.
2. Compare the numbers using `if` conditions.
3. Output the greatest number.

**Time Complexity:**  
O(1) because we only compare three numbers.

**Code:**
```java
public class GreatestOfThree {
    public static void main(String[] args) {
        int a = 10, b = 20, c = 30; // Example input
        int greatest = (a > b) ? (a > c ? a : c) : (b > c ? b : c);
        System.out.println("Greatest number is: " + greatest);
    }
}
```

**Output:**  
`Greatest number is: 30`

---

### **12. Print the Multiplication Table for a Given Number**
**Algorithm:**
1. Input the number.
2. Loop through numbers from 1 to 10.
3. Multiply and print the result.

**Time Complexity:**  
O(1) because it's a fixed number of operations.

**Code:**
```java
public class MultiplicationTable {
    public static void main(String[] args) {
        int num = 5; // Example input
        for (int i = 1; i <= 10; i++) {
            System.out.println(num + " * " + i + " = " + (num * i));
        }
    }
}
```

**Output:**  
```
5 * 1 = 5
5 * 2 = 10
5 * 3 = 15
5 * 4 = 20
5 * 5 = 25
5 * 6 = 30
5 * 7 = 35
5 * 8 = 40
5 * 9 = 45
5 * 10 = 50
```

---

### **13. Find the Second Largest Number in an Array**
**Algorithm:**
1. Input the array.
2. Traverse the array to find the largest and second-largest numbers.

**Time Complexity:**  
O(n) because we only traverse the array once.

**Code:**
```java
public class SecondLargest {
    public static void main(String[] args) {
        int[] arr = {1, 3, 4, 5, 2}; // Example input
        int max = Integer.MIN_VALUE, secondMax = Integer.MIN_VALUE;
        for (int num : arr) {
            if (num > max) {
                secondMax = max;
                max = num;
            } else if (num > secondMax && num != max) {
                secondMax = num;
            }
        }
        System.out.println("Second largest number is: " + secondMax);
    }
}
```

**Output:**  
`Second largest number is: 4`

---

### **14. Sort an Array in Ascending Order**
**Algorithm:**
1. Use the `Arrays.sort()` method to sort the array.

**Time Complexity:**  
O(n log n) because `Arrays.sort()` uses a variant of the Merge Sort or Tim Sort.

**Code:**
```java
import java.util.Arrays;

public class SortArray {
    public static void main(String[] args) {
        int[] arr = {5, 2, 9, 1, 5, 6}; // Example input
        Arrays.sort(arr);
        System.out.println("Sorted array: " + Arrays.toString(arr));
    }
}
```

**Output:**  
`Sorted array: [1, 2, 5, 5, 6, 9]`

---

### **15. Check if a Number is an Armstrong Number**
**Algorithm:**
1. Input the number.
2. Find the number of digits in the number.
3. Calculate the sum of each digit raised to the power of the number of digits.
4. Compare the sum to the original number.

**Time Complexity:**  
O(d) (where `d` is the number of digits).

**Code:**
```java
public class ArmstrongNumber {
    public static void main(String[] args) {
        int num = 153; // Example input
        int originalNum = num;
        int sum = 0;
        int digits = String.valueOf(num).length();
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits);
            num /= 10;
        }
        if (sum == originalNum) {
            System.out.println(originalNum + " is an Armstrong number.");
        } else {
            System.out.println(originalNum + " is not an Armstrong number.");
        }
    }
}
```

**Output:**  
`153 is an Armstrong number.`

---

### **16. Count the Number of Words in a Sentence**
**Algorithm:**
1. Input the sentence.
2. Split the string by spaces and count the resulting array's length.

**Time Complexity:**  
O(n) because we are splitting the string, which involves iterating over the string.

**Code:**
```java
public class WordCount {
    public static void main(String[] args) {
        String sentence = "This is a test sentence"; // Example input
        String[] words = sentence.split(" ");
        System.out.println("Number of words: " + words.length);
    }
}
```

**Output:**  
`Number of words: 5`

---

### **17. Merge Two Sorted Arrays**
**Algorithm:**
1. Input the two sorted arrays.
2. Use two pointers to traverse both arrays and merge them in sorted order.

**Time Complexity:**  
O(n + m) where `n` and `m` are the lengths of the two arrays.

**Code:**
```java
import java.util.Arrays;

public class MergeArrays {
    public static void main(String[] args) {
        int[] arr1 = {1, 3, 5}; // Example input
        int[] arr2 = {2, 4, 6};
        int[] merged = new int[arr1.length + arr2.length];
        int i = 0, j = 0, k = 0;
        while (i < arr1.length && j < arr2.length) {
            if (arr1[i] < arr2[j]) {
                merged[k++] = arr1[i++];
            } else {
                merged[k++] = arr2[j++];
            }
        }
        while (i < arr1.length) {
            merged[k++] = arr1[i++];
        }
        while (j < arr2.length) {
            merged[k++] = arr2[j++];
        }
        System.out.println("Merged Array: " + Arrays.toString(merged));
    }
}
```

**Output:**  
`Merged Array: [1, 2, 3, 4, 5, 6]`

---

### **18. Find the GCD of Two Numbers**
**Algorithm:**
1. Use the Euclidean algorithm:
   - Repeatedly divide the larger number by the smaller one until the remainder is 0.
   - The last non-zero remainder is the GCD.

**Time Complexity:**  
O(log(min(a, b))) because the Euclidean algorithm has logarithmic complexity.

**Code:**
```java
public class GCD {
    public static void main(String[] args) {
        int a = 56, b = 98; // Example input
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        System.out.println("GCD: " + a);
    }
}
```

**Output:**  
`GCD: 14`

---

### **19. Convert Decimal to Binary**
**Algorithm:**
1. Input the decimal number.
2. Repeatedly divide by 2 and record the remainder.
3. Append remainders in reverse order.

**Time Complexity:**  
O(log n) because the number of divisions is proportional to the logarithm of the number.

**Code:**
```java
public class DecimalToBinary {
    public static void main(String[] args) {
        int num = 10; // Example input
        StringBuilder binary = new StringBuilder();
        while (num > 0) {
            binary.insert(0, num % 2);
            num /= 2;
        }
        System.out.println("Binary: " + binary.toString());
    }
}
```

**Output:**  
`Binary: 1010`

---

### **20. Generate a Star Pattern (Pyramid Shape)**
**Algorithm:**
1. Input the number of rows.
2. Print spaces and stars in each row to form a pyramid shape.

**Time Complexity:**  
O(n) because we print each row once.

**Code:**
```java
public class StarPattern {
    public static void main(String[] args) {
        int rows = 5; // Example input
        for (int i = 1; i <= rows; i++) {
            for (int j = i; j < rows; j++) {
                System.out.print(" ");
            }
            for (int k = 1; k <= (2 * i - 1); k++) {
                System.out.print("*");
            }
            System.out.println();
        }
    }
}
```

**Output:**  
```
    *
   ***
  *****
 *******
*********
```

---




These problems will strengthen your foundational and intermediate-level programming skills. You can use any programming language of your choice, such as Python, Java, C++, or JavaScript, to solve these. Let me know if you’d like detailed solutions or hints for any of these!
