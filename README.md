package atmInterface;
import java.util.Scanner;
public class AtmInterface  {
     static float balance;
    
  public  static  void  withdraw(){
         
         Scanner read = new Scanner(System.in);
         System.out.println("Enter amount To Withdraw :----");
         int amount = read.nextInt();
         if(balance>amount){
         balance = balance - amount;
         System.out.println("Amount Withdraw Successfully !!!");
         System.out.println();
         }
         else
         {
           System.out.print("No Sufficient Money");
           System.out.println();
        }
      menubar();
  }    
    public  static  void deposite(){
        
         Scanner read = new Scanner(System.in);
         System.out.println("Enter amount To Deposite ");
          int amount = read.nextInt();
          
         balance  = balance + amount;
         System.out.println("Amount Deposited Successfully !!");
            System.out.println();
         menubar();
     }
  public  static void check_balance(){
      
      System.out.println("Total Balance Is :--- " + balance );
      System.out.println();
      menubar();
    }
     public static void menubar(){
         System.out.println();
          System.out.println(" Enter Operation  NO :--");
         System.out.println();
          System.out.println("WithDraw == 1");
          System.out.println("Deposite == 2");
          System.out.println("Check Balance == 3");
          System.out.println("Exit == 4");
          System.out.println("___________________________________________");
          Scanner sc = new Scanner(System.in);
         int  n = sc.nextInt();
        
          if(n == 1){
            withdraw();
          }
          else if(n==2){
                  deposite();
          }
                      
          else if(n==3){
              check_balance();
          }  
           else if(n==4){
            System.out.print("Exit !!!");
                }
          else {
             System.out.println("Select Proper Number to perform operation :--");
             System.out.println();
             menubar();
             
              }         
         }     
      
    public static void main(String[] args) {
        
              
           AtmInterface  obj = new AtmInterface();
            obj.menubar(); 
    } 
}
    
