# MinElementChallenge
package com.company;

import java.util.Arrays;
import java.util.Scanner;

public class Main {

    private static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {

        System.out.println("Enter count:");
        int count = scanner.nextInt();
        scanner.nextLine();

        int[] returnedArray = readInteger(count);

        int returnedMin = findMin(returnedArray);

        System.out.println("min = " + returnedMin);


    }

    private static int[] readInteger(int count) {

        int[] array = new int[count];

        for (int i = 0; i < array.length; i++) {
            System.out.println("Enter number");
            int number = scanner.nextInt();
            scanner.nextLine();
            array[i] = number;
        }
        return array;
    }

    private static int findMin(int[] array) {

        int min = Integer.MAX_VALUE;

        for (int i = 0; i < array.length; i++) {
            int value = array[i];

            if (value < min) {
                min = value;
            }
        }
        return min;
    }

}
/Library/Java/JavaVirtualMachines/amazon-corretto-11.jdk/Contents/Home/bin/java "-javaagent:/Applications/IntelliJ IDEA CE.app/Contents/lib/idea_rt.jar=55602:/Applications/IntelliJ IDEA CE.app/Contents/bin" -Dfile.encoding=UTF-8 -classpath /Users/Bilaal/IdeaProjects/MinElementChallenge/out/production/MinElementChallenge com.company.Main
Enter count:
4
Enter number
4
Enter number
66
Enter number
7
Enter number
23
min = 4

Process finished with exit code 0
