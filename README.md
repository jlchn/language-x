> for shell, please refer to [shell cheatsheet](shell-cheatsheet.md)

# basic types, operators, expressions

# control flow

## if, if else, else if

## loops (for, foreach, while, break, continue)

### for

go
```go
for i := 0; i < len(os.Args); i++ {
  fmt.Println( os.Args[i])
}
fmt.Println(s)
```

## switch

# object or struct

# pointers

# functions

## scope and external variables


shell

``` shell
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

## array to stream

``` java 
//java 
String[] array = {"a", "b", "c", "d", "e"};
Stream<String> stream1 = Arrays.stream(array);
stream1.forEach(x -> System.out.println(x));
```

## array to map

### 

``` java

```

# collections

## list 

### list to map 

java

``` java
Map<String, Item> map = list.stream().filter(
                vo -> !vo.getEnvType().equals("commercial"))
                .collect(
                        Collectors.toMap(vo -> String.join("@", vo.name(), vo.region()),
                                vo -> vo));
```

# map

# enum

java
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

- to lower case or upper case
- trim
- start with and end with
- contains and index of
- length 

python

``` python
message = " hello, worlD "
print(message)
// to upper case
print(message.upper())
// to lower case
print(message.lower())
// convert the first character in each word to uppercase, and all other chracters to lowwercase
print(message.title()) # Hello, World
// remove the specified characters from right hand side of a string (By default, White spaces) 
print(message.rstrip())
// remove the specified characters from left hand side of a string (By default, White spaces) 
print(message.lstrip())
// remove the specified characters from both left and right hand side of a string (By default, White spaces) 
print(message.strip())
```

## initialization 

## length 

## copy

## concat

## compare

## search in strings(contains, index of)

## split

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

