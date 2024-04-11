[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    //Base Case
    if(a.length == 1) 
        return a[0];
    
    //Recursive call if base case fails
    var foo = mystery(a.slice(1, a.length))
    
    //Return the greater value, the selected temporary value or the current value
    if(foo > a[0]) 
        return foo;
    else 
        return a[0];
}
```

This function provides the maximum value in an array through recursive calls

```
-Initially, the recursive call removes one element from the array
-On the last element in the array, it assigns the last value to a temporary variable named 'foo'
-At this point, the recursive calls collapse, and a single element will be added to the front every time
-The value of 'foo' is then compared to the newly added first value, and the greater element is returned
    -If 'foo' was the greater element, then the value of foo remains the same
    -If 'foo' was the lesser element, the value of 'foo' is overwritten
```
