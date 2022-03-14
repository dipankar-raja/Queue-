# Queue-
//Queue using Java




import java.io.*;
import java.util.Scanner;
class queue
{
   
        int front,rear;
        int item[]=new int[10];
}

class queue1
{
   
   
    void insert(queue ps,int x)
    {
            if(ps.rear==9)
            {
                    System.out.println("\nSTACK OVERFLOW");
                   
            }
            else
            ps.item[++(ps.rear)]=x;
    }
    int remove(queue ps)
    {
            if(ps.rear<ps.front)
            {
                    System.out.println("\nSTACK UNDERFLOW");
                    return 0;
            }
            else
            return(ps.item[ps.front++]);
    }
    void display(queue q)
    {
            int k;
            System.out.println("\nOUTPUT==>>");
            if(q.rear<q.front)
            {
                System.out.println("\tQUEUE UNDERFLOW");
            }
            else
            {
                    for(k=q.front;k<=q.rear;k++)
                    System.out.println("\t"+q.item[k]);
            }
    }
}

class ds1
{
    public static void main(String args[])
    {
        queue ps=new queue();
        queue1 s=new queue1();
        Scanner sc=new Scanner(System.in);
        ps.rear=-1;
            ps.front=0;;
        int i,j,n=20;
        while(n>=0)
            {
                     System.out.println("\nPress 1 for insert=");
                    System.out.println("\nPress 2 for remove=");
                    System.out.println("\nPress 3 for display=");
                   System.out.println("\nPress 4 for exit=");
                    System.out.println("\nEnter Choice=");
                    i=sc.nextInt();
               
                System.out.println("\n\n\t\t\t\t<<==QUEUE==>>\n\n");
                switch(i)
                {
                    case 1:    System.out.println("\nEnter element=");
                                j=sc.nextInt();
                               s.insert(ps,j);
                               break;
                    case 2:     System.out.println("\nThe remove element is="+s.remove(ps));
                            break;
                    case 3:     s.display(ps);
                               break;
                   
                    default:System.out.println("\n\bWRONG CHOICE");
                    }
        n--;
        }
           

    }

}
