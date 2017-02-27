1)Can you overload a method with same return type.? Explain your answer with proper logic.
Ans:
 Yes, a method with the same return type can be overloaded.This is can be done by passing different number of arguments to the overloaded method. This can be explained with proper logic as below:
     CODE :
            import java.util.*;
            public class Main 
            {
               public static void main(String args[])
               {
                 int x,y,z,ans=0;
                 Scanner sc=new Scanner(System.in);
                 System.out.println("Choice");
                 System.out.println("1.Sum of two numbers");
                 System.out.println("2.Sum of three numbers");
                 int ch=sc.nextInt();   //Choice of user is obtained
                 switch(ch)  //switch case
                 {
                 
                 case 1 : System.out.println("Enter two numbers");
                          x=sc.nextInt();
                          y=sc.nextInt();
                          ans=sum(x,y);   //Calling the overloaded function for the 1st choice
                          System.out.print("Sum of two numbers is : "+ans);
                          break;
                          
                 case 2 : System.out.println("Enter three numbers");
                            x=sc.nextInt();
                            y=sc.nextInt();
                            z=sc.nextInt();
                            ans=sum(x,y,z);   //Calling the overloaded function for the 2nd choice
                            System.out.print("Sum of three numbers is : "+ans);
                            break; 
                            
                 }

                 }
               static int sum(int a,int b)
               {
                 return a+b;   //Returns the sum of two numbers
               }
               
               static int sum(int a,int b,int c)
               {
                 return a+b+c; //Returns the sum of three numbers
               }
               
            }
     OUTPUT :
            Choice
            1.Sum of two numbers
            2.Sum of three numbers
            2
            Enter three numbers
            20
            30
            40
            Sum of three numbers is : 90 
           
           
 2)Write a program in java using Arrays, that sorts the element in descending order.
 Ans:
            import java.util.*;
            public class Main 
            {
               public static void main(String args[])
            {
                 Scanner sc=new Scanner(System.in);
                 int temp;
                 System.out.println("Enter the size of array : ");
                 int n=sc.nextInt();  //array size
                 int arr[]=new int[n];
                 System.out.println("Enter the elements of array");
                 for(int i=0;i<n;i++)
                 {
                   arr[i]=sc.nextInt(); //array elements
                 }
                 for(int i=0;i<n;i++)
                 {
                   for(int j=i+1;j<n;j++) 
                       {
                           if (arr[i] < arr[j]) 
                           {
                               temp = arr[i];
                               arr[i] = arr[j];
                               arr[j] = temp;
                           }
                       }
                 }
                 System.out.println("Sorted array is");
                 for(int i=0;i<arr.length;i++)
                   System.out.println(arr[i]); //displaying sorted elements
               }
            }
      Output :-
            Enter the array size : 
            6
            Enter the array elements
            4
            7
            2
            6
            9
            8
            Sorted array is 
            9
            8
            7
            6
            4
            2
