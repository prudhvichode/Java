# Java
Assignments -School

//Date Written - 02/08/2016
//Date Last Modified - 02/09/2016

//i am reading the number from left to right, so 4th 3rd 2nd 1st
//for example									  1   2   3   4

import java.util.Scanner;
public class Prudhvi_iAssignment1
{
    public static void main(String[] args) 
    {
        int x,num,a,b,c,d,encrypt,decrypt;
        
        Scanner keyboard = new Scanner(System.in);
        
        System.out.println("Enter 1 for Encrypt or enter 2 for Decrypt");
        x=keyboard.nextInt();
        
        if(x==1)
        {
        	System.out.println("Input a four digit number");
        	num=keyboard.nextInt();
        
        	a = (num/1000)%10;													//to seperate the 4th digit from the input number
        	b = (num/100)%10;													//to seperate the 3rd digit from the input number
        	c = (num/10)%10;													//to seperate the 2nd digit from the input number
        	d = num%10;															//to seperate the 1st digit from the unput number
        
        	a = (a+7)%10;														//to encrypt the 4th number by adding 7 and dividing by 10
        	b = (b+7)%10;														//to encrypt the 3rd number by adding 7 and dividing by 10
        	c = (c+7)%10;														//to encrypt the 2nd number by adding 7 and dividing by 10
        	d = (d+7)%10;														//to encrypt the 1st number by adding 7 and dividing by 10
        
        	encrypt = a;														//store value of a in a varaible "encrypt"
        	a=c;																//swap digit from 2nd to 4th
        	c = encrypt;														//from the stored value in "encrypt" it will copy in 2nd
        
        	System.out.println("Encrypted number: " +a +b +c +d);
        }
        if(x==2)
        {
        	System.out.println("Input a four digit number");
        	num=keyboard.nextInt();
        	
        	a = (num/1000)%10;													//to seperate the 4th digit from the input number
        	b = (num/100)%10;													//to seperate the 3rd digit from the input number
        	c = (num/10)%10;													//to seperate the 2nd digit from the input number
        	d = num%10;															//to seperate the 1st digit from the input number
        
        	decrypt = c;														//store the 2nd value to a varialbe "decrypt"
        	c=a;																//Swap digit from 4th to 2nd
        	a = decrypt;														//copy number from the "decrypt" in 4th
        	
        	a = ((a+10)-7)%10;													//add 10 to 4th digit and subtract it from 7 and take mod of 10
        	b = ((b+10)-7)%10;													//add 10 to 3rd digit and subtract it from 7 and take mod of 10
        	c = ((c+10)-7)%10;													//add 10 to 2nd digit and subtract it from 7 and take mod of 10
        	d = ((d+10)-7)%10;													//add 10 to 1st digit and subtract it from 7 and take mod of 10
        
        	System.out.println("Decrypted number: " +a+ " "+b+ " "+c+ " "+d);
        }
        if(x!=1 || x!=2)
        {
        	System.out.println("Invalid Input");								//if the user doesn't input 1 or 2 than this sign will be displayed
        }
    }
}
