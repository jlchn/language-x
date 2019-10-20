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

## pass by value and pass by reference

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

## declare enum

java
``` java 
public enum Day {
    MONDAY,TUESDAY,WEDNESDAY,THURSDAY,FRIDAY,SATURDAY,SUNDAY
}
```

## print enum

java

``` java
System.out.println(Day.MONDAY);//MONDAY
System.out.println(Day.TUESDAY);//TUESDAY
System.out.println(Day.WEDNESDAY);//WEDNESDAY
System.out.println(Day.TUESDAY);//TUESDAY
System.out.println(Day.FRIDAY);//FRIDAY
System.out.println(Day.SATURDAY);//SATURDAY
System.out.println(Day.SUNDAY);//SUNDAY
```

## get enum by string

java
``` java
Day day = Day.valueOf("FRIDAY");
System.out.println(day);//FRIDAY
day = Day.valueOf("WRONG");
System.out.println(day);//Exception in thread "main" java.lang.IllegalArgumentException: No enum constant com.company.Day.WRONG
```

## loop the enum

java
``` java
for (Day day : Day.values()){
    System.out.println(day);
}
```

## switch by enum

java
```java

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
```

## compare enum

java
```java
Day day = Day.FRIDAY;
System.out.println(day==Day.FRIDAY);
```

# string

## initialization 

## length 

## copy

## concat

## compare

## search in strings(contains, index of)

## split

# file IO

# network IO

# process 

# thread

# format 

# dependency management
