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
| **Output** | `print("With newline")`<br>`print("No newline", end="")` | `console.log("With newline")` | `echo "Hi", "\n"` |

## 2. Variables, Constants and Data Types

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Primitive datatypes** | **Immutable**<br>`num = 10`<br>`flt = 3.14`<br>`flag = True`<br>`name = "Bob"` | **Immutable**<br>`let num = 10`<br>`let flt = 3.14`<br>`let flag = true`<br>`let name = "Bob"` | **Mutable**<br>`$num = 10`<br>`$flt = 3.14`<br>`$flag = true`<br>`$name = "Bob"` |
| **Constants** | `PI = 3.14` | `const PI = 3.14` | `const PI = 3.14`<br>`define('PI', 3.14)` |
| **Cast** | `num = int("10")`<br>`flt = float("1.1")` | `let num = parseInt("10")`<br>`let flt = parseFloat("1.1")`<br> | `$num = (int)"10"`<br>`$flt = (float)"1.1"` |
| **Test type** | `if type(num) is int:`<br>`if type(flt) is float:`<br>`if type(flag) is bool:` | `if (typeof num === "number")`<br>`if (typeof flt === "number")`<br>`if (typeof flag === "boolean")`<br>Note: in JS int and float are both of `number` type. | `if (is_int($num))`<br>`if (is_float($flt))`<br>`if (is_bool($flag))` |
| **Print type** | `print(type(num))` | `console.log(typeof num)` | `var_dump($num)` |
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
| **Indexed array** | `list = [0, 1]`<br>`tuple = (0, 1)` | `let arr = [0, 1]` | `$arr = [0, 1]` |
| **Associative array<br>(unique keys)** | `dict = {'k1': 'v1', 'k2': 2}` | `let map = new Map([['k1', 'v1'], ['k2', 2]])`<br>`let obj = {'k1': 'v1', 'k2': 2}` | `$arr = ['k1' => 'v2', 'k2' => 2]` |
| **Set<br>(unique values)** | `s = {'v1', 2}` | `let s = new Set(['v1', 2])` | - |
| **Size** | `len(collection)` | `arr.length`<br>`map.size` | `count($arr)` |
| **Read** | `list[index]`<br>`tuple[index]`<br>`dict['k1']` | `arr[index]`<br>`map.get('k1')`<br>`obj['k1']` | `$arr[index]`<br>`$arr['k1']` |
| **Add** | `list.append(2)`<br>`dict['k3'] = 3` | `arr.push(2)`<br>`map.set('k3', 3)`<br>`obj['k3'] = 3` | `$arr[] = 2`<br>`$arr['k3'] = 3` |
| **Del** | `list.pop(index)`<br>`dict.pop('k3')` | `arr.pop()`<br>`map.delete('k3')`<br>`delete obj['k3']` | `array_pop($arr)`<br>`unset($arr['k1'])` |
| **Check item** | `'k1' in collection` | `arr.includes(1)`<br>`map.has('k1')` | `in_array('v2', $arr)`<br>`array_key_exists('k1', $arr)`|

- **Python tuples**: they are immutable lists.
- **PHP arrays**: there is only one type, indexed arrays are associative arrays with integer keys. Arrays in PHP are assigned and passed **by value**.
- **Javascript obj vs map**: objects only support strings as key, while maps support any value. Maps have a handy `size` property, but have to be accessed with the `get()` method. Objects are better for JSON serialization, while maps support more iteration methods. 
- **Sets**: in Python the insertion order is **not** preserved, while in javascript it is preserved.

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
