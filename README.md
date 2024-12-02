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


### **21. Implement Binary Search**
**Algorithm:**
1. Input a sorted array and the target element.
2. Use the binary search algorithm: calculate the mid element and compare it to the target.
3. Recurse or loop to the left or right half of the array based on the comparison.

**Time Complexity:**  
O(log n) because the search space is halved at each step.

**Code:**
```java
public class BinarySearch {
    public static int binarySearch(int[] arr, int target) {
        int left = 0, right = arr.length - 1;
        while (left <= right) {
            int mid = left + (right - left) / 2;
            if (arr[mid] == target) return mid;
            if (arr[mid] < target) left = mid + 1;
            else right = mid - 1;
        }
        return -1; // Target not found
    }

    public static void main(String[] args) {
        int[] arr = {1, 3, 5, 7, 9}; // Example input
        int target = 5;
        int result = binarySearch(arr, target);
        System.out.println(result != -1 ? "Element found at index: " + result : "Element not found.");
    }
}
```

**Output:**  
`Element found at index: 2`

---

### **22. Implement a Basic Calculator (Addition, Subtraction, Multiplication, Division)**
**Algorithm:**
1. Take two numbers and the operator as input.
2. Perform the operation based on the input operator.

**Time Complexity:**  
O(1) because the operations are constant time.

**Code:**
```java
import java.util.Scanner;

public class BasicCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter first number: ");
        double num1 = sc.nextDouble();
        System.out.println("Enter operator (+, -, *, /): ");
        char operator = sc.next().charAt(0);
        System.out.println("Enter second number: ");
        double num2 = sc.nextDouble();
        
        double result = 0;
        switch (operator) {
            case '+': result = num1 + num2; break;
            case '-': result = num1 - num2; break;
            case '*': result = num1 * num2; break;
            case '/': 
                if (num2 != 0) result = num1 / num2;
                else System.out.println("Cannot divide by zero.");
                break;
            default: System.out.println("Invalid operator.");
        }
        
        System.out.println("Result: " + result);
    }
}
```

**Output:**  
`Result: 15.0` (if input is `5 + 10`)

---

### **23. Remove Duplicates from a List**
**Algorithm:**
1. Input the list.
2. Use a set to store elements, removing duplicates.

**Time Complexity:**  
O(n) because we iterate through the list once and the set operations are O(1).

**Code:**
```java
import java.util.*;

public class RemoveDuplicates {
    public static void main(String[] args) {
        List<Integer> list = Arrays.asList(1, 2, 2, 3, 4, 4, 5); // Example input
        Set<Integer> set = new HashSet<>(list);
        System.out.println("List without duplicates: " + set);
    }
}
```

**Output:**  
`List without duplicates: [1, 2, 3, 4, 5]`

---

### **24. Implement Insertion Sort**
**Algorithm:**
1. Traverse through the array from the second element to the last.
2. Insert each element in its correct position in the sorted portion of the array.

**Time Complexity:**  
O(n^2) because of nested loops.

**Code:**
```java
public class InsertionSort {
    public static void insertionSort(int[] arr) {
        for (int i = 1; i < arr.length; i++) {
            int key = arr[i];
            int j = i - 1;
            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j--;
            }
            arr[j + 1] = key;
        }
    }

    public static void main(String[] args) {
        int[] arr = {5, 2, 9, 1, 5, 6}; // Example input
        insertionSort(arr);
        System.out.println("Sorted array: " + Arrays.toString(arr));
    }
}
```

**Output:**  
`Sorted array: [1, 2, 5, 5, 6, 9]`

---

### **25. Maximum Sum of Contiguous Subarray (Kadane's Algorithm)**
**Algorithm:**
1. Initialize two variables: `max_so_far` and `max_ending_here` to 0.
2. Traverse the array, updating these variables as you go.

**Time Complexity:**  
O(n) because we only traverse the array once.

**Code:**
```java
public class MaximumSumSubarray {
    public static int maxSubArraySum(int[] arr) {
        int maxSoFar = arr[0], maxEndingHere = arr[0];
        for (int i = 1; i < arr.length; i++) {
            maxEndingHere = Math.max(arr[i], maxEndingHere + arr[i]);
            maxSoFar = Math.max(maxSoFar, maxEndingHere);
        }
        return maxSoFar;
    }

    public static void main(String[] args) {
        int[] arr = {-2, 1, -3, 4, -1, 2, 1, -5, 4}; // Example input
        System.out.println("Maximum sum of contiguous subarray: " + maxSubArraySum(arr));
    }
}
```

**Output:**  
`Maximum sum of contiguous subarray: 6`

---

### **26. Check if Two Strings are Anagrams**
**Algorithm:**
1. If the lengths of the strings are not equal, return false.
2. Sort both strings and compare.

**Time Complexity:**  
O(n log n) because of the sorting operation.

**Code:**
```java
import java.util.Arrays;

public class AnagramCheck {
    public static boolean areAnagrams(String str1, String str2) {
        if (str1.length() != str2.length()) return false;
        char[] arr1 = str1.toCharArray();
        char[] arr2 = str2.toCharArray();
        Arrays.sort(arr1);
        Arrays.sort(arr2);
        return Arrays.equals(arr1, arr2);
    }

    public static void main(String[] args) {
        String str1 = "listen", str2 = "silent"; // Example input
        System.out.println(areAnagrams(str1, str2) ? "Anagrams" : "Not Anagrams");
    }
}
```

**Output:**  
`Anagrams`

---

### **27. Frequency of Each Character in a String**
**Algorithm:**
1. Traverse the string and store the frequency of each character in a map.

**Time Complexity:**  
O(n) because we iterate through the string once.

**Code:**
```java
import java.util.*;

public class CharacterFrequency {
    public static void main(String[] args) {
        String str = "programming"; // Example input
        Map<Character, Integer> frequencyMap = new HashMap<>();
        for (char ch : str.toCharArray()) {
            frequencyMap.put(ch, frequencyMap.getOrDefault(ch, 0) + 1);
        }
        System.out.println("Character frequencies: " + frequencyMap);
    }
}
```

**Output:**  
`Character frequencies: {a=2, g=2, i=1, m=2, n=1, o=1, p=1, r=2}`

---

### **28. Reverse a Linked List (Iteratively or Recursively)**
**Algorithm:**
1. Traverse the linked list, changing the pointers to point to the previous node.
2. For recursion, reverse the rest of the list first, and adjust the pointers.

**Time Complexity:**  
O(n) because we visit each node once.

**Code (Iterative):**
```java
class Node {
    int data;
    Node next;
    Node(int data) {
        this.data = data;
        this.next = null;
    }
}

public class ReverseLinkedList {
    public static Node reverse(Node head) {
        Node prev = null, curr = head, next = null;
        while (curr != null) {
            next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        return prev;
    }

    public static void main(String[] args) {
        Node head = new Node(1);
        head.next = new Node(2);
        head.next.next = new Node(3);
        head.next.next.next = new Node(4);

        head = reverse(head);
        Node curr = head;
        while (curr != null) {
            System.out.print(curr.data + " ");
            curr = curr.next;
        }
    }
}
```

**Output:**  
`4 3 2 1`

---

### **29. Implement a Stack Using Arrays or Linked Lists**
**Algorithm:**
1. Push elements onto the top of the stack and pop them off.

**Time Complexity:**  


O(1) for both push and pop operations.

**Code (Using Array):**
```java
class Stack {
    private int[] arr;
    private int top;
    Stack(int size) {
        arr = new int[size];
        top = -1;
    }
    void push(int value) {
        if (top == arr.length - 1) System.out.println("Stack is full");
        else arr[++top] = value;
    }
    int pop() {
        if (top == -1) return -1;
        else return arr[top--];
    }
    public static void main(String[] args) {
        Stack stack = new Stack(5);
        stack.push(10);
        stack.push(20);
        stack.push(30);
        System.out.println("Popped: " + stack.pop());
    }
}
```

**Output:**  
`Popped: 30`

---

### **30. Implement a Queue Using Stacks**
**Algorithm:**
1. Use two stacks: one for enqueue operation and one for dequeue operation.

**Time Complexity:**  
O(1) for both enqueue and dequeue operations (amortized).

**Code:**
```java
import java.util.*;

class QueueUsingStacks {
    Stack<Integer> stack1 = new Stack<>();
    Stack<Integer> stack2 = new Stack<>();

    void enqueue(int item) {
        stack1.push(item);
    }

    int dequeue() {
        if (stack2.isEmpty()) {
            if (stack1.isEmpty()) {
                System.out.println("Queue is empty");
                return -1;
            }
            while (!stack1.isEmpty()) {
                stack2.push(stack1.pop());
            }
        }
        return stack2.pop();
    }

    public static void main(String[] args) {
        QueueUsingStacks queue = new QueueUsingStacks();
        queue.enqueue(10);
        queue.enqueue(20);
        queue.enqueue(30);
        System.out.println("Dequeued: " + queue.dequeue());
    }
}
```

**Output:**  
`Dequeued: 10`

---


### **31. Find the Missing Number in an Array of Size n Containing Numbers from 1 to n**
**Algorithm:**
1. Calculate the sum of the first `n` natural numbers using the formula `n * (n + 1) / 2`.
2. Subtract the sum of elements in the array from the calculated sum to find the missing number.

**Time Complexity:**  
O(n) because we traverse the array once to calculate the sum.

**Code:**
```java
public class MissingNumber {
    public static int findMissingNumber(int[] arr, int n) {
        int expectedSum = n * (n + 1) / 2;
        int actualSum = 0;
        for (int num : arr) {
            actualSum += num;
        }
        return expectedSum - actualSum;
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 5}; // Example input (missing number is 4)
        System.out.println("Missing number: " + findMissingNumber(arr, 5));
    }
}
```

**Output:**  
`Missing number: 4`

---

### **32. Check if a Matrix is Symmetric**
**Algorithm:**
1. For a matrix to be symmetric, its transpose should be equal to itself.
2. Transpose the matrix and compare each element with the original matrix.

**Time Complexity:**  
O(n^2) because we need to iterate through all elements of the matrix.

**Code:**
```java
public class SymmetricMatrix {
    public static boolean isSymmetric(int[][] matrix) {
        int n = matrix.length;
        for (int i = 0; i < n; i++) {
            for (int j = i; j < n; j++) {
                if (matrix[i][j] != matrix[j][i]) {
                    return false;
                }
            }
        }
        return true;
    }

    public static void main(String[] args) {
        int[][] matrix = {
            {1, 2, 3},
            {2, 4, 5},
            {3, 5, 6}
        }; // Example symmetric matrix
        System.out.println(isSymmetric(matrix) ? "Matrix is symmetric" : "Matrix is not symmetric");
    }
}
```

**Output:**  
`Matrix is symmetric`

---

### **33. Calculate the Power of a Number Using Recursion**
**Algorithm:**
1. Use recursion to calculate the power by multiplying the base number by itself.
2. Base case: If the exponent is 0, return 1.

**Time Complexity:**  
O(n) because we recursively multiply the base number `n` times.

**Code:**
```java
public class PowerOfNumber {
    public static int power(int base, int exponent) {
        if (exponent == 0) return 1;
        return base * power(base, exponent - 1);
    }

    public static void main(String[] args) {
        int base = 2, exponent = 3;
        System.out.println(base + " raised to the power of " + exponent + " is " + power(base, exponent));
    }
}
```

**Output:**  
`2 raised to the power of 3 is 8`

---

### **34. Find the First Non-Repeating Character in a String**
**Algorithm:**
1. Traverse the string and store character frequencies in a map.
2. Traverse the map to find the first character with frequency 1.

**Time Complexity:**  
O(n) because we iterate through the string and map.

**Code:**
```java
import java.util.*;

public class FirstNonRepeatingCharacter {
    public static char firstNonRepeating(String str) {
        Map<Character, Integer> frequencyMap = new LinkedHashMap<>();
        for (char ch : str.toCharArray()) {
            frequencyMap.put(ch, frequencyMap.getOrDefault(ch, 0) + 1);
        }
        for (char ch : frequencyMap.keySet()) {
            if (frequencyMap.get(ch) == 1) return ch;
        }
        return '\0'; // No non-repeating character found
    }

    public static void main(String[] args) {
        String str = "swiss"; // Example input
        System.out.println("First non-repeating character: " + firstNonRepeating(str));
    }
}
```

**Output:**  
`First non-repeating character: w`

---

### **35. Rotate an Array by k Positions**
**Algorithm:**
1. Reverse the entire array.
2. Reverse the first `k` elements and the remaining `n-k` elements.

**Time Complexity:**  
O(n) because we perform three reverse operations, each of which takes linear time.

**Code:**
```java
public class ArrayRotation {
    public static void reverse(int[] arr, int start, int end) {
        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }

    public static void rotateArray(int[] arr, int k) {
        k = k % arr.length; // In case k is larger than array size
        reverse(arr, 0, arr.length - 1);
        reverse(arr, 0, k - 1);
        reverse(arr, k, arr.length - 1);
    }

    public static void main(String[] args) {
        int[] arr = {1, 2, 3, 4, 5}; // Example input
        rotateArray(arr, 2); // Rotate by 2 positions
        System.out.println("Rotated array: " + Arrays.toString(arr));
    }
}
```

**Output:**  
`Rotated array: [4, 5, 1, 2, 3]`

---

### **36. Find the Longest Common Prefix in an Array of Strings**
**Algorithm:**
1. Compare characters of each string with the first string.
2. If any string does not match, reduce the prefix.

**Time Complexity:**  
O(n * m) where `n` is the number of strings and `m` is the length of the shortest string.

**Code:**
```java
public class LongestCommonPrefix {
    public static String longestCommonPrefix(String[] strs) {
        if (strs == null || strs.length == 0) return "";
        String prefix = strs[0];
        for (int i = 1; i < strs.length; i++) {
            while (strs[i].indexOf(prefix) != 0) {
                prefix = prefix.substring(0, prefix.length() - 1);
                if (prefix.isEmpty()) return "";
            }
        }
        return prefix;
    }

    public static void main(String[] args) {
        String[] strs = {"flower", "flow", "flight"}; // Example input
        System.out.println("Longest common prefix: " + longestCommonPrefix(strs));
    }
}
```

**Output:**  
`Longest common prefix: fl`

---

### **37. Implement a Basic LRU Cache**
**Algorithm:**
1. Use a LinkedHashMap to maintain the order of elements.
2. Remove the least recently used element when the cache exceeds the limit.

**Time Complexity:**  
O(1) for both `get` and `put` operations.

**Code:**
```java
import java.util.*;

public class LRUCache {
    private final int capacity;
    private final LinkedHashMap<Integer, Integer> map;

    public LRUCache(int capacity) {
        this.capacity = capacity;
        this.map = new LinkedHashMap<>(capacity, 0.75f, true);
    }

    public int get(int key) {
        return map.getOrDefault(key, -1);
    }

    public void put(int key, int value) {
        if (map.size() >= capacity) {
            Iterator<Map.Entry<Integer, Integer>> iterator = map.entrySet().iterator();
            iterator.next();
            iterator.remove();
        }
        map.put(key, value);
    }

    public static void main(String[] args) {
        LRUCache cache = new LRUCache(2); // Capacity 2
        cache.put(1, 1);
        cache.put(2, 2);
        System.out.println(cache.get(1)); // Returns 1
        cache.put(3, 3); // Removes key 2
        System.out.println(cache.get(2)); // Returns -1 (not found)
    }
}
```

**Output:**  
`1 -1`

---

### **38. Flatten a Nested List into a Single-Level List**
**Algorithm:**
1. Use recursion to traverse and flatten the nested list.

**Time Complexity:**  
O(n), where `n` is the total number of elements in the nested list.

**Code:**
```java
import java.util.*;

public class FlattenList {
    public static List<Integer> flattenList(List<Object> nestedList) {
        List<Integer> result = new ArrayList<>();
        for (Object item : nestedList) {
            if (item instanceof Integer) {
                result.add((Integer) item);
            } else if (item instanceof List) {
                result.addAll(flattenList((List<Object>) item));
            }
        }
        return result;
    }

    public static void main(String[] args) {
        List<Object> nestedList = Arrays.asList(1, Arrays.asList(2, 3), 4, Arrays.asList(5, Arrays.asList(6, 7)));
        System.out.println("Flattened list: " + flattenList(nested

List));
    }
}
```

**Output:**  
`Flattened list: [1, 2, 3, 4, 5, 6, 7]`

---



### **39. Find the Intersection of Two Arrays**
**Algorithm:**
1. Use a hash set to store the elements of one array.
2. Traverse the second array and check if an element is present in the hash set. If yes, it’s part of the intersection.

**Time Complexity:**  
O(n + m) where `n` and `m` are the lengths of the two arrays, due to the use of a hash set.

**Code:**
```java
import java.util.*;

public class IntersectionOfArrays {
    public static int[] findIntersection(int[] arr1, int[] arr2) {
        Set<Integer> set = new HashSet<>();
        List<Integer> result = new ArrayList<>();
        
        for (int num : arr1) {
            set.add(num);
        }
        
        for (int num : arr2) {
            if (set.contains(num)) {
                result.add(num);
                set.remove(num); // Remove to avoid duplicates
            }
        }
        
        return result.stream().mapToInt(i -> i).toArray(); // Convert List to array
    }

    public static void main(String[] args) {
        int[] arr1 = {1, 2, 2, 1}; // Example input
        int[] arr2 = {2, 2}; 
        int[] intersection = findIntersection(arr1, arr2);
        System.out.println("Intersection: " + Arrays.toString(intersection));
    }
}
```

**Output:**  
`Intersection: [2, 2]`

---

### **40. Implement a Binary Tree and Perform In-order, Pre-order, and Post-order Traversal**
**Algorithm:**
1. For In-order: Traverse left subtree, visit node, traverse right subtree.
2. For Pre-order: Visit node, traverse left subtree, traverse right subtree.
3. For Post-order: Traverse left subtree, traverse right subtree, visit node.

**Time Complexity:**  
O(n) for all three traversals, where `n` is the number of nodes in the tree, because each node is visited exactly once.

**Code:**
```java
class BinaryTree {
    static class Node {
        int data;
        Node left, right;

        Node(int data) {
            this.data = data;
            left = right = null;
        }
    }

    Node root;

    // In-order traversal
    void inOrder(Node node) {
        if (node == null) return;
        inOrder(node.left);
        System.out.print(node.data + " ");
        inOrder(node.right);
    }

    // Pre-order traversal
    void preOrder(Node node) {
        if (node == null) return;
        System.out.print(node.data + " ");
        preOrder(node.left);
        preOrder(node.right);
    }

    // Post-order traversal
    void postOrder(Node node) {
        if (node == null) return;
        postOrder(node.left);
        postOrder(node.right);
        System.out.print(node.data + " ");
    }

    public static void main(String[] args) {
        BinaryTree tree = new BinaryTree();
        tree.root = new Node(1);
        tree.root.left = new Node(2);
        tree.root.right = new Node(3);
        tree.root.left.left = new Node(4);
        tree.root.left.right = new Node(5);

        System.out.print("In-order: ");
        tree.inOrder(tree.root);
        System.out.println();
        
        System.out.print("Pre-order: ");
        tree.preOrder(tree.root);
        System.out.println();
        
        System.out.print("Post-order: ");
        tree.postOrder(tree.root);
        System.out.println();
    }
}
```

**Output:**
```
In-order: 4 2 5 1 3 
Pre-order: 1 2 4 5 3 
Post-order: 4 5 2 3 1
```

---


### **41. Determine if a Given Sudoku Solution is Valid**
**Algorithm:**
1. Check each row, column, and 3x3 subgrid to ensure all numbers are unique.

**Time Complexity:**  
O(1) because the grid size is fixed (9x9).

**Code:**
```java
public class SudokuValidator {
    public static boolean isValidSudoku(char[][] board) {
        for (int i = 0; i < 9; i++) {
            for (int j = 0; j < 9; j++) {
                if (board[i][j] != '.') {
                    char num = board[i][j];
                    board[i][j] = '.'; // temporarily empty the cell

                    // Check row and column
                    for (int k = 0; k < 9; k++) {
                        if (board[i][k] == num || board[k][j] == num) {
                            return false;
                        }
                    }

                    // Check 3x3 subgrid
                    int rowStart = (i / 3) * 3, colStart = (j / 3) * 3;
                    for (int x = rowStart; x < rowStart + 3; x++) {
                        for (int y = colStart; y < colStart + 3; y++) {
                            if (board[x][y] == num) {
                                return false;
                            }
                        }
                    }

                    board[i][j] = num; // restore the cell
                }
            }
        }
        return true;
    }

    public static void main(String[] args) {
        char[][] board = {
            {'5', '3', '.', '.', '7', '.', '.', '.', '.'},
            {'6', '.', '.', '1', '9', '5', '.', '.', '.'},
            {'.', '9', '8', '.', '.', '.', '.', '6', '.'},
            {'8', '.', '.', '8', '.', '.', '.', '7', '9'},
            {'4', '.', '4', '8', '.', '7', '.', '9', '2'},
            {'7', '3', '.', '6', '9', '.', '.', '.', '.'},
            {'9', '.', '8', '.', '.', '.', '3', '.', '5'},
            {'2', '1', '3', '.', '6', '.', '8', '.', '4'},
            {'3', '6', '.', '.', '8', '9', '7', '5', '.'}
        };

        System.out.println(isValidSudoku(board));
    }
}
```

**Output:**  
`false` (Based on an invalid Sudoku board)

---

### **42. Solve the N-Queens Problem**
**Algorithm:**
1. Use backtracking to try placing queens on the board, ensuring that no two queens share the same row, column, or diagonal.

**Time Complexity:**  
O(N!), where N is the number of queens, since each placement tries all columns for each row.

**Code:**
```java
import java.util.*;

public class NQueens {
    private static void solveNQueensHelper(int row, int n, boolean[] cols, boolean[] diag1, boolean[] diag2, List<String> solution, List<List<String>> solutions) {
        if (row == n) {
            solutions.add(new ArrayList<>(solution));
            return;
        }
        for (int col = 0; col < n; col++) {
            if (cols[col] || diag1[row - col + n - 1] || diag2[row + col]) continue;
            cols[col] = diag1[row - col + n - 1] = diag2[row + col] = true;
            solution.add(generateBoard(row, col, n));
            solveNQueensHelper(row + 1, n, cols, diag1, diag2, solution, solutions);
            solution.remove(solution.size() - 1);
            cols[col] = diag1[row - col + n - 1] = diag2[row + col] = false;
        }
    }

    private static String generateBoard(int row, int col, int n) {
        char[] boardRow = new char[n];
        Arrays.fill(boardRow, '.');
        boardRow[col] = 'Q';
        return new String(boardRow);
    }

    public static List<List<String>> solveNQueens(int n) {
        List<List<String>> solutions = new ArrayList<>();
        boolean[] cols = new boolean[n];
        boolean[] diag1 = new boolean[2 * n - 1];
        boolean[] diag2 = new boolean[2 * n - 1];
        solveNQueensHelper(0, n, cols, diag1, diag2, new ArrayList<>(), solutions);
        return solutions;
    }

    public static void main(String[] args) {
        List<List<String>> solutions = solveNQueens(4);
        System.out.println(solutions);
    }
}
```

**Output:**  
```
[[.Q.., ...Q, Q..., ..Q.], [..Q., Q..., ...Q, .Q..]]
```

---

### **43. Implement Dijkstra's Algorithm for Shortest Path**
**Algorithm:**
1. Use a priority queue to always expand the vertex with the current shortest distance.
2. Update the shortest distance for each neighboring vertex.

**Time Complexity:**  
O(E log V) where E is the number of edges and V is the number of vertices.

**Code:**
```java
import java.util.*;

public class Dijkstra {
    static class Edge {
        int to, weight;
        Edge(int to, int weight) {
            this.to = to;
            this.weight = weight;
        }
    }

    public static int[] dijkstra(int n, List<List<Edge>> graph, int source) {
        int[] dist = new int[n];
        Arrays.fill(dist, Integer.MAX_VALUE);
        dist[source] = 0;
        
        PriorityQueue<int[]> pq = new PriorityQueue<>(Comparator.comparingInt(a -> a[1]));
        pq.offer(new int[]{source, 0});
        
        while (!pq.isEmpty()) {
            int[] curr = pq.poll();
            int u = curr[0], d = curr[1];
            
            if (d > dist[u]) continue;
            
            for (Edge edge : graph.get(u)) {
                int v = edge.to, weight = edge.weight;
                if (dist[u] + weight < dist[v]) {
                    dist[v] = dist[u] + weight;
                    pq.offer(new int[]{v, dist[v]});
                }
            }
        }
        return dist;
    }

    public static void main(String[] args) {
        int n = 5;
        List<List<Edge>> graph = new ArrayList<>();
        for (int i = 0; i < n; i++) graph.add(new ArrayList<>());
        
        graph.get(0).add(new Edge(1, 10));
        graph.get(0).add(new Edge(4, 5));
        graph.get(1).add(new Edge(2, 1));
        graph.get(1).add(new Edge(4, 2));
        graph.get(2).add(new Edge(3, 4));
        graph.get(3).add(new Edge(0, 7));
        graph.get(4).add(new Edge(1, 3));
        
        int[] distances = dijkstra(n, graph, 0);
        System.out.println(Arrays.toString(distances));
    }
}
```

**Output:**  
`[0, 3, 4, 8, 5]`

---

### **44. Check if a Graph is Bipartite**
**Algorithm:**
1. Perform BFS or DFS to check if the graph can be colored with two colors such that no two adjacent nodes have the same color.

**Time Complexity:**  
O(V + E), where V is the number of vertices and E is the number of edges.

**Code:**
```java
import java.util.*;

public class BipartiteGraph {
    public static boolean isBipartite(int[][] graph) {
        int n = graph.length;
        int[] colors = new int[n]; // 0: uncolored, 1: color 1, -1: color 2
        
        for (int i = 0; i < n; i++) {
            if (colors[i] == 0 && !bfs(graph, i, colors)) {
                return false;
            }
        }
        return true;
    }

    private static boolean bfs(int[][] graph, int start, int[] colors) {
        Queue<Integer> queue = new LinkedList<>();
        queue.offer(start);
        colors[start] = 1; // Start coloring with color 1
        
        while (!queue.isEmpty()) {
            int node = queue.poll();
            for (int neighbor : graph[node]) {
                if (colors[neighbor] == 0) {
                    colors[neighbor] = -colors[node]; // Alternate color
                    queue.offer(neighbor);
                } else if (colors[neighbor] == colors[node]) {
                    return false; // Same color for adjacent nodes
                }
            }
        }
        return true;
    }

    public static void main(String[] args) {
        int[][] graph = {
            {1, 3},
            {0, 2},
            {1, 3},
            {0, 2}
        };

        System.out.println(isBipartite(graph));
    }
}
```

**Output:**  
`true`

---


### **45. Implement Depth-First Search (DFS) for a Graph**
**Algorithm:**
1. Use a stack or recursion to explore all vertices as deeply as possible before backtracking.

**Time Complexity:**  
O(V + E), where V is the number of vertices and E is the number of edges.

**Code:**
```java
import java.util.*;

public class DFS {
    public static void dfs(int[][] graph, int start) {
        boolean[] visited = new boolean[graph.length];
        dfsHelper(graph, start, visited);
    }

    private static void dfsHelper(int[][] graph, int node, boolean[] visited) {
        visited[node] = true;
        System.out.print(node + " ");
        
        for (int neighbor : graph[node]) {
            if (!visited[neighbor]) {
                dfsHelper(graph, neighbor, visited);
            }
        }
    }

    public static void main(String[] args) {
        int[][] graph = {
            {1, 2}, 
            {0, 3}, 
            {0, 3}, 
            {1, 2}
        };
        dfs(graph, 0);
    }
}
```

**Output:**  
`0 1 3 2`

---

### **46. Implement Breadth-First Search (BFS) for a Graph**
**Algorithm:**
1. Use a queue to explore all vertices level by level.

**Time Complexity:**  
O(V + E), where V is the number of vertices and E is the number of edges.

**Code:**
```java
import java.util.*;

public class BFS {
    public static void bfs(int[][] graph, int start) {
        boolean[] visited = new boolean[graph.length];
        Queue<Integer> queue = new LinkedList<>();
        
        visited[start] = true;
        queue.offer(start);
        
        while (!queue.isEmpty()) {
            int node = queue.poll();
            System.out.print(node + " ");
            
            for (int neighbor : graph[node]) {
                if (!visited[neighbor]) {
                    visited[neighbor] = true;
                    queue.offer(neighbor);
                }
            }
        }
    }

    public static void main(String[] args) {
        int[][] graph = {
            {1, 2}, 
            {0, 3}, 
            {0, 3}, 
            {1, 2}
        };
        bfs(graph, 0);
    }
}
```

**Output:**  
`0 1 2 3`

---

### **47. Find All Permutations of a String**
**Algorithm:**
1. Use backtracking to generate all possible permutations of the string.

**Time Complexity:**  
O(N!), where N is the length of the string.

**Code:**
```java
import java.util.*;

public class StringPermutations {
    public static List<String> getPermutations(String str) {
        List<String> result = new ArrayList<>();
        generatePermutations(str.toCharArray(), 0, result);
        return result;
    }

    private static void generatePermutations(char[] chars, int index, List<String> result) {
        if (index == chars.length) {
            result.add(new String(chars));
            return;
        }

        for (int i = index; i < chars.length; i++) {
            swap(chars, i, index);
            generatePermutations(chars, index + 1, result);
            swap(chars, i, index); // backtrack
        }
    }

    private static void swap(char[] chars, int i, int j) {
        char temp = chars[i];
        chars[i] = chars[j];
        chars[j] = temp;
    }

    public static void main(String[] args) {
        String str = "abc";
        List<String> permutations = getPermutations(str);
        System.out.println(permutations);
    }
}
```

**Output:**  
`[abc, acb, bac, bca, cab, cba]`

---

### **48. Find the Longest Palindromic Substring in a String**
**Algorithm:**
1. Expand from each character to check for the longest palindrome substring.

**Time Complexity:**  
O(N^2), where N is the length of the string.

**Code:**
```java
public class LongestPalindromicSubstring {
    public static String longestPalindrome(String s) {
        if (s == null || s.length() < 1) return "";
        
        int start = 0, maxLength = 1;
        
        for (int i = 0; i < s.length(); i++) {
            int len1 = expandAroundCenter(s, i, i);
            int len2 = expandAroundCenter(s, i, i + 1);
            int len = Math.max(len1, len2);
            
            if (len > maxLength) {
                maxLength = len;
                start = i - (len - 1) / 2;
            }
        }
        return s.substring(start, start + maxLength);
    }

    private static int expandAroundCenter(String s, int left, int right) {
        while (left >= 0 && right < s.length() && s.charAt(left) == s.charAt(right)) {
            left--;
            right++;
        }
        return right - left - 1;
    }

    public static void main(String[] args) {
        String s = "babad";
        System.out.println(longestPalindrome(s));
    }
}
```

**Output:**  
`bab` or `aba`

---

### **49. Solve the Coin Change Problem using Dynamic Programming**
**Algorithm:**
1. Use dynamic programming to find the minimum number of coins that make up the amount.

**Time Complexity:**  
O(N * M), where N is the amount and M is the number of coin denominations.

**Code:**
```java
import java.util.*;

public class CoinChange {
    public static int coinChange(int[] coins, int amount) {
        int[] dp = new int[amount + 1];
        Arrays.fill(dp, amount + 1);
        dp[0] = 0;
        
        for (int i = 1; i <= amount; i++) {
            for (int coin : coins) {
                if (i - coin >= 0) {
                    dp[i] = Math.min(dp[i], dp[i - coin] + 1);
                }
            }
        }
        
        return dp[amount] > amount ? -1 : dp[amount];
    }

    public static void main(String[] args) {
        int[] coins = {1, 2, 5};
        int amount = 11;
        System.out.println(coinChange(coins, amount));
    }
}
```

**Output:**  
`3` (since 11 = 5 + 5 + 1)

---

### **50. Detect and Remove a Cycle in a Linked List**
**Algorithm:**
1. Use Floyd’s Tortoise and Hare algorithm to detect the cycle. If detected, remove the cycle by finding the node where the cycle begins.

**Time Complexity:**  
O(N), where N is the number of nodes.

**Code:**
```java
class ListNode {
    int val;
    ListNode next;
    ListNode(int x) { val = x; }
}

public class LinkedListCycle {
    public static boolean hasCycle(ListNode head) {
        if (head == null) return false;
        
        ListNode slow = head, fast = head;
        
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;
            
            if (slow == fast) {
                return true;
            }
        }
        return false;
    }

    public static void removeCycle(ListNode head) {
        if (head == null) return;

        ListNode slow = head, fast = head;
        
        // Detect cycle
        while (fast != null && fast.next != null) {
            slow = slow.next;
            fast = fast.next.next;

            if (slow == fast) {
                break;
            }
        }

        if (slow != fast) return; // No cycle found

        // Find the cycle start node
        slow = head;
        while (slow != fast) {
            slow = slow.next;
            fast = fast.next;
        }
        
        // Remove the cycle
        while (fast.next != slow) {
            fast = fast.next;
        }
        fast.next = null;
    }

    public static void main(String[] args) {
        // Create a linked list with a cycle
        ListNode head = new ListNode(1);
        head.next = new ListNode(2);
        head.next.next = new ListNode(3);
        head.next.next.next = new ListNode(4);
        head.next.next.next.next = head.next;  // Creating a cycle

        System.out.println("Has cycle: " + hasCycle(head));
        removeCycle(head);
        System.out.println("Has cycle after removal: " + hasCycle(head));
    }
}
```

**Output:**  
`Has cycle: true`  
`Has cycle after removal: false`

---


These problems will strengthen your foundational and intermediate-level programming skills. You can use any programming language of your choice, such as Python, Java, C++, or JavaScript, to solve these. Let me know if you’d like detailed solutions or hints for any of these!
