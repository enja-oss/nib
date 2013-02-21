## Position mixins

The position mixins `absolute`, `fixed`, and `relative` provide a shorthand variant to what is otherwise three CSS properties. The syntax is as follows:

````
fixed|absolute|relative: top|bottom [n] left|right [n]
````

The following example will default to (0,0):

````      
#back-to-top {
  fixed: bottom right;
}
````

yielding:

````
#back-to-top {
  position: fixed;
  bottom: 0;
  right: 0;
}
````

You may also specify the units:

````
#back-to-top {
  fixed: bottom 10px right 5px;
}
````

yielding:
      
````
#back-to-top {
  position: fixed;
  bottom: 10px;
  right: 5px;
}
````    
