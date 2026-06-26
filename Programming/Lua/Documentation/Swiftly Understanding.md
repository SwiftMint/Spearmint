# [Lua 5.1 Reference Manual](https://www.lua.org/manual/5.1/manual.html)
## 2.1 -- Lexical Conventions
**`Names`** (or **`Identifiers`**) can be any `alphanumeric string` *and/or* `_` combination, as long as a *digit* is not the first character. Conventionally, these also do not begin with a `_`, reserved for internal global variables used by Lua.

### Lua `Keywords`
**Keywords** are reserved by Lua and therefore cannot be used as **Identifiers**.
As Lua is ***case-sensitive***. While **`and`** is a **keyword**,  **`And`** &  **`AND`** are not.

||||
|:-:|:-|:-|
|**`and`**|
|**`break`**|
|**`do`**|
|**`else`**|
|**`elseif`**|
|**`end`**|
|**`false`**|
|**`for`**|
|**`function`**|
|**`if`**|
|**`in`**|
|**`local`**|
|**`nil`**|
|**`not`**|
|**`or`**|
|**`repeat`**|
|**`return`**|
|**`then`**|
|**`true`**|
|**`until`**|
|**`while`**|

`Variables`: local, function, nil
`Logical Operators`: and, or, not
https://www.tutorialspoint.com/lua/lua_operators.htm
https://www.tutorialspoint.com/compilers/online-lua-compiler.htm
in, false, true
`For Statement`: for
`Control Structures`: if, while, repeat, return, break, do, end, until, then, elseif, else

### Lua `Tokens`
**Tokens** are denoted by `symbols` to refine the exact intent of the code.
|||||||||||||||||||||||||||
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:
|**`+`**|**`-`**|**`*`**|**`/`**|**`%`**|**`^`**|
|**`#`**|
|**`==`**|**`~=`**|**`<=`**|**`>=`**|**`<`**|**`>`**|
|**`=`**|
|**`(`**|**`)`**||**`{`**|**`}`**|||**`[`**|**`]`**|
|**`;`**|
|**`:`**|
|**`,`**|
|**`.`**|
|**`..`**|
|**`...`**|

`Arithmetic Operators`: +, - [or unary], *, / ,  %, ^
`Relational Operators`: ==, ~=, <, >, <=, >=
`vararg`: ...
`Length Operator`: #
`Concatenation`: ..
`Table Constructors`: ;, ,, (, ), {, }, [, ]
 =, :, .


### `Escape Sequence` (`\`)
|||||||||||||
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|**`\a`**|
|**`\b`**|
|**`\f`**|
|**`\n`**|
|**`\r`**|
|**`\t`**|
|**`\v`**|
|**`\0`**|
|**`\\`** |
|**`\"`**|
|**`\'`**|
|**`+`**|


### Lua `Strings`
Literal strings are defined using *long brackets*, where *n* = level of literals, which may stack.
*Escape sequences* do not function here and will ignore long brackets of other levels.
A level of 4 would have an opening bracket of `[====` and eventually a closing bracket of `====]`.

*Short comment*s are defined with `--` at the start of a line, marking the entire line as a comment.
*Long comment*s are defined as a *short comment* with two bracket pairs, with an open ( `--[[`) and close (`--]]`). These may be within or across lines.

Each value carries their own type, which can be stored as variables, passed as arguments to other functions, and returned as results.

### Lua `Types`
|||
|-:|:-|
|**`nil`**|a difference from any other value, typically the absence of.|
|**`boolean`**|`false`/`nil` or `true`.|
|**`number`**|A real number.|
|**`string`**|An array of 8-bit characters, including embedded zeros.
|**`function`**|
|**`userdata`**|Calls on arbitrary C data to be stored in Lua variables, only modifiable in `C`|
|**`thread`**|Calls on individual threads, not operating-system threads.|
|**`table`**|An array of numbers or values, except *nil*.|

<br>

`Threads` and `Tables` are *objects*, meaning variables do not actually contain said values.

*Variables* store values and can be defined as *Global*, *Local*, or *Table Fields*.
A single name can denote a *global variable* or a *local variable*.
  ```
  var ::= Name
  ```
Any *variable* is assumed to be *global* unless explicitly declared as a *local*.
If a value is not assigned to a variable, it automatically becomes *nil*.
Brackets are used to index a table.
 ```
 var ::= prefixexp '[' exp ']'
 ```
*Global variables* live as *fields* (or *environments*).

Each unit of execution is called a *chunk*.
  ```
  chunk ::= {stat [';']}`
  ```
';;' is not legal as there may be no empty statements.
A *block* is a list of statements, syntactically the same as a *chunk*.
It can produce a single statement as well with explicit delimiters.
  ```
  stat ::= do block end
  ```

Multiple assignments can be attributed, therefore variables are defined on the left side and expressions are defined on the right.
```
stat ::= varlist '=' explist

varlist ::= var {',' var}

explist ::= exp {',' ex[]}
```

2.4.4 - Control Structures

<br>
<br>
<br>

https://www.tutorialspoint.com/developers_best_practices/index.htm