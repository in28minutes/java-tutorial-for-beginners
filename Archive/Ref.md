## 1

```
import java.util.Scanner;

public class UdemyCourseAccess {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Are you logged in? (yes/no): ");
        String loggedIn = scanner.nextLine();

        if (loggedIn.equalsIgnoreCase("yes")) {
            System.out.print("Are you enrolled in the in28Minutes course? (yes/no): ");
            String enrolled = scanner.nextLine();

            if (enrolled.equalsIgnoreCase("yes")) {
                System.out.println("Welcome to the in28Minutes Course!");
            } else {
                System.out.println("Please enroll in the in28Minutes course.");
            }
        } else {
            System.out.println("Please log in to Udemy.");
        }

        scanner.close();
    }
}
```


## 2

```
import java.util.Scanner;

public class UdemyCourseAccess {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Are you logged in? (1 for yes, 0 for no): ");
        int loggedIn = scanner.nextInt();

        if (loggedIn == 1) {
            System.out.print("Are you enrolled in the in28Minutes course? (1 for yes, 0 for no): ");
            int enrolled = scanner.nextInt();

            if (enrolled == 1) {
                System.out.println("Welcome to the in28Minutes Course!");
            } else {
                System.out.println("Please enroll in the in28Minutes course.");
            }
        } else {
            System.out.println("Please log in to Udemy.");
        }

        scanner.close();
    }
}
```