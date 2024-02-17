![[Pasted image 20240217132859.png]]

- Functional Programming ideas that have been around for over 40 years will be rediscovered to solve our current software complexity problems.
- The state of hardware, e.g. gigabytes of cheap memory and fast processors, will make functional techniques viable.
- CPUs will not get faster but the number of cores will continue to increase.
- Mutable state will be recognized as one of the biggest problems in complex systems.

## Purity

- Pure functions have no side effects
- They will always produce the same output given the same inputs
- Pure functions cannot change any external variables]

>[!INFO]
>Functional Languages cannot eliminate Side Effects, they can only confine them. Since programs have to interface to the real world, some parts of every program must be impure. The goal is to minimize the amount of impure code and segregate it from the rest of our program.

## Immutability

```
var x = 1;
x = x + 1;
```

And whoever was teaching you told you to forget what you learned in math class? In math, x can never be equal to x + 1.

But in Imperative Programming, it means, take the current value of x add 1 to it and put that result back into x.

Well, in functional programming, x = x + 1 is illegal. So you have to remember what you forgot in math… Sort of.

>[!INFO]
>There are no variables in Functional Programming.
>Stored values are still called variables but they are constants.

<mark style="background: #FF5582A6;"><b>HOW THE HELL AM I SUPPOSED TO DO ANYTHING WITHOUT VARIABLES?</b></mark>

>[!INFO]
>Functional Programming deals with changes to values in a record by making a copy of the record with the values changed. It does this efficiently without having to copy all parts of the record by using data structures that makes this possible.
>
>And solves the single-valued change in exactly the same way, by making a copy of it.

Also there are no loops... <mark style="background: #FF5582A6;"><b>WHAT NO VARIABLES AND NO LOOPS?!</b></mark>

>[!INFO]
>Functional Programming uses recursion to do looping.

```elm
sumRange start end acc =  
	if start > end then  
		acc  
	else  
		sumRange (start + 1) end (acc + start)
```

One obvious benefit is that if you have access to a value in your program, you only have read access, which means that no one else can change that value. Even you. So no accidental mutations.

Also, if your program is multi-threaded, then no other thread can pull the rug out from under you. That value is constant and if another thread wants to change it, it’ll have create a new value from the old one.

## High Order Functions

>[!INFO]
>In Functional Programming, a function is a first-class citizen of the language. In other words, a function is just another value. Since functions are just values, we can pass them as parameters.

```javascript
function validateValueWithFunc(value, parseFunc, type) {  
	if (parseFunc(value))  
		console.log('Invalid ' + type);  
	else  
		console.log('Valid ' + type);  
}

function makeRegexParser(regex) {  
    return regex.exec;  
}

var parseSsn = makeRegexParser(/^\d{3}-\d{2}-\d{4}$/);  
var parsePhone = makeRegexParser(/^\(\d{3}\)\d{3}-\d{4}$/);

validateValueWithFunc('123-45-6789', parseSsn, 'SSN');  
validateValueWithFunc('(123)456-7890', parsePhone, 'Phone');  
validateValueWithFunc('123 Main St.', parseAddress, 'Address');  
validateValueWithFunc('Joe Mama', parseName, 'Name');
```

>[!INFO]
>Higher-order Functions either take functions as parameters, return functions or both.

```javascript
function makeAdder(constantValue) {  
	return function adder(value) {  
		return constantValue + value;  
	};  
}

var add10 = makeAdder(10);  
```

## Closures

>[!INFO]
>A closure is a function’s scope that’s kept alive by a reference to that function.

```javascript
function grandParent(g1, g2) {
    var g3 = 3;
    return function parent(p1, p2) {
        var p3 = 33;
        return function child(c1, c2) {
            var c3 = 333;
            return g1 + g2 + g3 + p1 + p2 + p3 + c1 + c2 + c3;
        };
    };
}
```

- The Child has access to its variables, the parent’s variables and the grandParent’s variables.
- The Parent has access to its variables and grandParent’s variables.
- The grandParent only has access to its variables.

```javascript
var parentFunc = grandParent(1, 2); // returns parent()
var childFunc = parentFunc(11, 22); // returns child()
console.log(childFunc(111, 222)); // prints 738
// 1 + 2 + 3 + 11 + 22 + 33 + 111 + 222 + 333 == 738
```

When a function is created, all of the variables in its scope at the time of creation are accessible to it for the lifetime of the function. A function exists as long as there still a reference to it. For example, child’s scope exists as long as childFunc still references it.

>[!WARNING]
>In Javascript, closures are problematic since the variables are mutable, i.e. they can change values from the time they were _closed over_ to the time the returned function is called.

>[!INFO]
>Thankfully, variables in Functional Languages are Immutable eliminating this common source of bugs and confusion.

## Function Composition

>[!DANGER]
>Code reuse sounds great but is difficult to achieve. Make the code too specific and you can’t reuse it. Make it too general and it can be too difficult to use in the first place.

How to solve this?

What we need is a balance between the two, a way to make smaller, reusable pieces that we can use as building blocks to construct more complex functionality.

>In Functional Programming, functions are our building blocks. We write them to do very specific tasks and then we put them together like Lego™ blocks.

```javascript
var add10 = value => value + 10;  
var mult5 = value => value * 5;
var mult5AfterAdd10 = value => mult5(add10(value));
```

In math, f ∘ g is functional composition and is read “f composed with g” or, more commonly, “f after g”. So (f ∘ g)(x) is equivalent to calling f after calling g with x or simply, f(g(x)).

```elm
add10 value =
    value + 10
mult5 value =
    value * 5
mult5AfterAdd10 value =
    (mult5 << add10) value
```

Value is specified twice. But this parameter is unnecessary since add10, the rightmost function in the composition, expects the same parameter. The following point-free version is equivalent and easier to read:

```elm
-- This is also a function that expects 1 parameter
mult5AfterAdd10 =
    (mult5 << add10)
```

The << infixed operator is how you compose functions in Elm. It gives us a visual sense of how the data is flowing. First, value is passed to add10 then its results are passed to mult5.

```elm
f x =  
	(g << h << s << r << t) x
```

## Currying

```elm
add x y =
    x + y
mult5 value =
    value * 5
-- This is wrong !!!
mult5AfterAdd10 =  
    (mult5 << add) 10
```

This wouldn’t work because the add function is only getting 1 of its 2 parameters here then its incorrect results are passed to mult5. This will produce the wrong results.

We can solve this easily by just restricting all functions to take only 1 parameter.

```javascript
var mult5 = x => x * 5
var add = x => y => x + y
var compose = (f, g) => x => f(g(x));
var mult5AfterAdd10 = compose(mult5, add(10));
```

In Elm:

```elm
add x y =  
	x + y

mult5AfterAdd10 =  
	(mult5 << add 10)
```

### Refactoring

Another time currying shines is during refactoring when you create a generalized version of a function with lots of parameters and then use it to create specialized versions with fewer parameters.

```elm
bracket str =
    "{" ++ str ++ "}"
doubleBracket str =
    "{{" ++ str ++ "}}"

bracketedJoe =
    bracket "Joe"
doubleBracketedJoe =
    doubleBracket "Joe"

```

```elm
generalBracket prefix str suffix =  
	prefix ++ str ++ suffix
	
bracketedJoe =  
    generalBracket "{" "Joe" "}"
    
doubleBracketedJoe =  
    generalBracket "{{" "Joe" "}}"

```

```elm
generalBracket prefix suffix str =
    prefix ++ str ++ suffix
bracket =
    generalBracket "{" "}"
doubleBracket =
    generalBracket "{{" "}}"

bracketedJoe =
    bracket "Joe"
doubleBracketedJoe =
    doubleBracket "Joe"
```

## Common Functional Functions

```javascript
var map = (f, array) => {
    var newArray = [];
    for (var i = 0; i < array.length; ++i) {
        newArray[i] = f(array[i]);
    }
    return newArray;
};

var filter = (pred, array) => {
    var newArray = [];
	for (var i = 0; i < array.length; ++i) {
	        if (pred(array[i]))
	            newArray[newArray.length] = array[i];
	    }
	    return newArray;
	};
}

var reduce = (f, start, array) => {
    var acc = start;
    for (var i = 0; i < array.length; ++i)
        acc = f(array[i], acc); 
    return acc;
});
```

```javascript
var things = [1, 2, 3, 4];
var newThings = map(v => v * 10, things);
console.log(newThings); // [10, 20, 30, 40]

var isOdd = x => x % 2 !== 0;
var numbers = [1, 2, 3, 4, 5];
var oddNumbers = filter(isOdd, numbers);
console.log(oddNumbers); // [1, 3, 5]

var add = (x, y) => x + y;
var values = [1, 2, 3, 4, 5];
var sumOfValues = reduce(add, 0, values);
console.log(sumOfValues); // 15
```

## Referential Transparency

>Referential Transparency is a fancy term to describe that a pure function can safely be replaced by its expression

```elm
quote str =
    "'" ++ str ++ "'"

findError key =
    "Unable to find " ++ (quote key)

findError key =
   "Unable to find " ++ ("'" ++ str ++ "'")
```

## Execution Order

Most programs are single-threaded, i.e. one and only one piece of code is being executed at a time. Even if you have a multithreaded program, most of the threads are blocked waiting for I/O to complete, e.g. file, network, etc.

This is one reason why we naturally think in terms of ordered steps when we write code:

1. Get out the bread
2. Put 2 slices into the toaster
3. Select darkness
4. Push down the lever
5. Wait for toast to pop up
6. Remove toast
7. Get out the butter
8. Get a butter knife
9. Butter toast

In this example, there are two independent operations: getting butter and toasting bread. They only become interdependent at step 9. So you can do it like this:

Thread 1
1. Get out the bread
2. Put 2 slices into the toaster
3. Select darkness
4. Push down the lever
5. Wait for toast to pop up
6. Remove toast
Thread 2
1. Get out the butter
2. Get a butter knife
3. Wait for Thread 1 to complete
4. Butter toast

What happens to Thread 2 if Thread 1 fails? What is the mechanism to coordinate both threads? Who owns the toast: Thread 1, Thread 2 or both?

>[!SUCCESS]
>It’s easier to not think about these complexities and leave our program single threaded.
>But when it’s worth squeezing out every possible efficiency of our program, then we must take on the monumental effort to write multithreading software.

>[!DANGER]
>However, there are 2 main problems with multithreading. First, multithreaded programs are difficult to write, read, reason about, test and debug. 
>Second, some languages, e.g. Javascript, don’t support multithreading and those that do, support it badly.

But what if order didn’t matter and everything was executed in parallel?

While this sounds crazy, it’s not as chaotic as it sounds. Let’s look at some Elm code to illustrate this:

```elm
buildMessage message value =
    let
        upperMessage =
            String.toUpper message
        quotedValue =
            "'" ++ value ++ "'"
    in
        upperMessage ++ ": " ++ quotedValue
```

UpperMessage and quotedValue are independent. How do we know this?

There are 2 things that must be true for independence. First, they must be pure functions. This is important because they must not be affected by the execution of the other.

If they were not pure, then we could never know that they’re independent. In that case, we’d have to rely on the order that they were called in the program to determine their execution order. This is how all Imperative Languages work.

The second thing that must be true for independence is that the output of one function is not used as the input of the other. If this was the case, then we’d have to wait for one to finish before starting the second.

In this case, upperMessage and quotedValue are both pure and neither requires the output of the other.

Therefore, these 2 functions can be executed in ANY ORDER.

>[!INFO]
>The order of execution in a Pure Functional Language can be determined by the compiler.

This is extremely advantageous considering that CPUs are not getting faster. Instead, manufactures are adding more and more cores. This means that code can execute in parallel at the hardware level.

Unfortunately, with Imperative Languages, we cannot take full advantage of these cores except at a very coarse level. But to do so requires drastically changing the architecture of our programs.

>[!INFO]
>
>With Pure Functional Languages, we have the potential to take advantage of the CPU cores at a fine grained level automatically without changing a single line of code.

## Type Annotations

```elm
add : Int -> Int -> Int
add x y =
    x + y
```

This says that add is a function that takes a single parameter of type Int and returns a function that takes a single parameter Int and returns an Int.

```elm
doSomething : String -> (Int -> (String -> String))
doSomething prefix value suffix =
    prefix ++ (toString value) ++ suffix
```

This says that doSomething is a function that takes a single parameter of type String and returns a function that takes a single parameter of type Int and returns a function that takes a single parameter of type String and returns a String.

>Notice how everything takes a single parameter. That’s because every function is curried in Elm.

>[!WARNING]
>Parentheses are necessary when we pass functions as parameters. Without them, the type annotation would be ambiguous. 

Look the difference:

```elm
takes2Params : Int -> Int -> String
takes2Params num1 num2 =
    -- do something

takes1Param : (Int -> Int) -> String
takes1Param f =
    -- do something
```

Here’s the type annotation for **_map_**:

```elm
map : (a -> b) -> List a -> List b
map f list =
```

>[!INFO]
>When a type is uppercased, it’s an explicit type, e.g. String. When a type is lowercased, it can be any type. Here a can be String but it could also be Int.

But in the case of map, we have (a -> b). That means that it CAN return a different type but it COULD also return the same type.

But once the type for a is determined, a must be that type for the whole signature. For example, if a is Int and b is String then the signature is equivalent to:

```elm
(Int -> String) -> List Int -> List String
```

