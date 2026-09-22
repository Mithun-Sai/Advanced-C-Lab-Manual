## EXP NO:11 C ### Program TO DISPLAY STACK ELEMENTS USING AN ARRAY.

### Aim:
To write a C ### Program to display stack elements using an array.
### Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
### Program:
```
#include <stdio.h>

#define MAX 5

int stack[MAX];
int top = -1;

void push(int value) {
    if (top == MAX - 1)
        printf("Stack Overflow\n");
    else
        stack[++top] = value;
}

void pop() {
    if (top == -1)
        printf("Stack Underflow\n");
    else
        top--;
}

void display() {
    int i;

    if (top == -1) {
        printf("Stack is empty\n");
        return;
    }

    printf("Stack elements are:\n");

    for (i = top; i >= 0; i--)
        printf("%d\n", stack[i]);
}

int main() {
    push(10);
    push(20);
    push(30);
    push(40);

    display();

    return 0;
}
```

### Output:

<img width="467" height="225" alt="image" src="https://github.com/user-attachments/assets/3e7f3d34-11f5-485e-867d-26b22bf4ec97" />

### Result:
Thus, the ### Program to display stack elements using an array is verified successfully.
 

## EXP NO:12  ### Program TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
### Aim:
To create a C ### Program to push the given element in to a stack using array.
### Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
### Program:
```
#include <stdio.h>

#define MAX 5

float stack[MAX];
int top = -1;

void push(float value) {
    if (top == MAX - 1) {
        printf("Stack Overflow\n");
    } else {
        top++;
        stack[top] = value;
        printf("%.2f pushed into stack\n", value);
    }
}

int main() {
    float value;

    printf("Enter an element: ");
    scanf("%f", &value);

    push(value);

    printf("Stack element: %.2f\n", stack[top]);

    return 0;
}
```

### Output:



### Result:
Thus, the ### Program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C ### Program TO DISPLAY QUEUE ELEMENTS USING ARRAY.
### Aim:
To write a C ### Program to display queue elements using array

### Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
### Program:
```
#include <stdio.h>

#define MAX 5

int queue[MAX];
int front = 0;
int rear = -1;

void display() {
    int i;

    if (rear < front) {
        printf("Queue is empty\n");
        return;
    }

    printf("Queue elements are:\n");

    for (i = front; i <= rear; i++)
        printf("%d\n", queue[i]);
}

int main() {
    queue[++rear] = 10;
    queue[++rear] = 20;
    queue[++rear] = 30;
    queue[++rear] = 40;

    display();

    return 0;
}
```

### Output:

<img width="470" height="225" alt="image" src="https://github.com/user-attachments/assets/e01bda01-fd80-4051-b78a-079892d9e1da" />

### Result:
Thus, the ### Program to display queue elements using array is verified successfully.


 
## EXP NO:14 C ### Program TO INSERT ELEMENTS IN QUEUE USING ARRAY.
### Aim:
To write a C ### Program to insert elements in queue using array.

### Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

### Program:
```
#include <stdio.h>

#define MAX 5

float queue[MAX];
int front = 0;
int rear = -1;

void enqueue(float value) {
    if (rear == MAX - 1) {
        printf("Queue Overflow\n");
    } else {
        rear++;
        queue[rear] = value;
        printf("%.2f inserted into queue\n", value);
    }
}

int main() {
    float value;

    printf("Enter an element: ");
    scanf("%f", &value);

    enqueue(value);

    printf("Queue element: %.2f\n", queue[rear]);

    return 0;
}
```

### Output:

<img width="446" height="283" alt="image" src="https://github.com/user-attachments/assets/aa1aa046-37d8-454e-95d9-c825944fbead" />

### Result:
Thus, the ### Program to insert elements in queue using array is verified successfully.



 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



### Aim:

To create a function in C that deletes an element from a queue implemented using an array.

### Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



### Program:
```
#include <stdio.h>

#define MAX 5

int queue[MAX] = {10, 20, 30, 40};
int front = 0;
int rear = 3;

void dequeue() {
    if (front == -1) {
        printf("Queue is empty\n");
        return;
    }

    printf("Deleted element: %d\n", queue[front]);
    front++;

    if (front > rear) {
        front = -1;
        rear = -1;
    }
}

int main() {
    printf("Queue elements before deletion:\n");

    for (int i = front; i <= rear; i++)
        printf("%d ", queue[i]);

    printf("\n");

    dequeue();

    printf("Queue elements after deletion:\n");

    if (front == -1)
        printf("Queue is empty\n");
    else {
        for (int i = front; i <= rear; i++)
            printf("%d ", queue[i]);
    }

    return 0;
}
```

### Output:

<img width="508" height="222" alt="image" src="https://github.com/user-attachments/assets/86d41e82-f4d4-4d35-954b-05b3a6d30277" />

### Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
