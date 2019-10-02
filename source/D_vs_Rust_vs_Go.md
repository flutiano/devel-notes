
Toolchain
=========

Compile and Run 
---------------

|          | Rust              | Go       | D
|----------|-------------------|----------|---------
| Build    | cargo run <params>| go build | dmd or rdmd
| New      | cargo new ...     | |
| Test     | cargo test        |   

Testing
-------

Module and Package
------------------

Debugging
---------

Syntax and Grammar
==================

General
-------
Comment     | D     | Rust  | Go
--------|---|-------|-------|----
Single line | `//...`   ||
Multi lines | `/*...*/` ||
Nested      | `/+...+/` ||

Basic Types and Operators
-------------------------

Boolean T.  | D | Rust  | Go
------------|---|-------|----
Type    | `bool`    ||
Values  | `true`, `false`   ||


Logical Op. | D | Rust  | Go
------------|---|-------|----
AND         | `&&`  ||
OR          | `||`  ||
XOR         | `^`   ||
NOT         | `!` ||
short-circuit| Yes ||


Comparison  | D     | Rust  | Go
------------|-------|-------|-----
(Not)`EQ`   | `==`, `!=`, `is`, `!is`, `opEquals` ||
Less Than   | `<`, `<=` ||
Greater Than| `>`, `>=` ||
Associative | No        ||


Integral T. | D    | Rust  | Go    
------------|------|-------|------
signed      | `byte, short, int, long`     |
unsigned    | `ubyte, ushort, uint, ulong` |
literal suff.| `u,U,l,L`        |
default lit.| `int` or `long`   |
init value  | `<T>.init`        |
min/max     | `<T>.min/.max`    |


Floating Point T. |  D      | Rust      | Go       
------------------|---------|-----------|-----------
Types       | float, double, real |    
Literal suff.| `f,F,L,p,P`  |
Default Lit.| `double`      |
Width       | `<T>.sizeof`  | 
Init value  | `<T>.nan`     |
Max value   | `<T>.max`     |
Overflow    | `<T>.infinity`  |
Underflow   | `<T>.min_normal`|
NaN check   | `std.math.isNaN(var)` |
Dlang: [Properties for Floating Point Types at dlang.org](https://dlang.org/spec/property.html)
````
   +     +─────────+─────────+   ...   +   ...   +─────────+─────────+     +
   │   -max       -1         │         0         │         1        max    │
   │                         │                   │                         │
-infinity               -min_normal          min_normal               infinity
````

Arithmetic op. | D    | Rust  | Go    
-----------------|------|-------|------
+       | `+`
-       | `-`
*       | `*`   
/       | `/`
Negation| `-`
Plus    | `+`
Modulus | `%`
Power   | `^^`
Increment| `++a, a++`
Decrement| `--a, a--`


Shift op.|  |   |
--------|----------------|-------
D       | `a << b`, `a >> b`, `a >>> b` | `b` >= (width of `a`): either disallowed at compile time or impl.-dependent at runtime if `b` is a runtime value. 

Bitwise Op. | D | Rust | Go
------------|---|------|-----
AND       | `&` | |
OR        | `|` | |
XOR       | `^` | |
Complement| `~a`| |
short-circuit| No | |

Conditional op. | | |
----------------|-----|----
D       | `a ? b : c` | e.g. `(which ? x : y) += 5;` 
Rust    | |
Go      | |


Assignment op. | D  | Rust | Go
---------------|----|-------|----
single   | `a = b`  ||
combined | `a ω= b` ||
associate| RtoL     ||


Comma op.   | | |
--------|-----------|-------
D       | `,`   | yields the result of the rightmost expr.
Rust    |       |
Go      |       |


`in` op. |          | Result    |       |
---------|----------|-----------|--------
D        | `key in map`<br> `!(key in map)` <br> `key !in map`| key: K, map: V[K] -> `V*` or `null` | Result is _NOT_ `bool` type)
Rust     | 
Go       |


Type Cast|  |   |
--------|----------------|----
D       | `cast(Type) a` |
Rust    | 
Go      |
C++     |

Operator precedence | |
--------|------------------
D       | [operator precedence](https://wiki.dlang.org/Operator_precedence) 
Rust    |
Go      |


Assertion|  |   |
--------|----------------|-------
D       | `assert(expr)` | idiom: `(expr)||assert(false)`
Rust    | 
Go      |
C++     |


Character and String
--------------------

Character T.    |   |   |
----------------|---------------|----------------
D       | `char`(UTF-8), `wchar`(UTF-16), `dchar`(UTF-32) |
Rust    ||
Go      ||
C++     ||

Char. literal |     D       |    Rust   | Go
--------------|-------------|-----------|---------
quote         | `'<char>'`       |
char. name    | `'\&euro;'`      |
unicode value | `'\u0000011e'`   |
byte value    | `'\ooo','\xhh'`  |
escaped char  | `'\r','\n', ...` |

[D named characters](https://dlang.org/spec/entity.html#NamedCharacterEntity)

String T.   |   D   | Rust  |   Go  
------------|-------------|---------------|-------------
Type alias  | `string, wstring, dstring`             | 
Type        | _immutable_ `char[], wchar[], dchar[]` |


String literal  |   D       |   Rust    | Go
----------------|-----------|-----------|-----------
quote           | `"<str>"` |
Literal suffix  | `"..."c, "..."w, "..."d` |

String op.     |  D            |  Rust     |  Go 
---------------|---------------|-----------|--------------
concatenation  | `~, ~=`       | 
comparison     |  `==, <, >`   |

>  Note: 
> In Dlang, `std.string` [module](http://dlang.org/phobos/std_string.html) can be used when processing strings. Because strings are arrays (and as a corollary, ranges), the functions of the `std.array, std.algorithm, and std.range` modules are very useful with strings as well.

Statements
--------------------

Expression st. | | |
---------------------|-------------|------------
D        | `<expr>;` | but compile error if the resulting statement has no effect
Rust     |
Go       |

Compound st. | | |
-------------------|---------------------|-------------------
D     | `{ <statements> }` | A symbol defined in a scope masks a global symbol but illegal to mask a symbol in the same scope
Rust  | 
Go    |


`if`     | | |
---------|-------|----------
D        | `if (<expr>) <st1> else if (<expr>) <st2> else <st2>`
Rust     |
Go       |

conditional compilation | | |
------------------|--------------|------------
D     | `static if (e) <s1> else <s2>` | `<e>` should be evaluatable during compile time.
Rust  |
Go    |
C/C++ | `#if `

### `switch` statement
**D**

````D
switch (<expression>) {
   case <expr1>, ..., <exprN> : 
      ScopeStatementList
      break;
   case FirstExp : .. case LastExp : 
      ScopeStatementList
      break;
   default : 
      ScopeStatementList
      break;
}
````
`<expression>` is evaluated only once. The expression in each case label is any legal expression comparable for equality with `<expression>`, and also for inequality if the `..` syntax is used.

_Fall-through_ execution of `case <expr>` branches; `goto case;` transfers to the next CaseStatement (explicit fall-through)

`case <expr>` overlap is compile-time error

For enforcing `case` labels to cover all `enum` values, `final switch` statement can be used:

```D
final switch ( Expression ) 
   case value1:
      ...
   case value2:
      ...
   ...
   case valueN:
      ...
```
`final switch` does not allow ranged case labels and `default` label.

**Rust**

**Go**

`while` | | |
--------|------------|-------------
D       | `while (expr) <statement>` |
Rust    |
Go      | 

`do-while` | |
-----------|------------------|-------------------
D        | `do <statement> while (expr);` | semicolon at the end of the construct
Rust     |
Go       |

`for`    | | |
---------|-------------|-----------------
D        | `for (initiaze test; increment) <statement>` | if `test` is missing, it is considered to be `true`


`foreach` | |
----------|-------------
D         | `foreach (x; e1 .. e2) <s>` or `foreach ([k, [ref]] x; e) <s>`


`continue` ||
-----------|--------------
D        | `continue <label>;`   |
Rust     |
Go       |

`break`  ||
---------|----------------
D        | `break <label>;`   
Rust     |
Go       |

`goto`   ||
---------|------------------
D        | `goto <label>; goto case <expr>/default;`
Rust     |
Go       |

`return` ||
---------|--------------
D        | `return <expr>;`   
Rust     |
Go       |


`with` | | |
-------|---------------|--------------
D      | `with(e) <s>` | all symbols used in `s` are first looked up as members of `e`


`mixin` | | |
--------|--------------|----------
D       | `mixin(<str>;`) | `mixin(import(<file>));`


`scope` | D only  |
------------|---------------
`scope(exit|success|failure) <statments>;`


`synchronized` | |
---------------|---------------------
D          | `synchronized (<e1>, <e2>...) <statement>`


`try/catch/finally` | |
--------------------|------------------
D     | `try <st1> catch(T1 e1) <s1> ... catch(Tn en) <sn> finally <sf>` 
Rust  |
Go    |


`throw` | | |
--------|-------------|--------------
D       | `throw <e>` | control is transferred to the closest matching `catch`. 
Rust    |
Go      |


`asm` st. | | |
----------|-------------|----
D         | `asm <asm-st>` | Inline Assembler, system agnostic. 


Standard Libraries
============================

Standard Input/Output Stream
----------------------------
|               | D         | Rust | Go  
|---------------|-----------|------|-----
output          | `write`   || 
output w. \n    | `writeln` ||
formatted output| `writefln`||
formatted input | `readf`   ||
read until \n   | `readln`  ||


Frameworks
==========

References, Learning Tools
==========================


Products and Projects
=====================
