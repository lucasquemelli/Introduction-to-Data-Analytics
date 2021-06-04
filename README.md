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

