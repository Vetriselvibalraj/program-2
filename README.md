import java.util.Scanner;
public class JavaExample
{
    public static void main(String args[])
    {
        Scanner scan = new Scanner(System.in);
        System.out.print("Enter the number: ");

        //Storing the input number in a variable num
        int num = scan.nextInt();
        scan.close();

        /* Calling the user-defined function isSunny()
         * to check whether the input number is Sunny
         */
        isSunny(num);
    }

    /* This is the another function that we need to find whether
     * the passed number is perfect square or not.
     */
    static boolean isPerfectSquare(double num)
    {
        //Finds the square root of the passed number
        double square_root = Math.sqrt(num);

        //Whether the square root is an int or not.
        return((square_root - Math.floor(square_root)) == 0);
    }
    //This function checks whether the input number is Sunny
    static void isSunny(int num)
    {
        //we are checking whether the next number n+1 is perfect square
        if (isPerfectSquare(num + 1))
        {
            System.out.println(num + " is a Sunny number.");
        }
        //if not a perfect square that prints not a Sunny number
        else
        {
            System.out.println(num + " is not a Sunny number.");
        }
    }
}
