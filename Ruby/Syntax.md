# Syntax
Syntax used in ruby.
 
## Variables
When starting with:
  - `$`: global vars
  - `@`: member properties
  - `@@`: static properties (in class)
  - Cap: contants
  
## Operators
 
 `defined?` operator.
 `::` Variable scope
 
## Control sequence:
 - `if`<->`unless` : can be used as
 - `then` is used when `if` sentense finished in one line.
 - `else`, `elsif`
 - `case`, `when [then]`
 - `while [do]`, `until [do]`
 - `for var in expr [do]`
 - `expr.each do |var|`
 - `break`, `next`, `redo`
 
## Exceptions?
```ruby
begin
  do_something
rescue
  handle_exceptions
  retry
else
  ...
ensure
  ...
end
```
 
## Script control sequence:
```ruby
BEGIN {
  codes here
 }

END {
  codes here
 }
```
