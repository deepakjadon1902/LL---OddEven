import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();
        }

        int[] odd = new int[n];
        int[] even = new int[n];
        int oddIndex = 0, evenIndex = 0;

        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0) {
                even[evenIndex++] = arr[i];
            } else {
                odd[oddIndex++] = arr[i];
            }
        }

        for (int i = 0; i < oddIndex; i++) {
            System.out.print(odd[i] + " ");
        }
        for (int i = 0; i < evenIndex; i++) {
            System.out.print(even[i] + " ");
        }
    }
}
