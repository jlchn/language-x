> for shell, please refer to [shell cheatsheet](shell-cheatsheet.md)

# basic types, operators, expressions

# control flow

## if, if else, else if

- python 

``` python
# if, elif, else, and, or
flag_1 = 'a'
flag_2 = 'd'
if flag_1 == 'a' and flag_2 == 'd':
    print('best')
elif flag_1 == 'a' or flag_2 == 'd':
    print('not so good')
else:
    print('bad')

fruit = ['banana' , 'apple']

# in, not in
if 'apple' in fruit:
    print('yes')
if 'orange' not in fruit:
    print('yes')

# is list empty
empty_list = []

if empty_list:
    print(empty_list)
else:
    print('it is empty')

```

## loops (for, foreach, while, break, continue)

### for

- python

```python
for v in range(0, 3):
    print(v)
[output]
0
1
2

i = 0
while i < 5:
    print(i)
    i += 1

while True:
    message = input("please input")
    if message == 'quit':
        break
    print(message)
```
- go
```go
for i := 0; i < len(os.Args); i++ {
  fmt.Println(os.Args[i])
}
fmt.Println(s)
```

## switch

# object or struct

# pointers

# functions

### scope and external variables


- shell

``` bash
f1(){
local xxx=1
echo $xxx;
echo "all variables in a function are global like in js, set it with local to make them local variables"
echo "local can only be used in a function"
}
```

## pass by value and pass by reference

## dynamic length variable

# array

### array to stream

- java

``` java  
String[] array = {"a", "b", "c", "d", "e"};
Stream<String> stream1 = Arrays.stream(array);
stream1.forEach(x -> System.out.println(x));
```

## array to map

### 

``` java

```
# list 

### initialization

- python
```python
fruit = ['apple', 'banana', 3 , 5 ]
print(fruit) # ['apple', 'banana', 3, 5]
numbers = list(range(0,3))
print(numbers)
[output]
0
1
2
squares = [v**2 for v in range(0,2)]
print(squares)
```
### access via index

- python
```python
fruit = ['apple', 'banana', 3 , 5 ]
print(fruit[0])  # apple
print(fruit[-1]) # 5
```
- python tuple
``` python
fruit = ('apple', 'banana', 3 , 5 ) # ('apple', 'banana', 3, 5)
print(fruit[0])  # apple
print(fruit[-1]) # 5

```
### add, upate the list

- python
```python
fruit = ['apple', 'banana', 3 , 5 ]
fruit[0] = 'orange'
fruit.insert(0, 'all fruit: ')
fruit.append('all good')

```
- python tuple

python tuple is not allowed to be updated, only assignment allowed
``` python
fruit = ('apple', 'banana', 3 , 5 )
fruit = ('orange')

```
### delete from the list

- python

```python
fruit = ['apple', 'banana', 3 , 5 ]
del(fruit[0])
del(fruit[-1])
print(fruit)          # ['banana', 3]
poped = fruit.pop()   # delete the last one then return it
poped = fruit.pop(1)  # delete the 2rd one then return it
fruit.remove(3)       # delete according to specific value, this will only delete the first occurance value

fruit = ['apple', 'banana', 'banana' ]
while f in fruit:
    fruit.remove(f)

```
- python tuple

python tuple is not allowed to be deleted

### traverse the list

- python
```python
fruit = ['apple', 'banana', 3 , 5 ]
for f in fruit:
    print(f)

while fruit:
    poped = fruit.pop()
    print(poped)

```
- python tuple

``` python
fruit = ('apple', 'banana', 3 , 5 )
for f in fruit:
    print(f)

```
### slice the list

- python

```python

fruit = ['apple', 'banana', 3 , 5 ]
print(fruit[0:2]) # ['apple', 'banana']
print(fruit[2:]) # [3, 5]
print(fruit[:2]) # ['apple', 'banana']

```
- python tuple

``` python
fruit = ('apple', 'banana', 3 , 5 )
print(fruit[0:2]) # ('apple', 'banana')
print(fruit[2:]) # (3, 5)
print(fruit[:2]) # ('apple', 'banana')

```
### sort the list

- python
``` python
fruit = ['apple', 'banana', 3 ]
fruit.sort()           # TypeError: '<' not supported between instances of 'int' and 'str'
fruit = ['apple', 'banana']
fruit.sort(reverse=True) # [ 'banana', 'appale' ]

temp_sort = sorted(fruit) # sort temperarily, will not change fruit
```

- python tuple
``` python
fruit = ['apple', 'banana'] 
fruit.sort(reverse=True) # 'tuple' object has no attribute 'sort'
temp_sort = sorted(fruit) # sort temperarily, and return a list instead of a new tuple: ['apple', 'banana']
```

### copy the list

- python

```python
fruit = ['apple', 'banana', 3 , 5 ]
new_fruit = fruit[:]
fruit.pop()
print(fruit)     # ['apple', 'banana', 3]
print(new_fruit) # ['apple', 'banana', 3, 5]


```

- python tuple

```python
fruit = ('apple', 'banana', 3 , 5 )
new_fruit = fruit[:]

```

### reverse the list

- python
```python
fruit = ['apple', 'banana', 3 , 5 ]
fruit.reverse()
print(fruit) # [5, 3, 'banana', 'apple']
```
### list to map 

- java

``` java
Map<String, Item> map = list.stream().filter(
                vo -> !vo.getEnvType().equals("commercial"))
                .collect(
                        Collectors.toMap(vo -> String.join("@", vo.name(), vo.region()),
                                vo -> vo));
```
### numeric list operations

- python
```python
digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
min(digits)
max(digits)
sum(digits)
```
# map

### initialization
- python

```python
d = {}
d = { "name": "name", "age" : 1}
print(d['name'])
```

### add, update map
- python

```python
d = { "name": "name", "age" : 1}
d['sex'] = 'M' # add 
d['name'] = 'my_name' # update
print(d)
```

### delete from map
- python

```python
d = { "name": "name", "age" : 1}
d['sex'] = 'M' # add 
del d['sex']
print(d)
```

### traverse the map
- python

```python
d = { "name": "name", "age" : 1}
for k, v in d.items():
    print(k + ": " + str(v))

for k in d.keys():
    print(k)

for v in d.values():
    print(v)
```

# enum

- java
``` java
// declare enum
public enum Day {
    MONDAY,TUESDAY,WEDNESDAY,THURSDAY,FRIDAY,SATURDAY,SUNDAY
}

// print enum
System.out.println(Day.MONDAY);//MONDAY
System.out.println(Day.TUESDAY);//TUESDAY
System.out.println(Day.WEDNESDAY);//WEDNESDAY
System.out.println(Day.TUESDAY);//TUESDAY
System.out.println(Day.FRIDAY);//FRIDAY
System.out.println(Day.SATURDAY);//SATURDAY
System.out.println(Day.SUNDAY);//SUNDAY

// get enum by string

Day day = Day.valueOf("FRIDAY");
System.out.println(day);//FRIDAY
day = Day.valueOf("WRONG");
System.out.println(day);//Exception in thread "main" java.lang.IllegalArgumentException: No enum constant com.company.Day.WRONG

// loop over enum
for (Day day : Day.values()){
    System.out.println(day);
}

// switch by enum
Day day = Day.FRIDAY;
switch (day){
    case MONDAY:
        System.out.println(0);
        break;
    case TUESDAY:
        System.out.println(1);
        break;
    case WEDNESDAY:
        System.out.println(2);
        break;
    case THURSDAY:
        System.out.println(3);
        break;
    case FRIDAY:
        System.out.println(4);
        break;
    case SATURDAY:
        System.out.println(5);
        break;
    case SUNDAY:
        System.out.println(6);
        break;
}

// compare enum
Day day = Day.FRIDAY;
System.out.println(day==Day.FRIDAY);
```

# string

### string initialization

- python
``` python
message = " hello, worlD "
message = ' hello, worlD '
print(message)
```

### length 

- python 
```python

message = ' hello, worlD '
len(message)
```
### to lower case and upper case

- python
``` python
message = " hello, worlD "
print(message.upper())   # to upper case 
print(message.lower())   # to lower case
```
### trim

- python
```python
message = " hello, worlD "
print(message.rstrip())  # remove the specified characters from right hand side of a string (By default, White spaces)
 hello, worlD
print(message.lstrip())  # remove the specified characters from left hand side of a string (By default, White spaces) 
hello, worlD 
print(message.strip())   # remove the specified characters from both left and right hand side of a string (By default, White spaces)
hello, worlD
```
### start with and end with
### contains and index of
### concat and split

- python
``` python
 print("hello," + " world") # concat 2 strings
```
### compare
### title

- python

```python
# python
message = "hello, worlD"
print(message.title())   # convert the first character in each word to uppercase, and all other chracters to lowwercase
Hello, World 
```
# type conversion

python
``` python
age = 3
print("I am " + str(age))
age = '3'
age = int(age)
```
# date and time

# json

java gson

``` xml
/* To use Gson, add following to pom.xml  */
<dependency>
    	<groupId>com.google.code.gson</groupId>
    	<artifactId>gson</artifactId>
    	<version>2.6.2</version>
</dependency>
```

``` java
// Convert java object to json string
User user = new User();
String userInString = new Gson().toJson(user);

// Convert json string to java object
User user = new Gson().from(userInString,User.class);

// Convert json array to java List
String jsonInstring = "[{\"tenant\":\"Google\"}, {\"tenant\":\"Facebook\"}]";
List<Customer> list = gson.fromJson(jsonInString, new TypeToken<List<Customer>>(){}.getType());
list.forEach(x -> System.out.println(x));

// Convert json to java Map
String jsonInstring = "{\"tenant\":\"Google\", \"landscape\":"develop"}";
Map<String, Object> map = gson.fromJson(jsonInString, new TypeToken<Map<String, Object>>(){}.getType());
map.forEach((x,y)-> System.out.println( x + "-" + y));
```

# file IO

# network IO

# object oriented programming

## object lifecycle

## object initialization

## memory nodel

## reflect 

## garbage collection

# errors and exceptions

# process 

# thread

# format 

# read from stdin

- python

```python

message = input("Please input your message: ")
print(message)
```

# test

# dependency/package management

## maven for java

``` shell
mvn dependency:tree # check dependency
```

## npm for node.js

```bash
npm search db # locate the modules by keywords db
npm install commander@">1.0.0" # greater than version 1.0.0
npm install commander@1.0.0 # exactly matches version 1.0.0
npm install commander@"=1.0.0" # exactly matches version 1.0.0
npm install commander@"~1.0.0" # greater than or equal to version 1.0.0 , but less than the mexe major version

npm outdated [module-name] [-g] # display outdated packages [in golbal folder]
npm update [module-name] [-g]  # update outdated packages [in golbal folder]

npm adduser
npm publish

npm ls # view all the m-odules installed in current directory
npm ls -g # view all the modules installed in global directory
npm root -g # view the path that the global modules been installed

npm rm module-name # remove a module

# linking packages is very useful if you are developing a module and want another project to reference your local copy of the module . 
# a linked package can be refered as if it were a global package , 
# which is very similar to module installation . 
#1. create global link
cd my-project & npm link # now your 'my-project' is a global module , you can verify using npm ls -g 
#2. reference an existing link 
cd other-project & npm link my-project # link my-project as a module in your other-project 
#3.unlink package 
cd other-project & npm unlink my-project 
cd my-project & npm unlink 

```

