# Anomous functions

## Proc.New
A multi line lambda object
```ruby
a = Proc.New { some_codes }
```
This object will only be executed by `a.call`!

### Difference between `lambda`, `proc` 
![Stackoverflow discuss here.](
https://stackoverflow.com/questions/1740046/whats-the-difference-between-a-proc-and-a-lambda-in-ruby)
 - `lambda`: strictly check the number of parameters passed when called.
 - `proc` : autofills nil
 - `lambda`: `return` to enclosure function
 - `proc`: `return` jumps out enclosure function


## Block
Is used when a function yielding. Closed between `{}`.
Can be used by `Array.each` (Array doesn't change) or `Array.map`
(Array changes). Notice here: In ruby, Arrays are mutable!
Another way to say it is by 
```Ruby
do 
codes 
end
```

## Yielding
`Yeild`s in a function calls block when it's executed. 



