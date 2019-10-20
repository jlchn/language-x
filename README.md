# basic types, operators, expressions

# control flow

## if, if else, else if

## loops (for, foreach, while, break, continue)

### for

```go
// go
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

``` java
// java
Map<String, Item> map = list.stream().filter(
                vo -> !vo.getEnvType().equals("commercial"))
                .collect(
                        Collectors.toMap(vo -> String.join("@", vo.name(), vo.region()),
                                vo -> vo));
```

# map

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
