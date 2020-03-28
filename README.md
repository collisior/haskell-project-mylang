# Project for Functional Programming Languages Course.
Project: New language written in Haskell. 

This language has its own compilation logic, language structure, and associaticity rules. 

Project repo be found in [this link](https://github.com/BU-CS320/project-supercalifragilisticexpialidocious/tree/master/project)

## Project Language Description
The precedence, associativity, and default meaning as in Haskell. But there is one important exception: the precedence for application should follow the rule where application is lower in precedence rather than a very high precedence (as in Haskell). The operators are listed below in classes (operators of the same precedence) in increasing order of precedence, with associativity and other characteristics noted. 


## Additional Features of the Language:

	Supports scientific notation for Double type
	Lambdas support multiple arguments. So you may write \x y z -> x instead of \x -> \ y -> \ z -> x
	Can run a file in cabal repl with execFile <filename>
	Strings and Chars support escaped characters
	Doesn't need a statemnt on both sides of a separator. "2+2;" will parse and run fine
	Can parse strings as ints or doubles like (double x) where x can be a string like "123.456"	


#### Precedence Classes
in increasing order, L associative except as noted, for arithmetic,relational,
    and boolean operators both operands must be same type
<pre>  
    ;     Separator                  -- lowest precedence, R associative
  <hr> 
          Application                -- function application (no operators, just a blank between expressions)
  <hr> 
    ||    Boolean Or                  
   <hr>    
    &&    Boolean And 
    <hr>   
                                     -- relational operators are non-associative (can only be one operator 
                                     -- in an expression) 
    ==    Equals                     -- equality operators are overloaded for all types except functions                  
    /=    Not-equal                                                     
    <     Less-than                  -- these four operators only need to compare integers and floats,  
    <=    Less-than-or-equal                              
    >=    Greater-than-or-equal              
    >     Greater-than 
      <hr> 	
    :     List cons                  -- R associative
    ++    List concatenation         -- R associative
    <hr>    
    +     Addition                   -- these 2 operators overloaded for integers and floats
    -     Subtraction                -- this is overloaded to also be a unary minus function (see below)
   <hr>    
    *     Multiplication             -- overloaded for integers and floats                          
    /     Floating-Point Division     
    //    Integer Division   
    %     Modulus (remainder after integer division)    -- only for integers
    <hr>   
    ^     Floating-Point Exponentiation             -- R associative
    **    Integer Exponential                       -- R associative
  <hr> 
    !!    List indexing operator     -- L associative, left operand must be list, right must be integer
  <hr> 
    -- prefix operators and functions
    not    Boolean not
    -      Unary minus
    print  Print expression
  <hr> 
    -- atomic expressions
    The highest precedence is the atoms, e.g., integers, floats, chars, lists represented by syntax [,,,], variables, let, if-then-else,lambda abstractions. 
</pre>  
