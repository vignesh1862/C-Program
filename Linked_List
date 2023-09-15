
#include<stdio.h>
#include<stdlib.h>

struct node
{
    int data;
    struct node *next;
};

    struct node *head=NULL;

    void Newnode(int val)
    {
        struct node *list;
        list=(struct node*)malloc(sizeof(struct node));
        
        if(head==NULL)
        {
            list->data=val;
            list->next=NULL;
            head=list;
            printf("created %d \n",list->data);
        }
        else
        {
            list->data=val;
            list->next=head;
            head=list;
            printf("created %d \n",list->data);
        }
        
    }
        
        void display()
        {
            struct node *temp=head;
            
            while(temp!=NULL)
            {
                printf("%d",temp->data);
                temp=temp->next;
            }
            
            if(temp==NULL)
            {
                printf("\n");
            }
        }
        
        void addposition(int pos,int val)
        {
            struct node *temp=head;
            
            struct node *list;
            list =(struct node*)malloc(sizeof(struct node));
            
            for(int i=1;i<=pos-1;i++)
            {
                temp=temp->next;
            }
            
            list->next=temp->next;
            temp->next=list;
            list->data=val;
            printf("added %d position \n",pos);
            printf("added %d value \n",val);
        }
        
        void delete(int pos)
        {
            struct node *temp=head;
            struct node *prev=NULL;
            
            for(int i=0;i<pos;i++)
            {
                prev=temp;
                temp=temp->next;
            }
            
            prev->next=temp->next;
            printf("Delted %d \n",temp->data);
            free(temp);
        }
        
        
        void main()
        {
            int choice,val,pos;
            
            while(1)
            {
                scanf("%d",&choice);
                
                switch(choice)
                {
                    case 1: printf("Enter the value \n");
                            scanf("%d",&val);
                            Newnode(val);
                            break;
                    
                    case 2: display();
                            break;
                            
                            
                    case 3: printf("Enter position Value\n");
                            scanf("%d",&pos);
                            scanf("%d",&val);
                            addposition(pos,val);
                            break;
                    
                    case 4: printf("Enteer position for delete\n");
                            scanf("%d",&pos);
                            delete(pos);
                            break;
                            
                            
                            
                    default : printf("Enter valid choice \n");
                }
            }
            
            
            
            
        }
        
        
        
