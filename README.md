# stack-1
#include<stdio.h>
#include<stdlib.h>
#define SIZE 10
int stack[SIZE];
int top=-1;

void push(int x)
{
    if(top==SIZE)
    printf("full\n");
    else{
        top++;
        stack[top]=x;
    
    }
}

void pop()
{
    if(top==-1)
    printf("empty\n");
    else{
        printf("%d", stack[top]);
        top--;
    
        }
}

void display()
{
    if(top!=-1){
        for(int i=top; i>=0; i--)
        printf("%d\n", stack[i]);
        }   
        else printf("Stack is empty\n");
    
}

int main()
{
    while(1){
        int n, a;
        printf("menu\n");
        printf(" 1 for push\n 2 for pop\n 3 for display\n 4 for exit: \n");
        scanf("%d", &n);
        switch(n){
            case 1: printf("What value do you want to be pushed?: \n");
                scanf("%d", &a);
                push(a);
                break;
            case 2: pop();
                break;
            case 3: display();
                break;
            case 4: printf("exciting program!");
                    exit(0);
        }
    }
}
