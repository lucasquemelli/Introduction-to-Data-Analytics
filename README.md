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

#Try except specific example

a = 1

try:
    b = int(input("Please enter an integer number to divide a"))
    a = a/b
    print("Success a=",a)
except ZeroDivisionError:
    print("The number you provided cannot divide because it is 0")
except ValueError:
    print("You did not provide an integer or a number")
except:
    print("Something went wrong")
        
#Try except else and finally example

a = 1

try:
    b = int(input("Please enter an integer to divide a"))
    a = a/b
except ZeroDivisionError:
    print("The number you provided cant divide 1 because it is 0")
except ValueError:
    print("You did not provide a number")
except:
    print("Something went wrong")
else:
    print("success a=",a)
finally:
    print("Processing Complete")

# Classes and Objects

#You have been recruited by your friend, a linguistics enthusiast, to create a utility tool that can perform analysis on a given piece of text. Complete the class 'analysedText' with the following methods -

Constructor - Takes argument 'text',makes it lower case and removes all punctuation. Assume only the following punctuation is used - period (.), exclamation mark (!), comma (,) and question mark (?). Store the argument in "fmtText"
freqAll - returns a dictionary of all unique words in the text along with the number of their occurences.
freqOf - returns the frequency of the word passed in argument.

class analysedText(object):
    
    def __init__ (self, text):
        pass
    
    def freqAll(self):        
        pass
    
    def freqOf(self,word):
        pass
        
#Try of the previous exercise

class analysedText(object):
    # Constructor
    def __init__ (self, text):
        text.lower()
        text.split()
        text.split('.')
        text.split('!')
        text.split(',')
        text.split('?')
        fmtText = text
        pass
    
    def freqAll(self):        
        j = 0
        for i in text:
            Dict = {"key[j]": text[i]}
            j = j + 1
            return(Dict)
        k = 0
        n = 0
        for i in Dict:
            b = 0
        for i in Dict:
            while(Dict[k] != Dict[i]):
                b = b + 1
                return(Dict2)
                if (b == len(Dict)):
                Dict2 = {"key[n]": Dict[k]}
                n = n + 1
                print("The word",Dict2[k],"appears only once!")
            else:
                Dict3 = {"key[k]": Dict[k]}
                c[k] = len(Dict) - b
                print("Do nothing")
            return(Dict)
        k = k + 1
        return(Dict)
        pass
    
    def freqOf(self,word):
        for i in Dict3:
            print("The word ",Dict3[i]," appears ",c[i],"times!")    
        pass
        
        
        
        #Last try
        
        class analysedText(object):
    # Constructor
    def __init__ (self, text):
        text.lower()
        text.split()
        text.split('.')
        text.split('!')
        text.split(',')
        text.split('?')
        fmtText = text
        pass
    
    def freqAll(self):        
        j = 0
        for i in text:
            Dict = {"key[j]": text[i]}
            j = j + 1
            return(Dict)
        k = 0
        n = 0
        for i in Dict:
            b = 0
        for i in Dict:
            while(Dict[k] != Dict[i]):
                b = b + 1
                return(Dict2)
            if (b == len(Dict)):
                g = 1
                Dict2 = {"key[n]": Dict[k]}
                Dict3 = {"Dict[k]": g}
                n = n + 1
                print("Dict3[k]")
            else:
                Dict4 = {"key[k]": Dict[k]}
                c[k] = len(Dict) - b
                print("Do nothing")
                Dict5 = {"Dict[k]": c[k]}
                 return(Dict)
        k = k + 1
        return(Dict)
        pass
    
    def freqOf(self,word):
        for i in Dict3:
            print("The word ",Dict3[i]," appears ",c[i],"times!")    
        pass
        
#The solution:

class analysedText(object):
    
    def __init__ (self, text):
        # remove punctuation
        formattedText = text.replace('.','').replace('!','').replace('?','').replace(',','')
        
        # make text lowercase
        formattedText = formattedText.lower()
        
        self.fmtText = formattedText
        
    def freqAll(self):        
        # split text into words
        wordList = self.fmtText.split(' ')
        
        # Create dictionary
        freqMap = {}
        for word in set(wordList): # use set to remove duplicates in list
            freqMap[word] = wordList.count(word)
        
        return freqMap
    
    def freqOf(self,word):
        # get frequency map
        freqDict = self.freqAll()
        
        if word in freqDict:
            return freqDict[word]
        else:
            return 0
    
# Write and save files in Python

Your local university's Raptors fan club maintains a register of its active members on a .txt document. Every month they update the file by removing the members who are not active. You have been tasked with automating this with your Python skills.
Given the file currentMem, Remove each member with a 'no' in their Active coloumn. Keep track of each of the removed members and append them to the exMem file. Make sure the format of the original files in preserved. 

def cleanFiles(currentMem,exMem):
    with open(currentMem,'r+') as writeFile: 
        with open(exMem,'a+') as appendFile:
            #get the data
            writeFile.seek(0)
            members = writeFile.readlines()
            #remove header
            header = members[0]
            members.pop(0)
                
            inactive = [for member in members if ('no' in member)]
            
            writeFile.seek(0) 
            writeFile.write(header)
            for member in members:
                if (member in inactive):
                    appendFile.write(member)
                else:
                    writeFile.write(member)      
            writeFile.truncate()
                
memReg = 'members.txt'
exReg = 'inactive.txt'
cleanFiles(memReg,exReg)

headers = "Membership No  Date Joined  Active  \n"

with open(memReg,'r') as readFile:
    print("Active Members: \n\n")
    print(readFile.read())
    
with open(exReg,'r') as readFile:
    print("Inactive Members: \n\n")
    print(readFile.read())
    
# One Dimensional Numpy

Implement the following vector subtraction in numpy: u-v

#Write your code below and press Shift+Enter to execute

u = np.array([1, 0])
v = np.array([0, 1])

z = u - v
z

Multiply the numpy array z with -2:

#Write your code below and press Shift+Enter to execute

z = np.array([2, 4])

w = z*2
w

Consider the list [1, 2, 3, 4, 5] and [1, 0, 1, 0, 1]. Cast both lists to a numpy array then multiply them together:

#Write your code below and press Shift+Enter to execute

a = np.array([1,2,3,4,5])
b = np.array([1,0,1,0,1])
c = a*b
c

Convert the list [-1, 1] and [1, 1] to numpy arrays a and b. Then, plot the arrays as vectors using the fuction Plotvec2 and find their dot product:

#Write your code below and press Shift+Enter to execute

a = np.array([-1, 1])
b = np.array([1, 1])
Plotvec2(a,b)
c = np.dot(a,b)
c

![image](https://user-images.githubusercontent.com/81119854/122645769-63cd6400-d0f2-11eb-8442-ea40fb400e61.png)


# Here is a link with commonly-used pre-defined functions in Python: 

https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%203/Python_reference_sheet.pdf?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkPY0101ENSkillsNetwork19487395-2021-01-01


