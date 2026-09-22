## EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
### Aim:
To write a C program print the lowercase English word corresponding to the number
### Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
### Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    switch (n) {
        case 71:
            printf("seventy one");
            break;
        case 72:
            printf("seventy two");
            break;
        case 73:
            printf("seventy three");
            break;
        case 74:
            printf("seventy four");
            break;
        case 75:
            printf("seventy five");
            break;
        case 76:
            printf("seventy six");
            break;
        case 77:
            printf("seventy seven");
            break;
        case 78:
            printf("seventy eight");
            break;
        case 79:
            printf("seventy nine");
            break;
        default:
            printf("Greater than 79");
    }

    return 0;
}
```

### Output:

<img width="513" height="176" alt="image" src="https://github.com/user-attachments/assets/868091ac-d27b-4f75-ae9d-8d3f20b223b0" />

### Result:
Thus, the program is verified successfully
 
## EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
### Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
### Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
### Program:
```
#include <stdio.h>

int main() {
    char a[50];
    int i, j, c;

    printf("Enter a string: ");
    scanf("%s", a);

    for (i = 0; i <= 3; i++) {
        c = 0;

        for (j = 0; a[j] != '\0'; j++) {
            if (a[j] == i + '0')
                c++;
        }

        printf("%d ", c);
    }

    return 0;
}
```

### Output:

<img width="446" height="182" alt="image" src="https://github.com/user-attachments/assets/33e9debe-98a6-46d0-af71-8cef56053e1c" />

### Result:
Thus, the program is verified successfully

## EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
### Aim:
To write a C program to print all of its permutations in strict lexicographical order.

### Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
### Program:
```
#include <stdio.h>
#include <string.h>

void swap(char *a, char *b) {
    char temp = *a;
    *a = *b;
    *b = temp;
}

void reverse(char *s, int start, int end) {
    while (start < end) {
        swap(&s[start], &s[end]);
        start++;
        end--;
    }
}

int nextPermutation(char *s) {
    int i, j, n = strlen(s);

    i = n - 2;
    while (i >= 0 && s[i] >= s[i + 1])
        i--;

    if (i < 0)
        return 0;

    j = n - 1;
    while (s[j] <= s[i])
        j--;

    swap(&s[i], &s[j]);
    reverse(s, i + 1, n - 1);

    return 1;
}

int main() {
    char s[50];
    int i, j, n;

    printf("Enter a string: ");
    scanf("%s", s);

    n = strlen(s);

    for (i = 0; i < n - 1; i++) {
        for (j = i + 1; j < n; j++) {
            if (s[i] > s[j])
                swap(&s[i], &s[j]);
        }
    }

    printf("Permutations in lexicographical order:\n");
    printf("%s\n", s);

    while (nextPermutation(s))
        printf("%s\n", s);

    return 0;
}
```

### Output:

<img width="482" height="387" alt="image" src="https://github.com/user-attachments/assets/4f77f89c-e61c-406b-ab34-e9d7910b1f82" />

### Result:
Thus, the program is verified successfully
 
## EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
### Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
### Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
### Program:
```
#include <stdio.h>

int main() {
    int n, i, j, min, len;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    len = n * 2 - 1;

    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            min = i;

            if (j < min)
                min = j;

            if (len - 1 - i < min)
                min = len - 1 - i;

            if (len - 1 - j < min)
                min = len - 1 - j;

            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```

### Output:

<img width="443" height="332" alt="image" src="https://github.com/user-attachments/assets/5a5e5cb9-9f96-4e52-8668-19b208f34950" />

### Result:
Thus, the program is verified successfully

## EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

### Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

### Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

### Program:
```
#include <stdio.h>

int square() {
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    return n * n;
}

int main() {
    int result;

    result = square();

    printf("Square = %d", result);

    return 0;
}
```

### Output:

<img width="545" height="197" alt="image" src="https://github.com/user-attachments/assets/36fc87e4-a68d-4851-80fb-570760980d4f" />

### Result:
Thus, the program is verified successfully






