/*
 * This Code Takes a Integer and a String input from the user, removes the Duplicate entries and outputs the Distinct values
 * in a sorted fashion.
 * This will convert all the numbers to lowercase before removing the Duplicates.
 * As it was not mentioned particularly to check for Upper and lower case letters 
 * this program will consider two same strings with different cases as same.Thus resulting only one of the two strings in Lowecase
 * 
 */
/*
 * 
 * --Authored by Lakshmana Deepesh.--
 * 
 * */
package problem_1;

import java.util.ArrayList;
import java.util.Collections;
import java.util.List;
import java.util.Scanner;

public class Main 
{
	public static void main(String[] args) 
	{
		@SuppressWarnings("resource")
		Scanner x= new Scanner(System.in);
		/*--------This Block inputs the integer N ------*/
		System.out.println("Enter the number of Strings (N):");
		/* this while loop prevents the runtime exception of data-type mismatch.
		 * In case where the user enters the string instead of a number
		 */
		while(!x.hasNextInt())
		{
			System.out.println("Illegal entry,Please enter a Integer value");
			System.out.println("Enter the number of Strings (N):");
			x.next();
		}
		int N =x.nextInt();//The integer enterd by user is assigned to a internal int variable
		/*----------Integer block Ends here---------------------*/
		/*----------This Block of code is for inputting the Strings----*/
		String[] Inputs=new String[N];
		System.out.println();
		System.out.println("Enter the "+N+" Strings,Each followed by enter key:");

		for(int i=0;i<N;i++)
		{
			Inputs[i]=x.next();//the inpur Strings are stored in a String Array
		}
		/*--------------------String Code Ends Here------------------*/
		for(int h=0;h<N;h++)
		{
			Inputs[h]=Inputs[h].toLowerCase();//This converts the string to lower case
		}
		deletedups(Inputs);//Calling the deletedups method to delete the duplicates in the Strings
	}
	/*This Method takes a String Array as an Argument
	 * and uses the ArrayList function in the Java.util Libriary and removes 
	 *the Duplicate strings in a String Array.
	 */
	public static void deletedups(String[] arr)
	{

		List<String> arrList = new ArrayList<String>();//A new ArrayList is created
		int count= 0;//The Counter is assigned and initialised to zero

		/*This is the iteration that is used to compare each string in the array and it increments the Count.
		 * if the count is less than one then that particular string will be added to the array List*/
		for(int i=0;i<arr.length;i++){
			for(int j=i+1;j<arr.length;j++){
				if(arr[i].equals(arr[j])){
					count++;//incrementing the count if a duplicate is found.
				}                
			}
			if(count<1){
				arrList.add(arr[i]);//adding that non duplicate value to the Array List.
			}
			count=0;//re-seting the Count to zero for next iteration.
		}
		Collections.sort(arrList.subList(0, arrList.size()));//This Collections functions sorts the ArrayList
		System.out.println("Unique Strings are ");
		//This for loop helps in printing the non-duplicate distinct Strings
		for(int k=0;k<arrList.size();k++)
		{
			System.out.println(arrList.get(k));//This Prints the values

		}
	}


}

