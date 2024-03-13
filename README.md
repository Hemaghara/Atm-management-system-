# Atm-management-system-
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        atm sbi=new atm();
        int total_balance=10000;
        while (true){
            System.out.println("atm menu:");
            System.out.println("1.withdraw your money");
            System.out.println("2.deposit your money");
            System.out.println("3.check balance from the account");
            System.out.println("4.exit");

            System.out.println("Please enter your choice:");
            int choice=scanner.nextInt();

            switch (choice){
                case 1:
                    total_balance = sbi.withdraw_money(total_balance);
                    break;

                case 2:
                    total_balance = sbi.deposit_money(total_balance);
                    break;

                case 3:
                    sbi.check_balance(total_balance);
                    break;

                case 4:
                    sbi.exit();
                    System.exit(0);
                    break;

                default:
                    System.out.println("please enter a valid choice");
            }
        }
    }
}

class atm {
    public int withdraw_money(int total_balance) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("please enter your account number:");
        int account_number=scanner.nextInt();

        System.out.println("Please enter your amount:");
        int amount = scanner.nextInt();

        System.out.println("please enter your pin number:");
        int pin_number=scanner.nextInt();
        if (amount>0 && amount<=total_balance){
            total_balance-=amount;
            System.out.println("after the complete withdraw show your balalnce:"+total_balance);
        } else{
            System.out.println(" insufficient balance in your account:");
        }
        return total_balance;
    }
    public int deposit_money(int total_balance) {
        Scanner scanner=new Scanner(System.in);
        System.out.println("please enter your account number:");
        int account_number=scanner.nextInt();

        System.out.println("Please enter your amount:");
        int amount=scanner.nextInt();

        System.out.println("please enter your pin number:");
        int pin_number=scanner.nextInt();
        if (amount>0) {
            total_balance+=amount;
            System.out.println("your total balance in your account:" + total_balance);
        } else{
            System.out.println("please enter a valid amount:");
        }
        return total_balance;
    }
    public void check_balance(int total_balance) {
        System.out.println("Your current balance:"+total_balance);
    }
    public void exit() {
        System.out.println("Visit again sbi atm Have a good day...");
    }
}
