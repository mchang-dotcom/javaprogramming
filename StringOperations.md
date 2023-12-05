# javaprogramming
Oriented Programming with Java
by Min Chang

public class StringOperations {
    public static void main(String[] args) {
        String myName = "Min";
        System.out.println(myName);

        String alteredName = 'A' + myName.substring(1, myName.length() - 1) + 'Z';
        System.out.println(alteredName);

        String webAddress = "www.stackoverflow.com";
        System.out.println(webAddress);

        String nameSection = webAddress.substring(4, webAddress.lastIndexOf('.'));
        String finalOutput = nameSection + "1331";
        System.out.println(finalOutput);
    }
}
