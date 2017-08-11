# 云课堂昵称：耿耿余淮丶
Hello,this is test3

import java.util.Scanner;  
  
public class Main {  
    public static boolean isPrime(int n){  
        int i;  
        if(n==1)  
            return false;  
        else if(n==2)  
            return true;  
        else{  
            for(i=2;i<Math.sqrt(n)+1;i++)  
                if(n%i==0)  
                    return false;  
            return true;  
        }  
    }  
      
    public static void main(String[] args) {  
        // TODO Auto-generated method stub  
        Scanner in = new Scanner(System.in);  
            
        int n = in.nextInt();  
        int i;  
        boolean frist =true;  
        if(isPrime(n))  
            System.out.println(n+"="+n);  
        else{  
            System.out.print(n+"=");  
            while(!isPrime(n))  
                for(i=2;i<Math.sqrt(n)+1;i++)  
                    if(isPrime(i)&&n%i==0)  
                        {System.out.print(i+"x");n/=i;break;}  
            System.out.println(n);  
        }  
           
    }  
}
