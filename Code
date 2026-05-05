Experiment No. 1
Implementation of Array Operations (Insertion, Deletion, Display and Exit)
c#include <stdio.h>
int main()
{
    int arr[100], n = 0;
    int choice = 0;
    int i, pos, value;
    while(choice != 4)
    {
        printf("\n--- ARRAY OPERATIONS MENU ---\n");
        printf("1. Insert Element\n");
        printf("2. Delete Element\n");
        printf("3. Display Array\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        if(choice == 1)
        {
            printf("Enter position to insert: ");
            scanf("%d", &pos);
            printf("Enter value: ");
            scanf("%d", &value);
            if(pos > n + 1 || pos <= 0)
            {
                printf("Invalid position\n");
            }
            else
            {
                i = n;
                while(i >= pos)
                {
                    arr[i] = arr[i - 1];
                    i--;
                }
                arr[pos - 1] = value;
                n++;
                printf("Element inserted successfully\n");
            }
        }
        else if(choice == 2)
        {
            printf("Enter position to delete: ");
            scanf("%d", &pos);
            if(pos > n || pos <= 0)
            {
                printf("Invalid position\n");
            }
            else
            {
                i = pos - 1;
                while(i < n - 1)
                {
                    arr[i] = arr[i + 1];
                    i++;
                }
                n--;
                printf("Element deleted successfully\n");
            }
        }
        else if(choice == 3)
        {
            if(n == 0)
            {
                printf("Array is empty\n");
            }
            else
            {
                printf("Array elements are: ");
                i = 0;
                while(i < n)
                {
                    printf("%d ", arr[i]);
                    i++;
                }
                printf("\n");
            }
        }
        else if(choice == 4)
        {
            printf("Exiting program...\n");
        }
        else
        {
            printf("Invalid choice\n");
        }
    }
    return 0;
}


Experiment No. 2
Title: Program to Check Whether the Given String is an Anagram or Not
c#include <stdio.h>
#include <string.h>
int main() {
    char str1[100], str2[100];
    int count[256] = {0};
    int i;
    scanf("%s", str1);
    scanf("%s", str2);
    if(strlen(str1) != strlen(str2)) {
        printf("Not Anagram\n");
        return 0;
    }
    for(i = 0; str1[i] != '\0'; i++) {
        count[str1[i]]++;
        count[str2[i]]--;
    }
    for(i = 0; i < 256; i++) {
        if(count[i] != 0) {
            printf("Not Anagram\n");
            return 0;
        }
    }
    printf("Anagram\n");
    return 0;
}



Experiment No. 3
Implementation of Stack Operation Using Array
c#include <stdio.h>
#define MAX 100
int main() {
    int stack[MAX];
    int top = -1;
    int choice, value, i;
    while (1) {
        printf("\n--- STACK MENU ---\n");
        printf("1. Push\n");
        printf("2. Pop\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
            case 1: // Push
                if (top == MAX - 1) {
                    printf("Stack Overflow! Cannot push.\n");
                } else {
                    printf("Enter value to push: ");
                    scanf("%d", &value);
                    top++;
                    stack[top] = value;
                    printf("Value pushed successfully.\n");
                }
                break;
            case 2: // Pop
                if (top == -1) {
                    printf("Stack Underflow! Cannot pop.\n");
                } else {
                    printf("Popped value: %d\n", stack[top]);
                    top--;
                }
                break;
            case 3: // Display
                if (top == -1) {
                    printf("Stack is empty.\n");
                } else {
                    printf("Stack elements are:\n");
                    for (i = top; i >= 0; i--) {
                        printf("%d\n", stack[i]);
                    }
                }
                break;
            case 4: // Exit
                printf("Exiting program...\n");
                return 0;
            default:
                printf("Invalid choice! Try again.\n");
        }
    }
    return 0;
}





Experiment No. 4
Program to Implement Queue Operations Using Array Implementation
c#include <stdio.h>
#define MAX 5
int main() {
    int queue[MAX];
    int front = -1, rear = -1;
    int choice, item;
    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue\n");
        printf("2. Dequeue\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
            case 1: // Enqueue
                if (rear == MAX - 1) {
                    printf("Queue Overflow!\n");
                } else {
                    printf("Enter value: ");
                    scanf("%d", &item);
                    if (front == -1) {
                        front = 0;
                    }
                    rear++;
                    queue[rear] = item;
                    printf("Inserted: %d\n", item);
                }
                break;
            case 2: // Dequeue
                if (front == -1 || front > rear) {
                    printf("Queue Underflow!\n");
                } else {
                    printf("Deleted: %d\n", queue[front]);
                    front++;
                }
                break;
            case 3: // Display
                if (front == -1 || front > rear) {
                    printf("Queue is empty\n");
                } else {
                    printf("Queue elements: ");
                    for (int i = front; i <= rear; i++) {
                        printf("%d ", queue[i]);
                    }
                    printf("\n");
                }
                break;
            case 4:
                printf("Exiting...\n");
                return 0;
            default:
                printf("Invalid choice!\n");
        }
    }
}






Experiment No. 5
Title: Implementation of Stack Using Linked List
c#include <stdio.h>
#include <stdlib.h>
int main() {
    struct node {
        int data;
        struct node *next;
    };
    struct node *top = NULL, *newnode, *temp;
    int choice, value;
    while(1) {
        scanf("%d", &choice);
        switch(choice) {
            // PUSH
            case 1:
                newnode = (struct node*)malloc(sizeof(struct node));
                if(newnode == NULL) {
                    printf("Stack Overflow\n");
                    break;
                }
                scanf("%d", &value);
                newnode->data = value;
                newnode->next = top;
                top = newnode;
                printf("%d\n", value);
                break;
            case 2:
                if(top == NULL) {
                    printf("Stack Underflow\n");
                    break;
                }
                temp = top;
                printf("Deleted element: %d\n", top->data);
                top = top->next;
                free(temp);
                break;
            case 3:
                if(top == NULL) {
                    printf("Stack is Empty\n");
                    break;
                }
                temp = top;
                while(temp != NULL) {
                    printf("%d ", temp->data);
                    temp = temp->next;
                }
                printf("\n");
                break;
            case 4:
                exit(0);
            default:
                printf("Invalid choice\n");
        }
    }
    return 0;
}




Experiment No. 8
Title: Reverse a Singly Linked List
c#include <stdio.h>
#include <stdlib.h>
int main() {
    struct node {
        int data;
        struct node *next;
    };
    struct node *head = NULL, *newnode, *temp;
    struct node *prev = NULL, *current, *nextnode;
    int choice, value;
    while(1) {
        scanf("%d", &choice);
        switch(choice) {
            // INSERT AT END
            case 1:
                newnode = (struct node*)malloc(sizeof(struct node));
                if(newnode == NULL) {
                    printf("Memory Overflow\n");
                    break;
                }
                scanf("%d", &value);
                newnode->data = value;
                newnode->next = NULL;
                if(head == NULL) {
                    head = newnode;
                } else {
                    temp = head;
                    while(temp->next != NULL) {
                        temp = temp->next;
                    }
                    temp->next = newnode;
                }
                printf("%d\n", value);
                break;
            // REVERSE LINKED LIST
            case 2:
                if(head == NULL) {
                    printf("List is Empty\n");
                    break;
                }
                prev = NULL;
                current = head;
                while(current != NULL) {
                    nextnode = current->next;
                    current->next = prev;
                    prev = current;
                    current = nextnode;
                }
                head = prev;
                printf("List Reversed\n");
                break;
            // DISPLAY
            case 3:
                if(head == NULL) {
                    printf("List is Empty\n");
                    break;
                }
                temp = head;
                while(temp != NULL) {
                    printf("%d ", temp->data);
                    temp = temp->next;
                }
                printf("\n");
                break;
            // EXIT
            case 4:
                exit(0);
            default:
                printf("Invalid choice\n");
        }
    }
    return 0;
}






Experiment No. 12
Program to Sort a Given Array Using Selection Sorting Method
c#include <stdio.h>
int main() {
    int arr[100], n, i, j, min_idx, temp;
    printf("Enter number of elements: ");
    scanf("%d", &n);
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    for(i = 0; i < n - 1; i++) {
        min_idx = i;
        for(j = i + 1; j < n; j++) {
            if(arr[j] < arr[min_idx]) {
                min_idx = j;
            }
        }
        temp = arr[min_idx];
        arr[min_idx] = arr[i];
        arr[i] = temp;
    }
    printf("Sorted array:\n");
    for(i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}





Experiment No. 13 (Corrected)
Program to Search an Element in an Array Using Binary Search Method
c#include <stdio.h>
int main()
{
    int i, n, mid, low, high, tar, found = 0;
    printf("Enter number of elements:\n");
    scanf("%d", &n);
    int a[n];
    printf("Enter %d elements (in sorted order):\n", n);
    for(i = 0; i < n; i++)
        scanf("%d", &a[i]);
    printf("Enter element to search: ");
    scanf("%d", &tar);
    low = 0;
    high = n - 1;
    while(low <= high)
    {
        mid = (low + high) / 2;
        if(a[mid] == tar)
        {
            found = 1;
            break;
        }
        else if(a[mid] > tar)
        {
            high = mid - 1;
        }
        else
        {
            low = mid + 1;
        }
    }
    if(found)
        printf("Element found at position %d\n", mid + 1);  // corrected
    else
        printf("Element not found\n");
    return 0;
}






