import java.util.*;
class CombinationalCircuit
{

static String dec2bin(int i)
{
String str="";
for(int k=i; k!=0;k=k/2)
{
str=k%2+str;
}
int l=str.length();
while(l<3)
{
str="0"+str;
l=str.length();
}
return str;
}

public static void main() 
{
Scanner sc = new Scanner(System.in);
int i=0;
System.out.println("How do you want to enter the function output? Remember it has to be a 3 variable function!");
do
{
if(i!=4)
{
System.out.println();
System.out.println("1. Enter the output values in the truth table");
System.out.println("2. Enter the minterms manually");
System.out.println("Enter 0 to exit");
System.out.println();
}
try
{
i = Integer.parseInt(sc.nextLine());
}
catch(NumberFormatException e)
{
i=4;
}
ArrayList<Integer> arr=new ArrayList<Integer>(); 
switch(i)
{
case 1:
System.out.println("Enter corresponding values of F in the truth table.");
System.out.println();
System.out.println("A\tB\tC\tF(A,B,C)");
for(int j=0;j<8;j++)
{
int k; String s;
do
{
System.out.print("\n"+dec2bin(j).charAt(0)+"\t"+dec2bin(j).charAt(1)+"\t"+dec2bin(j).charAt(2)+"\t"); 
s=sc.next();
try
{
k=Integer.parseInt(s); 
if(k==1 || k==0)
{
if (k==1) arr.add(j);
}
else System.out.println("\nEnter either 0 or 1"); 
}
catch(NumberFormatException e)
{
System.out.println("\nEnter either 0 or 1");
}
}while(s.equals("0")==false && s.equals("1")==false);
}
break;
case 2:
System.out.println("Enter minterms. When you're done, enter 'done'");
System.out.println("When you enter any minterm greater than 7 or any wrong unacceptable input, it automatically stops entering further minterms and ignores the current one as well");
String s;
do
{
s=sc.next(); 
try{
arr.add(Integer.parseInt(s));
}
catch(NumberFormatException e)
{
break;
}
}
while(s.equalsIgnoreCase("done")==false && Integer.parseInt(s)<8);
break;
case 0:
System.out.println("Bye!");
break;
default:
System.out.println("Follow instructions. Enter either 1 or 2 or 0"); i=4;
break;
}
if (i==1 || i==2) 
{
int l=arr.size();
int ia[]=new int[l];
for(int m=0;m<l;m++)
{
ia[m]=arr.get(m);
}
Kmap ob= new Kmap();
System.out.println("\nMinimal SOP expression: F(A,B,C) = "+ob.mapsolver(ia));
}
System.out.println();
if(i==1 || i==2){
System.out.println("\nWanna try again? Type yes or no.");
System.out.println("Entering anything else will be assumed as a no!");
String s0=sc.next();
if (s0.equalsIgnoreCase("yes")) i=3;
else System.out.println("Bye!");
}
}while (i!=0 && i!=1 && i!=2);
}
}

