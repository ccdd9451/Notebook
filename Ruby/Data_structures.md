# Data structures

 
## String 

### Creating:

``` ruby
ruby: 'string' approx= python: r'string'

ruby: "string" approx= python: "string"

ruby: <<Ends
  strings
Ends
~
python: """
  strings
"""
```

### formating: 

`#{expr}` in string.

## Class 

Class is defined starting with `class`, ending with `end`.
```ruby
class Class
end
```
Objects are created by `new` method. `initialize` is invoked 
during creating a object. Statics properities defined with prefix
`@@`. Member properties created with prefix `@`
