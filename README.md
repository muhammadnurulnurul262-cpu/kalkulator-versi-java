# kalkulator-versi-java
This is my personal project. I’m not too worried about mistakes—feel free to fix issues or develop it further yourself.
import java.util.Scanner; //untuk input dari user

public class Kalkulator {  // Class name capitalized for convention
    public static void main(String[] args) {  // Fixed: "String" with capital S
        Scanner scanner = new Scanner(System.in);

        System.out.println("Pilih operasi matematika:");
        System.out.println("1. Penjumlahan (+)");
        System.out.println("2. Pengurangan (-)");
        System.out.println("3. Perkalian (*)");
        System.out.println("4. Pembagian (/)");

        System.out.print("Masukkan pilihan (1/2/3/4): ");
        int choice = scanner.nextInt();

        System.out.print("Masukkan angka pertama: ");
        double num1 = scanner.nextDouble();

        System.out.print("Masukkan angka kedua: ");
        double num2 = scanner.nextDouble();

        double result;

        switch (choice) {
            case 1:
                result = num1 + num2;
                System.out.println("Hasil: " + result);
                break;
            case 2:
                result = num1 - num2;
                System.out.println("Hasil: " + result);
                break;
            case 3:
                result = num1 * num2;
                System.out.println("Hasil: " + result);
                break;
            case 4:
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Hasil: " + result);
                } else {
                    System.out.println("Error: Pembagian dengan nol tidak diperbolehkan.");
                }
                break;
            default:
                System.out.println("Pilihan tidak valid.");
                break;
        }

        scanner.close();
    }
}
