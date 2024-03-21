# ATM_INTERFACE
import java.util.Scanner;

public class Codesoft2{
   static Scanner sc=  new Scanner(System.in);
static int balance = 10000;
static int withdraw;
static int deposit;


private static void checkbalance(){
    System.out.println("The Available Balance in Your Account is="+balance);
    System.out.println();
}


private static void Withdraw(){
    System.out.println("ENTER THE MONEY YOU WANT TO WITHRAW :-");
withdraw= sc.nextInt();

if(withdraw > balance){
    System.out.println("INSUFFICIENT BALANCE");
}else{
    balance=balance-withdraw;
    System.out.println("YOUR WITHDRAW HAS BEEN SUCCESSFUL");
    System.out.println("PLEASE COLLECT YOUR MONEY");
    System.out.println();
}  
System.out.println();
}


private static void deposit(){
    System.out.println("ENTER THE MONEY YOU WANT TO DEPOSIT");
    deposit=sc.nextInt();
balance= balance+deposit;
System.out.println("YOUR MONEY HAS BEEN SUCCESFUULY DEPOSITED IN YOUR ACCOUNT");
System.out.println("The Available Balance in Your Account is="+balance);
System.out.println();
}


private static void exit(){
    System.exit(0);
}


public static void main(String args[]){

    while(true){
        System.out.println("WELCOME TO AUTOMATED TELLER MACHINE");
        System.out.println("CHOOSE 1 FOR CHECKING BALANCE");
         System.out.println("CHOOSE 2 FOR WITHDRAWING MONEY FROM YOUR ACCOUNT");
          System.out.println("CHOOSE 3 FOR DEPOSITING MONEY IN YOUR ACCOUNT");
           System.out.println("CHOOSE 4 FOR EXIT");

       
           
        int choice=sc.nextInt();

           switch(choice){
            case 1:
            checkbalance();
            break;
           
           case 2:
           Withdraw();
           break;

           case 3:
           deposit();
           break;

           case 4:
           exit();
           break;
    }

    }
}
}
