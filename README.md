# interface
package calculator.program;
import java.util.Scanner;
//define a calculator interface
interface Calculator {
    double add(double a,double b);
     double subtract(double a,double b);
      double multiply(double a,double b);
       double divide(double a,double b);
}
//implement the interface in simplecalculator
class Simplecalculator implements Calculator{
  @Override
  public double add(double a,double b){
      return a+b;
  }
  @Override
   public double subtract(double a,double b){
      return a-b;
  }
  @Override
    public double multiply(double a,double b){
      return a*b;
  }
    public double divide(double a,double b){
        if (b==0){
            System.out.println("error: division by zero is not allowed");
            return Double.NaN;
        }
        return a/b;
    }
 }
public class CalculatorProgram {
 public static void main(String[] args) {
   Scanner sc = new Scanner(System.in);
        Calculator calc = new Simplecalculator();
        System.out.println("welcome to the simple calculator");
        //input 2 numbers
        System.out.println("enter 1st number: ");
        double num1 = sc.nextDouble();
        System.out.println("enter 2nd number: ");
        double num2 = sc.nextDouble();
         //perform calculations
        System.out.println("\n results: ");
        System.out.println("addition:" + calc.add(num1,num2));
        System.out.println("subtraction:" + calc.subtract(num1,num2));
        System.out.println("multiplication:" + calc.multiply(num1,num2));
        System.out.println("division:" +calc.divide(num1, num2));
       sc.close();
        
    }
    }
output:
welcome to the simple calculator
enter 1st number: 
10
enter 2nd number: 
5
results: 
addition:15.0
subtraction:5.0
multiplication:50.0
division:2.0
