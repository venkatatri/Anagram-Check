# Anagram-Check
Check the Strings is Anagram are Not.
package Pratice_programs;
import java.util.Scanner;
import java.util.Arrays;
public class Assignment2 
{
	    public static void main(String[] args) {
	        Scanner scanner = new Scanner(System.in);
	        System.out.print("Enter first string: ");
	        String str1 = scanner.nextLine().toLowerCase();

	        System.out.print("Enter second string: ");
	        String str2 = scanner.nextLine().toLowerCase();

	        boolean result = areAnagrams(str1, str2);
	        System.out.println("Are they anagrams: " + result);
	    }

	    public static boolean areAnagrams(String s1, String s2) {
	   
	        char[] arr1 = s1.replaceAll("\\s", "").toCharArray();
	        char[] arr2 = s2.replaceAll("\\s", "").toCharArray();

	   
	        if (arr1.length != arr2.length) {
	            return false;
	        }

	        // Sort and compare
	        Arrays.sort(arr1);
	        Arrays.sort(arr2);

	        return Arrays.equals(arr1, arr2);
	    }
	}
