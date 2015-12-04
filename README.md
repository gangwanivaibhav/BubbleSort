//# BubbleSort
//Bubble Sort in java using methods, taking input from user for valid input only using exception handling
import java.util.*;
class Bubble{
	public static void main(String [] args){
		Scanner in = new Scanner (System.in);
		try{
		System.out.println("Enter length of array");
		int size = in.nextInt();
		int[]unsortedArray = new int [size];	
		
		System.out.println("Enter Array");
		for(int c=0;c<=size-1;c++){
			unsortedArray[c] = in.nextInt(); 
		}
	
		int [] sortedArray = sortArray(unsortedArray,size);
		
		System.out.println("Bubbled up array is");
		printSortedArray(sortedArray,size);
		
		}catch(InputMismatchException e){
			System.out.println("You can enter valid number only");
		}
	}
	
	public static int [] sortArray(int [] list,int size){	
	int temp;
	for(int p=0;p<=size-1;p++){
			for(int c=0;c<size-p-1;c++)
			{
			if(list[c]>list[c+1])
			{
			temp = list[c];
			list[c] = list[c+1];
			list[c+1] =temp;
			}
			}
		}
		return list;
		}
	public static void printSortedArray(int [] sortedArray,int size){
		for(int c=0;c<=size-1;c++){
			System.out.println(sortedArray[c]);
		}
	}	
}
