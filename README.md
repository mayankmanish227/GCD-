# GCD-
list of all common divisor can be obtained by returning whole list (in java)


import java.util.*; 
import java.io.*; 
public class HelloWorld
{
    public static void main(String []args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int[] arr=new int[n];
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
        }
        System.out.println(check(arr));
    }
    static int check(int[] arr) 
    {
        int count=0;
        List<Integer> li=new ArrayList<>();
        int max=arr[0];
       for(int i=0;i<arr.length;i++)
       {
           if(max<arr[i])
           {
               max=arr[i];
           }
           
       }

        for(int i=2;i<max/2;i++)
        {
            count=0;
            for(int j=0;j<arr.length;j++)
            {
                if(arr[j]%i==0)
                {
                    count++;
                }
            }
            if(count==arr.length)
            {
                li.add(i);
            }
        }
        return Collections.max(li);
        
    }
}
