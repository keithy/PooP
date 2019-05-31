# PHP-Infinity

## Specification of ideas to improve to PHP

1. Classes as first class objects

$person = $_CLASSES['Models\\Persons']->new();
$person = $_NAMESPACE['Models']['Persons']->new();

2. Scalar Object methods 

 (tidy/remove std library functions)
``` 
 "Testing"->length();
$person->class();
```
3. Function call as a sentence
```
function between($a)and($b) 
{
return $this > $a && $this < $b;
}
```
## Tricky - requiring Language pre-parser  

4. Evaluate Callables and Scalars
```
class Person { function hello() { return "Hello World"; } }

assert( true == ($this->hello->__value() == "Hello World"->__value());
```
5. Naming Convention for DCI-Roles

"role" => "trait"

6. If variable isset do - operator
```
if (!isset($name)) $name = "Dolittle";  // $name ?? $name = "Dolittle";
if (isset($data)) $name = "Dr. $name";  // $name ? $name = "Dr. $name"
i.e. $a ? <exp>  is equivalent to $a ? <exp> : null;
```

## More Difficult requiring Language Updates

7. Exceptions to be Notifications

When Exceptions can return to the thrown context returning data from an outside context.
```
try {
  $whoseThere = throw new Shout()
}
catch( Shout $ex )
{
return "Mummy";
}
```
8. Assert to raise Notification (see above)

Allows assertions to be counted in the catching context, marked as passed as well as failed.
Allows functions other than `assert()` to raise AssertionNotification and AssertionException and carry on execution.

9. Dynamic loading and unloading of traits for DCI

## Miscellaneous

10. PDO to accept array as alternative to dsn

Improve the consistency of PDO instanciation as per http://keithy/primo-pdo-php

11. If variable isset do - operator
```
if (!isset($name)) $name = "Dolittle";  // $name ?? $name = "Dolittle";
if (isset($data)) $name = "Dr. $name";  // $name ? $name = "Dr. $name"
i.e. $a ? <exp>  is equivalent to $a ? <exp> : null;
```





