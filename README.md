# Python vs JavaScript vs PHP: Syntax Comparison

This guide provides a side-by-side comparison of three of the most popular programming languages.

## 1. Basic Syntax

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Whitespaces & Indentation** | **Strict Indentation:** Meaningful whitespace. | **Ignored:** Blocks defined by `{}`. | **Ignored:** Blocks defined by `{}`. |
| **Line Termination** | **Newline:** Semicolons optional. | **Optional Semicolon:** ASI used, `;` recommended. | **Required Semicolon:** Strictly required `;`. |
| **Case Sensitivity** | **Fully Sensitive** | **Fully Sensitive** | **Mixed:** Vars sensitive; functions/keywords insensitive. |

## 2. Variables, Constants, and Data Types

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Variables** | `name = "Bob"` | `let name = "Bob";` | `$name = "Bob";` |
| **Constants** | `PI = 3.14` (Convention) | `const PI = 3.14;` | `const PI = 3.14;` |
| **Null/Missing** | `None` | `null` and `undefined` | `null` |

## 3. Strings

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Interpolation** | `f"Hi {name}"` | ` `Hi ${name}` ` | `"Hi $name"` |
| **Multi-line** | `"""Line 1\nLine 2"""` | ` `Line 1\nLine 2` ` | `<<<EOF\nLine 1\nLine 2\nEOF;` |

## 4. Operators

| **Key Points** | **Python** | **JavaScript** | **PHP** | 
| :--- | :--- | :--- | :--- |
| **Arithmetic** | `**` (power), `//` (floor) | `**` (power) | `**` (power) |
| **Comparison** | `==`, `is` (identity) | `==`, `===` (strict) | `==`, `===` (strict) |
| **Logical** | `and`, `or`, `not` | `&&`, `||`, `!` | `&&`, `||`, `!` |

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
