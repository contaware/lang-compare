# Python vs JavaScript vs PHP <!-- omit from toc -->

This guide provides a side-by-side comparison of popular programming languages.


## Table of contents <!-- omit from toc -->

- [1. Basics](#1-basics)
- [2. Variables, Constants and Data Types](#2-variables-constants-and-data-types)
- [3. Strings](#3-strings)
- [4. Operators](#4-operators)
- [5. Collections](#5-collections)
- [6. Control Flow](#6-control-flow)
- [7. Loops](#7-loops)
- [8. Exceptions](#8-exceptions)
- [9. Functions](#9-functions)
- [10. Classes](#10-classes)
- [11. Package Managers](#11-package-managers)


## 1. Basics

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Comments** | `#` | `//` `/* .. */` | `//` `#` `/* .. */` |
| **Tags** | - | `<script>code</script>` | `<?php code ?>` <br> and <br>`<?= "echoed" ?>` |
| **Whitespaces & indentation** | Whitespaces meaningful, code blocks are defined by indentation. Common is 4 spaces for indentation. | Whitespaces ignored, blocks defined by `{}`. Common is 2 or 4 spaces for indentation. | Whitespaces ignored, blocks defined by `{}`. Common is 4 spaces for indentation. |
| **Statement separator** | Semicolon, optional at end of line. | Semicolon, optional at end of line. | Semicolon, can only be omitted when preceding `?>` |
| **Case sensitivity** | Fully sensitive | Fully sensitive | **Sensitive**: variables, properties, constants and array indexes.<br>**Insensitive**: functions, methods, classes, namespaces and keywords. |
| **General naming convention** | snake_case | camelCase | snake_case<br>camelCase |
| **Classes naming convention** | PascalCase | PascalCase | PascalCase |
| **Constants naming convention** | SCREAMING_SNAKE_CASE | SCREAMING_SNAKE_CASE | SCREAMING_SNAKE_CASE |
| **Output** | `print("With newline")`<br>`print("No newline", end="")` | `console.log("With newline")`<br>`document.write("Hi\n")` | `echo "Hi", "\n"` |


## 2. Variables, Constants and Data Types

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Primitive datatypes** | **Immutable**<br>`num = 10`<br>`flt = 3.14`<br>`flag = True`<br>`name = "Bob"` | **Immutable**<br>`let num = 10`<br>`let flt = 3.14`<br>`let flag = true`<br>`let name = "Bob"` | **Mutable**<br>`$num = 10`<br>`$flt = 3.14`<br>`$flag = true`<br>`$name = "Bob"` |
| **Constants** | `PI = 3.14` | `const PI = 3.14` | `const PI = 3.14`<br>`define('PI', 3.14)` |
| **Cast** | `num = int("10")`<br>`flt = float("1.1")` | `let num = parseInt("10")`<br>`let flt = parseFloat("1.1")`<br> | `$num = (int)"10"`<br>`$flt = (float)"1.1"` |
| **Test type** | `type(num) is int`<br>`type(flt) is float`<br>`type(flag) is bool` | `typeof num === "number"`<br>`typeof flt === "number"`<br>`typeof flag === "boolean"`<br>Note: in JS int and float are both of `number` type. | `is_int($num)`<br>`is_float($flt)`<br>`is_bool($flag)` |
| **Print type** | `print(type(num))` | `console.log(typeof num)` | `var_dump($num)` |
| **Missing** | `None` is intentional absence. | `null` is intentional absence.<br>`undefined` means uninitialized. | `null` is intentional absence. |
| **Test defined** | `"val" in locals()` | `typeof val !== "undefined"` | `isset($val)`<br>(tests whether defined and not null) |


## 3. Strings

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Single vs double quotes** | **Identical behavior:** parse escape sequences. | **Identical behavior:** parse escape sequences. | **Single-quotes:** literal.<br>**Double-quotes:** parse vars and escape sequences. |
| **Raw strings** | `r"Literal\n"`<br>`r'Literal\n'` | `` String.raw`Literal\n` `` | `'Literal\n'` |
| **Interpolation** | `f"Hi {name}"`<br>`f'Hi {name}'` | `` `Hi ${name}` `` | `"Hi $name"`<br>`"Hi {$name}"` |
| **Multi-line** | `"""L1`<br>`L2"""`<br>`'''L1`<br>`L2'''` | `` `L1``<br>``L2` `` | `"L1`<br>`L2"`<br>`'L1`<br>`L2'` |
| **Unicode** | Full support | `String` uses UTF-16 code units. APIs work on code units. For codepoints > U+FFFF, `length` returns 2. | APIs work on bytes. Use the `mb_*` functions to support UTF-8. |
| **Common functions** | `len(s)`<br>`s.upper()`<br>`s.find(sub)`<br>`s.replace(old, new)` | `s.length`<br>`s.toUpperCase()`<br>`s.indexOf(sub)`<br>`s.replace(old, new)` | `strlen($s)`<br>`strtoupper($s)`<br>`strpos($s, $sub)`<br>`str_replace($old, $new, $s)` |


## 4. Operators

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Arithmetic** | `+ - * / % **` | `+ - * / % **` | `+ - * / % **` |
| **Inc/Dec** | `x += 1` `x -= 1` | `++` `--` | `++` `--` |
| **Loose<br>comparison** | `< <= > >= == !=`<br>`1 < y <= 3` | `< <= > >= == !=` | `< <= > >= == !=` |
| **Strict<br>comparison** | - | `=== !==` | `=== !==` |
| **Logical** | `and` `or` `not` | `&&` `\|\|` `!` | `&&` `\|\|` `!` |
| **Bitwise** | `~` `\|` `&` `^` | `~` `\|` `&` `^` | `~` `\|` `&` `^` |
| **Shift** | `<<` `>>` | `<<` `>>` | `<<` `>>` |
| **Ternary** | `x if cond else y` | `cond ? x : y` | `cond ? x : y` |
| **Null<br>coalescing** | - | `val ?? 'default'` | `$val ?? 'default'` |
| **Chaining** | `obj.prop` | `obj.prop`<br>`obj?.prop` | `$obj->prop`<br>`$obj?->prop` |
| **String<br>concat** | `+` | `+` | `.` |

- Operators with two operands, often have a corresponding compound assignment operator that combines operation and assignment in a single step (`+=`, `-=`, `*=`, `/=`, ...).
- The Python **comparison** operators are **almost strict** except for `1 == True` and `0 == False` which are `True`.
- In JavaScript the null coalescing operator can be seen as `val !== null && val !== undefined ? val : 'default'`. As opposed to PHP, in JavaScript an exception is thrown if the tested variable has not been defined/declared.
- In PHP the null coalescing operator can be seen as `isset($val) ? $val : 'default'`.
- In JavaScript the optional chaining operator `?.` silently returns `undefined` when the left side is nullish (`undefined` or `null`).
- In PHP the null-safe operator `?->` silently returns `null` when the left side evaluates to `null`.


## 5. Collections

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Indexed array** | `mylist = [0, 1]`<br>`mytuple = (0, 1)` | `let arr = [0, 1]` | `$arr = [0, 1]` |
| **Associative array<br>(unique keys)** | `mydict = {'k1': "v1", 'k2': 2}` | `let mymap = new Map([['k1', "v1"], ['k2', 2]])`<br>`let obj = {k1: "v1", k2: 2}` | `$arr = ['k1' => "v2", 'k2' => 2]` |
| **Set<br>(unique values)** | `myset = {"v1", 2}` | `let myset = new Set(["v1", 2])` | - |
| **Size** | `len(collection)` | `arr.length`<br>`mymap.size`<br>`myset.size` | `count($arr)` |
| **Read** | `mylist[index]`<br>`mydict['k1']` | `arr[index]`<br>`mymap.get('k1')`<br>`obj['k1']`<br>`obj.k1` | `$arr[index]`<br>`$arr['k1']` |
| **Add** | `mylist.append(2)`<br>`mydict['k3'] = 3`<br>`myset.add("v2")` | `arr.push(2)`<br>`mymap.set('k3', 3)`<br>`obj['k3'] = 3`<br>`myset.add("v2")` | `$arr[] = 2`<br>`$arr['k3'] = 3` |
| **Del** | `mylist.pop(index)`<br>`mydict.pop('k3')`<br>`myset.remove("v2")` | `arr.pop()`<br>`mymap.delete('k3')`<br>`delete obj['k3']`<br>`myset.delete("v2")` | `array_pop($arr)`<br>`unset($arr['k1'])` |
| **Check item** | `'k1' in collection` | `arr.includes(1)`<br>`mymap.has('k1')`<br>`myset.has("v2")` | `in_array("v2", $arr)`<br>`array_key_exists('k1', $arr)`|
| **Get keys<br>and values** | `mydict.keys()`<br>`mydict.values()`<br>`mydict.items()` | `mymap.keys()`<br>`mymap.values()`<br>`mymap.entries()`<br>`Object.keys(obj)`<br>`Object.values(obj)`<br>`Object.entries(obj)` | `array_keys($arr)`<br>`array_values($arr)` |
| **Slice** | `mylist[start:end_exclusive]` | `arr.slice(start, end_exclusive)` | `array_slice($arr, $offset, $mylen)` |
| **Unpack or<br>Destructure** | `[x, y] = mylist`<br>`[x, y] = mydict.values()` | `const [x, y] = arr`<br>`const {k1, k2} = obj` | `[$x, $y] = $arr`<br>`['k1' => $x, 'k2' => $y] = $arr` |
| **Splat or<br>Spread** | Both sides:<br>`[0, 1, *mylist]`<br>Right side:<br>`{'k': "v", **mydict}` | Both sides:<br>`[0, 1, ...arr]`<br>Right side:<br>`{k: "v", ...obj}`<br>Left side:<br>`const {k1, ...obj}` | Right side:<br>`[0, 1, ...$arr]`<br>`['k': "v", ...$arr]` |

- **Python tuples**: they are immutable lists. For tuples the parentheses can be omitted when there is no ambiguity.
- **PHP arrays**: there is only one type, indexed arrays are associative arrays with integer keys. Arrays in PHP are assigned and passed **by value**.
- **JavaScript obj vs map**: objects only support strings as key, while maps support any value. Maps have a handy `size` property, but have to be accessed with the `get()` method. Objects are better for JSON serialization, while maps are optimized for iteration.
- **Sets**: in Python the insertion order is **not** preserved, whereas in JavaScript it is.


## 6. Control Flow

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **if** | `if x > 1:` | `if (x > 1) {}` | `if ($x > 1) {}` |
| **else if** | `elif x == 1:` | `else if (x === 1) {}` | `elseif ($x === 1) {}` |
| **else** | `else:` | `else {}` | `else {}` |
| **switch** | `match x:` | `switch (x) {}` | `switch ($x) {}` |
| **switch case** | `case 1:` | `case 1: .. break;` | `case 1: .. break;` |
| **switch default** | `case _:` | `default:` | `default:` |

- In Python each case is under its own block, while in JavaScript and PHP the cases are delimited by `break`.


## 7. Loops

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **while** | `while x > 1:` | `while (x > 1) {}` | `while ($x > 1) {}` |
| **do / while** | `-` | `do {} while (x < 10);` | `do {} while ($x < 10);` |
| **for** | `for i in range(mylen):` | `for (let i = 0; i < mylen; i++) {}` | `for ($i = 0; $i < $mylen; $i++) {}` |
| **Loop<br>collection** | `for item in items:` | `for (const item of items) {}` | `foreach ($arr as $v) {}` |
| **Loop<br>key-value** | `for k, v in mydict.items():` | `for (const [k, v] of mymap) {}`<br>`for (const [k, v] of Object.entries(obj)) {}` | `foreach ($arr as $k => $v) {}` |

- Use `break` to break out of a loop and `continue` to jump to the condition.
- In JavaScript to debug objects we can use `for (const k in obj) {}`. Note that it will loop over the entire prototype chain returning also inherited properties.


## 8. Exceptions

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Guarded<br>block** | `try:` | `try {}` | `try {}` |
| **Trigger<br>exception** | `raise Exception("Bad")` | `throw new Error("Bad")` | `throw new Error("Bad")` |
| **Handle<br>exception** | `except Exception as e:` | `catch (e) {}` | `catch (Error $e) {}` |
| **Run if no exception** | `else:` | - | - |
| **Run always** | `finally:` | `finally {}` | `finally {}` |

- JavaScript supports only one `catch (e)` block, inside that block we can distinguish the exception type with `e instanceof EvalError`.


## 9. Functions

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Declaration** | `def sub(a, b=0):` | `function sub(a, b=0) {}` | `function sub($a, $b=0) {}` |
| **return value** | `return a - b` | `return a - b` | `return $a - $b` |
| **Named args** | `sub(b=2, a=1)` | - | `sub(b: 2, a: 1)` |
| **Read/write<br>global var** | Needed for write:<br>`global g` | Declaration defines scope | Always needed:<br>`global $g` |
| **Arrow /<br>Lambda** | `lambda: print('Hi')`<br>`lambda a: a**2`<br>`lambda a, b: a - b` | `() => console.log('Hi')`<br>`a => a**2`<br>`(a, b) => a - b` | `fn() => echo 'Hi'`<br>`fn($a) => $a**2`<br>`fn($a, $b) => $a - $b` |

- Variables declared in Python or PHP functions have function scope unless `global` is used.
- Variables declared in JavaScript functions with `let` or `const` have block scope, those declared with `var` have function scope, and the ones declared without `let`, `const` or `var` become global.
- JavaScript supports multiple statements in **arrow** functions:  
`(a, b) => {console.log('Hi!'); return a - b;}`


## 10. Classes

| **Key Points** | **Python** | **JavaScript** | **PHP** |
| :---- | :---- | :---- | :---- |
| **Class<br>declaration** | `class C1:` | `class C1 {}` | `class C1 {}` |
| **Constructor** | `def __init__(self, param):` | `constructor(param) {}` | `function __construct($param) {}` |
| **Property<br>declaration** | **In constructor:**<br>`self.prop = param` | **In constructor:**<br>`this.prop = param` | **In class:**<br>`public $prop = "default"` |
| **Method<br>declaration** | `def method(self, param):` | `method(param) {}` | `function method($param) {}` |
| **Static<br>member<br>declaration** | `cnt = 0`<br>`@staticmethod`<br>`def inc():` | `static cnt = 0`<br>`static inc() {}` | `static $cnt = 0`<br>`static function inc() {}` |
| **Access member<br>inside method** | `self.prop`<br>`self.method(param)` | `this.prop`<br>`this.method(param)` | `$this->prop`<br>`$this->method($param)` |
| **Instance** | `obj = C1("val")` | `let obj = new C1("val")` | `$obj = new C1("val")` |
| **Access<br>member** | `obj.prop`<br>`obj.method(param)` | `obj.prop`<br>`obj.method(param)` | `$obj->prop`<br>`$obj->method($param)` |
| **Access<br>static<br>member** | `C1.cnt`<br>`C1.inc()` | `C1.cnt`<br>`C1.inc()` | `C1::$cnt`<br>`C1::inc()` |
| **Inheritance** | `class C2(C1):` | `class C2 extends C1 {}` | `class C2 extends C1 {}` |
| **Call<br>parent** | `super().__init__(param)`<br>`super().method(param)` | `super(param)`<br>`super.method(param)` | `parent::__construct($param)`<br>`parent::method($param)` |

- In Python the first parameter of non-static methods holds the current object, by convention it is named `self`.
  

## 11. Package Managers

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Install<br>location** | Global | `./node_modules/` | `./vendor/` |
| **Config files** | `requirements.txt`<br>maintained manually:<br>`pip freeze > requirements.txt` | `package.json`<br>`package-lock.json`<br>created with:<br>`npm init -y`<br>then maintained automatically. | `composer.json`<br>`composer.lock`<br>created and maintained automatically. |
| **Install from<br>Config files** | `pip install -r requirements.txt` | `npm ci` | `composer install` |
| **Install <pkg>** | `pip install <pkg>` | `npm install <pkg>` | `composer require <pkg>` |
| **List outdated** | `pip list --outdated` | `npm outdated` | `composer outdated` |
| **Update** | `pip install --upgrade <pkg>` | `npm update <pkg>` | `composer update <pkg>` |
| **Delete** | `pip uninstall <pkg>` | `npm uninstall <pkg>` | `composer remove <pkg>` |
