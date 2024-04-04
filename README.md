# Python-work
 # Lambda Function
 sqrt=lambda x: x**2

sqrt(8)

is_even=lambda x: x%2==0
is_even(2)
is_even(21)

x=["Java","python","C","CPP","Perl","Javascript"]

sorted_words=sorted(x,key=lambda x: len(x))
print(sorted_words)

fib=lambda n: n if n<=1 else fib(n-1)+fib(n-2)     # Fibonacci Series Program
[fib(i) for i in range(10)]

fact= lambda x : 1 if x==1 else x*fact(x-1)         # Factorial program
print(fact(6))

## Map Fuction->executes a specified function for each of items of an iterable
#Syntax->map(func, *iterables) --> map object
help(map)
l=[1,2,3,4,5]
def square(l):
  sq=[]
  for i in l:
    sq.append(i*i)
  return sq

square(l)

def sq(a):
  return a*a
list(map(sq,l))

name=["ankit","kumod","ashish"]
greet=lambda x: print("hello",x)
list(map(greet,name))

list(map(lambda x:x+10,l))

l1=["1","2","100","45"]
convert=lambda l:int(l)
list(map(convert,l1))

list(map(lambda a:int(a),l1))

l1=[1,2,3,4,5]
l2=[100,101,102,103,104]
list(map(lambda x,y:x+y,l1,l2))

x="ankitshah"
list(map(lambda name:name.upper(),x))

# Calculate_CGPA
list_grades=["A","B","C","D","E"]
list(map(lambda grade: 4 if grade=="A"else (3 if grade=="B" else 2),list_grades))



## Reduce Function -> folding or reductions.
from functools import reduce
marks=[23,43,54,12,56]
reduce(lambda x,y:x+y,marks)


def add(x,y):
  return x+y
reduce(add,marks)

# Reduce in Strings
words=["ankit","shah","name"]
reduce(lambda x,y: x ," ",y,words)

#Factorial through reduce
def factorial(n):
  return reduce(lambda x,y:x*y,range(1,n+1))
factorial(5)
