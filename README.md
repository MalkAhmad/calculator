#include <iostream>
#include<math.h>
#include<bitset>
#include<cmath>
#include<string>
using namespace std;


int convertToBinary(std::string str_num) {
	int binary;
	binary = (int)std::bitset<64>(str_num).to_ulong();
	return binary;
}

// function of conversion  process

void conversion()
{

	// menu to the user to choose the type of conversion
	cout << "choose ur input system \n" << '\a';
	cout << " 1=hex to binary        7=dec to octal \n";
	cout << " 2=hex to oct           8=dec to hex \n";
	cout << " 3=hex to decimal       9=dec to binary\n";
	cout << " 4=oct to binary        10=binary to hex \n";
	cout << " 5=oct to dec           11=binary to dec   \n";
	cout << " 6=oct to hex           12=binary to oct\n";

	int convert;    // switch choice

	string myBinaryNum;		//the binary number that will be converted
	long long result;       // needed in binary 
	long long num1;			// the user input in all the system 
	cin >> convert;
	switch (convert)
	{
	case 1:		// hex to binary
		cout << "enter your hex number\n";
		cin >> hex >> num1;
		cout << "the binary number is=" << bitset<16>(num1) << '\a' << endl;
		break;
	case 2:		// hex to octal
		cout << "enter your hex number\n";
		cin >> hex >> num1;
		cout << "the octal number is=" << oct << num1 << '\a' << endl;
		break;
	case 3:		// hex to decimal
		cout << "enter your hex number\n";
		cin >> hex >> num1;
		cout << "the decimal number is=" << dec << num1 << '\a' << endl;
		break;
	case 4:		// octal to binary 
		cout << "enter your oct number\n";
		cin >> oct >> num1;
		cout << "the binary number is=" << bitset<16>(num1) << '\a' << endl;
		break;
	case 5:		//octal to decimal
		cout << "enter your oct number\n";
		cin >> oct >> num1;
		cout << "the dec number is=" << dec << num1 << '\a' << endl;
		break;
	case 6:		//octal to hex 
		cout << "enter your oct number\n";
		cin >> oct >> num1;
		cout << "the hex number is=" << hex << num1 << '\a' << endl;
		break;
	case 7:		// decimal to oct
		cout << "enter your dec number\n";
		cin >> dec >> num1;
		cout << "the oct number is=" << oct << num1 << '\a' << endl;
		break;
	case 8:		//decimal to hex 
		cout << "enter your dec number\n";
		cin >> dec >> num1;
		cout << "the hex number is=" << hex << num1 << '\a' << endl;
		break;
	case 9:		//decimal to binary 
		cout << "enter your dec number\n";
		cin >> dec >> num1;
		cout << "the binary number is=" << bitset<16>(num1) << '\a' << num1 << endl;
		break;
	case 10:	//binary to hex 
		cout << "enter the binary number : ";
		cin >> myBinaryNum;
		result = convertToBinary(myBinaryNum);
		cout << "The Hex conversion of your number is: " << hex << result << '\a' << endl;

		break;
	case 11:	// binary to decimal 
		cout << "enter the binary number : ";
		cin >> myBinaryNum;
		result = convertToBinary(myBinaryNum);
		cout << "The Dec conversion of your number is: " << dec << result << '\a' << endl;
		break;
	case 12:	// binary to octal
		cout << "enter the binary number : ";
		cin >> myBinaryNum;
		result = convertToBinary(myBinaryNum);
		cout << "The octal conversion of your number is: " << oct << result << '\a' << endl;
		break;
	default:
		cout << "enter a number form 1-12!!!!!" << '\a' << endl;
	}

}
// function of calculation process

void calulation()

{
	int mybinary_num_int;
	int mybinary_num2_int;
	int result;
	string mybinary_num;
	string mybinary_num2;

	int firsthexnumber, secondhexnumber;
	int firstoctalnumber, secondoctalnumber;
	int firstdecnumber, seconddecnumber;
	// menu to the user to choose the  numbring system of the  summation 
	cout << "choose ur system \n" << "1=dec\n" << "2=oct\n" << "3=hexa\n" << "4=binary\n" << '\a';
	// enter the type of the system according to its number in the menu
	int system;
	cin >> system;
	// switch statment to choose between the numbring system to sum 
	switch (system) {
	case 1:		  //adding decimal numbers 


		cout << "enter the  first decimal  number \n";
		cin >> firstdecnumber;                   // enter first number in decimal 
		cout << "enter the second decimal  numbe r\n";       // enter second  number in decimal  
		cin >> seconddecnumber;
		cout << " there sum equal : " << firstdecnumber + seconddecnumber << '\a' << endl;  // print the sum in decimal 

		break;
	case 2:				 // adding octal number


		cout << " enter the first octal number :  ";
		cin >> oct >> firstoctalnumber;
		cout << " enter the second octal number :  ";
		cin >> oct >> secondoctalnumber;
		cout << "there sum equal :  " << oct << firstoctalnumber + secondoctalnumber << '\a' << endl;    // need work (/*means it may be apart of the code */

		break;
	case 3:			  // adding hexadecimal number 


		cout << " enter the first hexadecimal number :  ";
		cin >> hex >> firsthexnumber;
		cout << " enter the second  hexadecimal number :  ";
		cin >> hex >> secondhexnumber;
		cout << "there sum equal :  " << hex << firsthexnumber + secondhexnumber << '\a' << endl;

		break;

	case 4: // adding binary number 

		cout << "Please enter the first number" << endl;
		cin >> mybinary_num;
		mybinary_num_int = convertToBinary(mybinary_num);
		cout << "Please enter the second number" << endl;
		cin >> mybinary_num2;
		mybinary_num2_int = convertToBinary(mybinary_num2);
		result = mybinary_num_int + mybinary_num2_int;
		cout << "there sum equal :  " << bitset<16>(result) << '\a' << endl;

		break;
	default:
		cout << " enter 1 , 2 ,3 or  4  according to the number of the numbering system  in the previous list \n "; 
	}
}

// the main code function 
int main()
{
	
		system("color 7D");
		// introduction to the user 
		cout << "                              Programmer Calculator!!!                                     \n";
		cout << " choose your operation\n" << "1=converstion       2=calculation \n" << '\a';  //the menu which the user should choose the operation from either convertion or calculator

		int operation;

		cin >> operation;               //the user enter either 1 or 2 

		// switch statment to manage the choice  of  the type of operation either convertion or calculation   

		switch (operation) {
		case 1:

			conversion(); // conversion is function to be processed
			break;

		case 2:

			calulation(); //calculation is function to be processed
			break;

		default:
			cout << " please enter 1 or 2 according to your choice "; 

		}
	
	return 0;

}
