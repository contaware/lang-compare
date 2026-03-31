# Python vs JavaScript vs PHP: Syntax Comparison

This guide provides a side-by-side comparison of three of the most popular programming languages.

## 1. Basics

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Comments** | `#` | `//` `/* .. */` | `//` `#` `/* .. */` |
| **Tags** | none | `<script>code</script>` | `<?php code ?>` <br> and <br>`<?= "echoed" ?>` |
| **Whitespaces & indentation** | Whitespaces meaningful, code blocks are defined by indentation. Common is 4 spaces for indentation. | Whitespaces ignored, blocks defined by `{}`. Common is 2 or 4 spaces for indentation. | Whitespaces ignored, blocks defined by `{}`. Common is 4 spaces for indentation. |
| **Statement separator** | Semicolon, optional at end of line. | Semicolon, optional at end of line. | Semicolon, can only be omitted when preceding `?>` |
| **Case sensitivity** | Fully sensitive | Fully sensitive | **Sensitive**: variables, properties, constants and array indexes.<br>**Insensitive**: functions, methods, classes, namespaces and keywords. |
| **General naming convention** | Preferred is snake_case | Preferred is camelCase | Mixed snake_case and camelCase |
| **Classes naming convention** | PascalCase | PascalCase | PascalCase |
| **Constants naming convention** | SCREAMING_SNAKE_CASE | SCREAMING_SNAKE_CASE | SCREAMING_SNAKE_CASE |
| **Output** | `print("With newline")`<br>`print("No newline", end="")` | `console.log("With newline");` | `echo "Hi", "\n";` |

## 2. Variables, Constants and Data Types

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Primitive datatypes** | **Immutable**<br>`num = 10`<br>`flt = 3.14`<br>`flag = True`<br>`name = "Bob"` | **Immutable**<br>`let num = 10;`<br>`let flt = 3.14;`<br>`let flag = true;`<br>`let name = "Bob";` | **Mutable**<br>`$num = 10;`<br>`$flt = 3.14;`<br>`$flag = true;`<br>`$name = "Bob";` |
| **Constants** | `PI = 3.14` | `const PI = 3.14;` | `const PI = 3.14;`<br>`define('PI', 3.14);` |
| **Cast** | `num = int("10")`<br>`flt = float("1.1")` | `let num = parseInt("10");`<br>`let flt = parseFloat("1.1");`<br> | `$num = (int)"10";`<br>`$flt = (float)"1.1";` |
| **Test type** | `if type(num) is int:`<br>`if type(flt) is float:`<br>`if type(flag) is bool:` | `if (typeof num === "number")`<br>`if (typeof flt === "number")`<br>`if (typeof flag === "boolean")`<br>Note: in JS int and float are both of `number` type. | `if (is_int($num))`<br>`if (is_float($flt))`<br>`if (is_bool($flag))` |
| **Print type** | `print(type(num))` | `console.log(typeof num);` | `var_dump($num);` |
| **Missing** | `None` is intentional absence. | `null` is intentional absence.<br>`undefined` means uninitialized. | `null` is intentional absence. |
| **Test defined** | `if 'val' in locals():` | `if (typeof val !== "undefined")` | `if (isset($val))`<br>Note: tests whether defined and not null. |

## 3. Strings

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Single vs double quotes** | **Identical behavior**: parse escape sequences. | **Identical behavior**: parse escape sequences. | **Single-quotes**: literal.<br>**Double-quotes**: parse vars and escape sequences. |
| **Raw strings** | `r"Literal\n"`<br>`r'Literal\n'` | `` String.raw`Literal\n` `` | `'Literal\n'` |
| **Interpolation** | `f"Hi {name}"`<br>`f'Hi {name}'` | `` `Hi ${name}` `` | `"Hi $name"`<br>`"Hi {$name}"` |
| **Multi-line** | `"""L1`<br>`L2"""`<br>`'''L1`<br>`L2'''` | `` `L1``<br>``L2` `` | `"L1`<br>`L2"`<br>`'L1`<br>`L2'` |
| **Common functions** | `len(s)`<br>`s.upper()`<br>`s.find(sub)`<br>`s.replace(old, new)` | `s.length`<br>`s.toUpperCase()`<br>`s.indexOf(sub)`<br>`s.replace(old, new)` | `strlen($s)`<br>`strtoupper($s)`<br>`strpos($s, $sub)`<br>`str_replace($old, $new, $s)` |

## 4. Operators

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Arithmetic** | `+ - * / % **` | `+ - * / % **` | `+ - * / % **` |
| **Inc/Dec** | `x += 1` `x -= 1` | `++` `--` | `++` `--` |
| **Comparison** | `< <= > >= == !=`<br>`1 < y <= 3`<br>`is` `is not` (identity) | `< <= > >= == !=`<br>`=== !==` (strict) | `< <= > >= == !=`<br>`=== !==` (strict) |
| **Logical** | `and` `or` `not` | `&&` `\|\|` `!` | `&&` `\|\|` `!` |
| **Bitwise** | `~` `\|` `&` `^` | `~` `\|` `&` `^` | `~` `\|` `&` `^` |
| **Shift** | `<<` `>>` | `<<` `>>` | `<<` `>>` |
| **String concat** | `+` `+=` | `+` `+=` | `.` `.=` |

## 5. Collections

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Basic Types** | List `[]`, Dict `{}`, Tuple `()`, Set | Array `[]`, Object `{}`, Map, Set | Indexed & Assoc. Array `[]` |
| **Check Item** | `x in my_list` | `myArr.includes(x)` | `in_array($x, $arr)` |

## 6. Control Flow and Loops

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **If / Else** | `if / elif / else` | `if / else if / else` | `if / elseif / else` |
| **Looping** | `for item in items:` | `for (let item of items) {}` | `foreach ($items as $item) {}` |

## 7. Functions

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Declaration** | `def func(a, b):` | `function func(a, b) {}` | `function func($a, $b) {}` |
| **Arrow/Lambda** | `lambda a, b: a + b` | `(a, b) => a + b` | `fn($a, $b) => $a + $b` |

## 8. Classes and OOP

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Constructor** | `def __init__(self, n):` | `constructor(n) {}` | `public function __construct($n)` |
| **This/Self** | `self` | `this` | `$this` |

## 9. Package Managers

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **CLI Tool** | `pip` | `npm` | `composer` |
| **Config File** | `requirements.txt` | `package.json` | `composer.json` |
