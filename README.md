import java.util.Scanner;

public class Main
{

    static int print_space(int space)
    {

        if (space == 0)
            return 1;
        System.out.print(" ");


        print_space(space - 1);
        return 1;
    }

    static int print_row(int no, int val)
    {

        if (no == 0)
            return 1;
        System.out.print(val + " ");


        print_row(no - 1, val);
        return 1;
    }


    static int pattern(int sayi, int num)
    {


        if (sayi ==0)
            return 1;
        print_space(sayi - 1);
        print_row(num - sayi +1, num - sayi +1);
        System.out.println();


        
        pattern(sayi - 1, num);
        return 1;
    }


    public static void main(String[] args)
    {
        Scanner girdi=new Scanner(System.in);

        System.out.println("1 ile 10 arasınd kat sayısını giriniz ");
        int sayi=girdi.nextInt();

        while(sayi<1||sayi>10){
            System.out.println("Kat sayısı 1 ile 10 arsınd girmediniz! ");
            System.out.println("1 ile 10 arasınd kat sayısını giriniz ");
            sayi=girdi.nextInt();
        }
        pattern(sayi, sayi);




    }
}


