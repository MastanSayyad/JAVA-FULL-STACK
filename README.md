# JAVA-FULL-STACK

### How to solve a problem

**Ask 3 questions every time:**
1. **What do they want me to read? → Input**
2. **What do they want me to print? → Output**
3. **What happens between reading and printing? → Logic**

| Step | What We Did                  | Why                          |
| ---- | ---------------------------- | ---------------------------- |
| 1    | Read the problem slowly      | To understand what’s needed  |
| 2    | Found inputs                 | To know what we’ll read      |
| 3    | Found outputs                | To know what to print        |
| 4    | Wrote steps in plain English | So we can “see” the logic    |
| 5    | Wrote Java code              | Just translated step by step |
| 6    | Tested                       | Confirmed it works           |


### 🧩 Problem:

> Given an array of integers, print the smallest and largest number.

### 🧠 Step 1: Understand the story

What’s happening here?

👉 You will get a set (or list) of numbers.
👉 You need to find the minimum and maximum values among them.
👉 Then print both.

Example:
```
If input is 5 2 9 1 6,
→ smallest = 1, largest = 9.
```
Output:
```
Minimum: 1
Maximum: 9
```
### 🔍 Step 2: Identify Inputs

Usually, HackerRank gives input like this:
```
5
2 9 1 6 4
```

But let’s break it down:

- First line = number of elements (n = 5)
- Second line = the actual elements
- We’ll store them in an array.

### 🖨 Step 3: Identify Outputs

We just print:
```
Minimum: <smallest number>
Maximum: <largest number>
```
### ⚙️ Step 4: Think in plain English (Algorithm)

- Read n (number of integers).
- Create an array of size n.
- Read n integers and store them in the array.
- Assume min and max are the first number in the array.
- Loop through the array:
    - If a number is smaller than min, update min.
    - If a number is larger than max, update max.
- Print both min and max.

### 💻 Step 5: Translate into Java Code
```
import java.util.*;

public class Solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();        // Step 1: read number of elements
        int[] arr = new int[n];      // Step 2: create array
        
        for (int i = 0; i < n; i++) {   // Step 3: read n integers
            arr[i] = sc.nextInt();
        }
        
        int min = arr[0];   // Step 4: initialize min and max
        int max = arr[0];
        
        for (int i = 1; i < n; i++) {   // Step 5: loop to find min & max
            if (arr[i] < min) {
                min = arr[i];
            }
            if (arr[i] > max) {
                max = arr[i];
            }
        }
        
        // Step 6: print results
        System.out.println("Minimum: " + min);
        System.out.println("Maximum: " + max);
    }
}
```

### 🧪 Step 6: Test with Example
Input:
```
5
2 9 1 6 4
```
Output:
```
Minimum: 1
Maximum: 9
```

✅ Works perfectly!
