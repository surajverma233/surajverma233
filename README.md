import java.util.Scanner;
public class ATMMachine{
 public static void main(String[] args){
    int Balance = 100000, withdraw, deposit;
    Scanner sc = new Scanner(System.in);

    while(true)
    {
        System.out.println(" ----!! Welcome to ATM !!----");
        System.out.println("1. Withdraw Money");
        System.out.println("2. Deposite Money");
        System.out.println("3. Check A/C Balance");
        System.out.println("4. Exit");
        System.out.println("Please select option You want to perform");  

       int choice = sc.nextInt();
           switch (choice)
            {
              case 1:
        System.out.print("Enter Money to be Withdraw :");
    
         withdraw = sc.nextInt();

         if(Balance >= withdraw)
         {
            Balance = Balance - withdraw;
            System.out.println("-Successfully Withdraw- ! Please Collect Your Money !");
         }
         else{
            System.out.println("Insufficient Balance");
         }
         System.out.println("");
         break;
         case 2:
         System.out.print("Enter Money to be deposited :");
         deposit = sc.nextInt();

         Balance = Balance + deposit;
         System.out.println("Your Money has been Seccessfully deposited");
         System.out.println("");
         break;

         case 3:
         System.out.println("Balance :"+Balance);
         System.out.println("");
         break;

         case 4:
         System.exit(0);
        }
    }
}
}
