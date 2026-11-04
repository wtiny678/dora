#value error 
import math
x=int(input("Enter a positive number:"))
try:
    ans=math.sqrt(x)
    print("The squareroot of given number is",ans)
except ValueError as ve:
    print("Value Error....")



#INDEX ERROR
mytuple=(1,2,3,4,5,6,7,8)
index=int(input("Enter a index value:"))
try:
    element=mytuple[index]
    print("The element at",index,"is",element)
except IndexError as ie:
          print("Index value occured",ie)
#NAME ERROR
x=int(input("Enter a number A:"))
y=int(input("Enter a number B:"))
try:
    sum=x+y
    print("The sum is",sum1)
except NameError as NE:
    print("Name Error Occured")



#TYPE ERROR
x=int(input("Enter a Number:"))
y=input("Enter a Value:")
try:
    print(x+y)
except TypeError as te:
    print("Datatype error",te)



#ZERODIVISION ERROR
try:
    x=int(input("Enter a number A:"))
    y=int(input("Enter a number B:"))
    z=x/y
    print("The didivied number is",z)
except ZeroDivisionError as zde:
    print("ZeroDivision Error occured")



#sUSER DEFINED ERROR,ELSE FINALLY,RAISE ERROR

class AgeException(Exception):
    pass

age = int(input("Enter your age: "))

try:
    if age >= 18:
        print("Eligible to Vote")
    else:
        raise AgeException

except AgeException:
    print("Not Eligible to Vote")

else:
    print("Age verified successfully")

finally:
    print("Program executed successfully")


# AGE VERIFICATION 


class AgeException(Exception):
    pass

age = input("Enter your age: ")

try:
    if age.isdigit() and 1 <= len(age) <= 3:
        print("Valid Age")
    else:
        raise AgeException

except AgeException:
    print("Invalid Age")

else:
    print("Verified successfully")

finally:
    print("Program executed successfully")

