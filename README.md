# Account

Program #1 (25 points): Design and implement a Java class, named Account. The class defines the
following data fields and methods:
1. Private int data field named id to store the account ID (default value is 0).
2. Private double data field named balance to store the account balance (default value is 0.0).
3. Private double data field named annualInterestRate to store the interest rate (default value is 0.0%).
(Assume all accounts have the same interest rate. The annual interest rate is percentage such as 3.2%,
thus you need to divide by 100 to get double value 0.032).
4. Private Date data field named dateCreated (an object of class Date) to store the date when the account
was created.
5. Non-argument constructor method that creates a default account (with default values).
6. Constructor method that creates an account with specified ID and initial balance.
7. Get and Set methods for variables id, balance, and annualInterestRate.
8. Get method for variable dateCreated.
9. Method named getMonthlyInterestRate() that returns the monthly interest rate as double value (i.e.,
annualInterestRate / 12). The monthly interest rate is formatted as percentage (%) when displayed.
10. Method named getMonthlyInterest() that returns the earned monthly interest amount as double value
(i.e., balance * monthlyInterestRate). The monthly interest amount is formatted as currency ($)
when displayed.
11. Method named withdraw() that withdraws a specific amount from the account.
12. Method named deposit() that deposits a specific amount to the account.
In a separate file, write a test program (named TestAccount) to create an account object named myObject
as follows:
- Account ID is 123456; Initial balance is $10,000, annual interest rate is 2.5%.
- Withdraw $3,500
- Deposit $500
- Print out the account balance
- Print out the earned monthly interest
Page 2 of 4
- Print out the date the account was created
Now, add method toString()to class Account to allow the user to printout a meaningful description of an
account object using all of its instance variables. For example, the following statement in the test program
System.out.print(myObject);
on object myObject would display the account information as follows. Make sure your code displays the
outputs following the test data format.
Account ID: 123456
Account Balance: $7,000.00
Annual Interest Rate: 2.5%
Monthly Interest: $14.58
Date Opened: Wed Jul 06 10:35:04 EDT 2022
Here is an example of toString()method for a student object:
//-----------------------------------------------------------------------------
// Returns a string representation of student object using name and studentID.
//-----------------------------------------------------------------------------
public String toString(){
// name and studentID are instance variables in class Student
return ("The student name is " + name + ", and the ID is " + studentID);
}
Now, modify the test program above to create 2 more account objects (say myAccount and yourAccount)
with different initial balance values and different interest rates. Allow the user to enter the object values. Test
all class methods on at least one object in a logical order and display meaningful information about the object
after each method call. Use a sentinel loop to allow re-runs and re-create those objects with different values.
Handle account overdraft issue with proper error message.
Document your code and organize and space the outputs properly. Use escape characters and formatting
objects ($ and %) as needed.
Note: To show the fraction part of the Interest rate value as 2.5%, you need to set the fraction digits of the
formatting object fmt as follows:
 fmt.setMinimumFractionDigits(1);
Here is an example:

import java.text.NumberFormat;
. . .
Double rate = 0.05275; //rate is 5.275%
NumberFormat fmt = NumberFormat.getPercentInstance();
fmt.setMaximumFractionDigits(1);
System.out.println(fmt.format(rate));
