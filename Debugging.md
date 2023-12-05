# javaprogramming
Oriented Programming with Java

// Bad1.java

public class Bad1 {
    public static void main(String[] args) {
        String str = new String("CS1331ROCKS");
        System.out.println((str.length() - 5) + " is 11 - 5");
    }
}



// Bad2.java

public class Bad2 {
    public static void main(String[] args) {
        int a = 1331;
        int b = 0;
        System.out.println("Welcome to \nCS 1331!");
        if (b != 0) {
            int c = a / b;
            System.out.println("c is equal to: " + c);
        } else {
            System.out.println("Cannot divide by zero");
        }
    }
}



// Bad3.java

public class Bad3 {
    public static void main(String[] args) {
        String letter = "a";
        System.out.println("letter is " + letter);
    }
}
