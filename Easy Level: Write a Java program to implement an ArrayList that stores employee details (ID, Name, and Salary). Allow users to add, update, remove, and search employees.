import java.util.*;

class Employee {
    int id;
    String name;
    double salary;

    Employee(int id, String name, double salary) {
        this.id = id;
        this.name = name;
        this.salary = salary;
    }

    public String toString() {
        return id + " " + name + " " + salary;
    }
}

public class EmployeeManagement {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ArrayList<Employee> employees = new ArrayList<>();
        while (true) {
            System.out.println("1. Add 2. Update 3. Remove 4. Search 5. Exit");
            int choice = sc.nextInt();
            if (choice == 5) break;
            switch (choice) {
                case 1:
                    System.out.println("Enter ID, Name, Salary:");
                    employees.add(new Employee(sc.nextInt(), sc.next(), sc.nextDouble()));
                    break;
                case 2:
                    System.out.println("Enter ID to update:");
                    int updateId = sc.nextInt();
                    for (Employee e : employees) {
                        if (e.id == updateId) {
                            System.out.println("Enter new Name, Salary:");
                            e.name = sc.next();
                            e.salary = sc.nextDouble();
                            break;
                        }
                    }
                    break;
                case 3:
                    System.out.println("Enter ID to remove:");
                    int removeId = sc.nextInt();
                    employees.removeIf(e -> e.id == removeId);
                    break;
                case 4:
                    System.out.println("Enter ID to search:");
                    int searchId = sc.nextInt();
                    for (Employee e : employees) {
                        if (e.id == searchId) {
                            System.out.println(e);
                            break;
                        }
                    }
                    break;
            }
        }
        sc.close();
    }
}
