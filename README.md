# Adv-C-Mod-12


EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display stack elements using linked list.


Algorithm:

1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.

2.	Declare a global variable head representing the starting node of the linked list.

3.	Define a function display to print the elements of the linked list.

4.	Declare a pointer p and initialize it with the head of the linked list.

5.	Use a while loop to traverse the linked list:

6.	Print the data of the current node.

7.	Move to the next node using the next pointer.
 
Program:

```
struct Node   
{  
char data;  
struct Node *next;  
}*head;  
void display()  
{  
    struct Node *ptr;
    ptr=head;
    
        while(ptr!=NULL)
        {
        printf("%c\n",ptr->data);
        ptr=ptr->next;
        }
    
}
```

Output:

![image](https://github.com/user-attachments/assets/5bac2e30-764e-4942-abe3-0d7ab683a197)

Result:

Thus, the program to display stack elements using linked list is verified successfully. 



EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.

Aim:

To write a C program to pop an element from the given stack using liked list.

Algorithm:

1.	Check for Empty Stack

2.	If head is equal to NULL, Print "Stack is empty."

3.	Else Proceed to the next step.

4.	Set head to point to the next node in the stack.
 
Program:

```
struct Node   
{  
int data;  
struct Node *next;  
}*head,*temp;  
void pop()  
{ 
    if(head==NULL)
    {
        printf("stack is empty");
    }
    else
    {
        temp=head;
        head=temp->next;
        free(temp);
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/df837143-e70c-4052-96e0-42c338a79445)

Result:

Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.

Aim:

To write a C program to display queue elements using linked list.

Algorithm:

1.	Check if Queue is Empty

2.	Display Queue Elements

3.	Print the data of the current node pointed to by front

4.	Update front to point to the next node.

5.	End the display function.
 
Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display()
{
    if(front==NULL){
        printf("queue is empty\n");
        return;
    };
    printf("Queue elements:\n");
    while(front!=NULL){
        printf("%.3f\n",front->data);
        front=front->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/9be81989-52aa-4d11-a7a0-db64221c9ce6)


Result:

Thus, the program to display queue elements using linked list is verified successfully.


 
EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

Aim:

To write a C program to insert elements in queue using linked list

Algorithm:

1.	Allocate Memory for New Node

2.	Set Data and Next Pointer

3.	Check if Queue is Empty

4.	Set both front and rear to point to the new node p.

5.	Set the next pointer of the current rear to point to the new node p.

6.	End of Enqueue Operation
 
Program:
```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(float data)
{
    struct Node*newNode;
    newNode=(struct Node*)malloc(sizeof(struct Node));
    newNode->data=data;
    newNode->next=NULL;
    if(front==NULL)
    {
        front=rear=newNode;
    } else {
        rear->next=newNode;
        rear=newNode;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/409396da-6657-428b-9d99-bff603b6b1b2)


Result:

Thus, the program to insert elements in queue using linked list is verified successfully.



EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

Algorithm:

1.	Check if the queue is empty:

o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.

2.	Access the front element:

o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

Program:

```
struct Node
{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%.2f\n",front->data);
}
```

Output:

![image](https://github.com/user-attachments/assets/f99bb834-fbe6-4d95-b0e9-350ae6443d4e)


Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


