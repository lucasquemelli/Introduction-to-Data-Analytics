# Introduction-to-Data-Analytics

# Conditions-Statement
It is a repository of the codes about conditions statements I have done in the "Introduction to Data Analytics" course.

  Conditions Statements 
#Write an if statement to determine if an album had a rating greater than 8. Test it using the rating for the album “Back in Black” that had a rating of 8.5. If the statement is true print "This album is Amazing!"

#Album rating for Back in Black
album_rating = 8.5

if(album_rating > 8):
print("This album is Amazing!")
else:
print("Not that amazing...")

#Write an if-else statement that performs the following. If the rating is larger then eight print “this album is amazing”. If the rating is less than or equal to 8 print “this album is ok”.

#Album rating for Back in Black
album_rating = 8.05

if(album_rating > 8):
print("This album is Amazing!")
else:
print("This album is ok")

#Write an if statement to determine if an album came out before 1980 or in the years: 1991 or 1993. If the condition is true print out the year the album came out.

album_year = 1992

if(album_year < 1980):
print("The album came out in the 1970's! It was in:",album_year)
elif (album_year == 1991) or (album_year == 1993):
print("The album came out in:", album_year,"!")
else:
print("The album did not come out in the 1970's and neither did in 1991 or 1993, it came out in:", album_year)

# Loops-in-Python-3

#Write a for loop the prints out all the element between -5 and 5 using the range function.

range(-5,6)
for i in range(-5,6):
    print(i)
    
#Print the elements of the following list: Genres=[ 'rock', 'R&B', 'Soundtrack', 'R&B', 'soul', 'pop'] Make sure you follow Python conventions.

Genres=[ 'rock', 'R&B', 'Soundtrack', 'R&B', 'soul', 'pop']

N = len(Genres)

for i in range(N):
    print(Genres[i])
    
#Write a for loop that prints out the following list: squares=['red', 'yellow', 'green', 'purple', 'blue']

squares=['red', 'yellow', 'green', 'purple', 'blue']

N = len(squares)

for i in range(N):
    print(squares[i])
    
#Write a while loop to display the values of the Rating of an album playlist stored in the list PlayListRatings. If the score is less than 6, exit the loop. The list PlayListRatings is given by: PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]

PlayListRatings = [10, 9.5, 10, 8, 7.5, 5, 10, 10]

i = 0
Rating = PlayListRatings[0]

while(Rating > 6):
    print(Rating)
    i = i + 1
    Rating = PlayListRatings[i]
    
print("Index", i,"presented a rating of:",Rating)    

#Write a while loop to copy the strings 'orange' of the list squares to the list new_squares. Stop and exit the loop if the value on the list is not 'orange':

squares = ['orange', 'orange', 'purple', 'blue ', 'orange']
new_squares = []

i = 0

while(squares[i] == 'orange'):
    new_squares.append(squares[i])
    print(new_squares[i])
    i = i + 1
    
print("Index", i,"presented a string different of orange!")

# Functions in Python

#This is an example of a function

def add(a):       #keyword: def; #name: add; #parameter: a.
    b = a + 1     #here begins the indent and it will be finished on line 99; #these three lines are called "the body" of the function". 
    print(a, "if you add one", b)
    return(b)
    
#A manner of calling the previous function is:

add(1) #this will assign the value 1 to the variable a. Thus, the result will be 2.

#Another way of calling the funcion named "add" is by doing:

add(2) #this will result in 3.

#Let's pay attention to the next function that multiplies two numbers:

def Mult(a, b):
    c = a * b
    return(c)
    print('This is not printed')
    
result = Mult(12,2)
print(result)

#Obviously, the result of the previous function is 24. Not that difficult and neither interesting... But the attention goes to the command "print". The string 'This is not printed' actually was not printed - only the result 24. Think about it!

#The last function 'Mult' can be used to multiply integers, floats and even strings. In the last case, the string will be repeated the times you want. But only works when we use an integer to multiply a string - not a float, I mean. Example:

Mult(2, "Lucas Quemelli")

#We may call variables of a local and a global manner

#Local manner

def square(a):
    
    # Local variable b
    b = 1
    c = a * a + b
    print(a, "if you square + 1", c) 
    return(c)

#Global manner

x = 3

#Makes function call and return function a y

y = square(x)
y                                            

#In this manner, we defined the variable 'x' and the function 'y'. The variable 'x' is a parameter of the function 'y'. Both of them                                              are part of the same set of codes. Because of this, if we set a different value for 'x', the function 'y' will return the result as                                              (x*x + 1).

#When there is not return statement, the function return none as may be seen: 

def LQ():
    print('Lucas Quemelli')
    
def LQ1():
    print('Lucas Quemelli')
    return(None)
    
#See the output

LQ()

#See the output

LQ1()

#Printing the function after a call reveals a "none" is the default return statement:

print(LQ())
print(LQ1())

#We can concatenate two strings using a function con:

def con(a, b):
    return(a + b)
con("This ", "is!")

#We may use a loop for printing every element in a function, such as:

def PrintList(the_list):
    for element in the_list:
        print(element)
        
PrintList(['1', 1, 'the man', "abc"])

#Come up with a function that divides the first input by the second input:

def div(a,b):
    c = a/b
    return(c)
    
result = div(8,2)
print(result)

#Use the function con for concatenating two variables.

def con(a, b):
    return(a + b)
result = con("Lucas ","Quemelli")
print(result)

#Can the con function we defined before be used to add two integers or strings?

def con(a, b):
    return(a + b)
result = con("2","7")
print(result)

#Can the con function we defined before be used to concatenate lists or tuples?

#List

def con(a, b):
    return(a + b)
L1 = [2,3,4]
L2 = [5,6,7]
result = con(L1,L2)
print(result)

#Tuple

def con(a, b):
    return(a + b)
T1 = (9,8,7)
T2 = (6,5,4)
result = con(T1,T2)
print(result)

# Exception Handling

#Try except example: in this example we are trying to divide a number given by the user, save the outcome in the variable a, and then we would like to print the result of the operation.

a = 1

try:
    b = int(input("Please enter a number to divide a"))
    a = a/b
    print("Success a=",a)
except:
    print("There was an error")
        
#Note that the input 'b' must be an integer.
#Note that it is not possible to insert a float or zero (as an integer). 

# Here is a link with commonly-used pre-defined functions in Python: 

https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%203/Python_reference_sheet.pdf?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkPY0101ENSkillsNetwork19487395-2021-01-01


