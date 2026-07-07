# Day 1: Variables, Types, Operators - Quick Reference

## var vs let vs const

| | var | let | const |
|---|---|---|---|
| Scope | Function | Block | Block |
| Reassignment | ✅ | ✅ | ❌ |
| Redeclaration | ✅ | ❌ | ❌ |
| Hoisting | ✅ (undefined) | ❌ (error) | ❌ (error) |
| Use in 2024 | ❌ Avoid | ✅ Default | ✅ Prefer |

```javascript
var x = 1;      // Function scoped, old way
let y = 2;      // Block scoped, modern
const z = 3;    // Block scoped, immutable
```

**Rule:** Use `const` by default. Use `let` if you need to reassign. Never use `var`.

---

## Primitive Types

```javascript
typeof "hello"           // "string"
typeof 42                // "number"
typeof true              // "boolean"
typeof undefined         // "undefined"
typeof null              // "object" (quirk!)
typeof Symbol("id")      // "symbol"
typeof 123n              // "bigint"
```

---

## Operators

### Arithmetic
```javascript
5 + 3       // 8 (addition)
5 - 3       // 2 (subtraction)
5 * 3       // 15 (multiplication)
5 / 3       // 1.666... (division)
5 % 3       // 2 (modulo - remainder)
5 ** 3      // 125 (exponent)
```

### Comparison
```javascript
5 === 5     // true (strict - same type AND value)
5 == "5"    // true (loose - coerces types)
5 !== 5     // false
5 > 3       // true
5 >= 5      // true
5 < 10      // true
5 <= 5      // true
```

**IMPORTANT:** Use `===` and `!==`, avoid `==` and `!=`

### Logical
```javascript
true && true    // true (AND)
true || false   // true (OR)
!true           // false (NOT)
```

---

## Type Coercion (The Gotcha)

JavaScript tries to convert types automatically:

```javascript
"5" + 3         // "53" (concatenation)
"5" - 3         // 2 (converts to number)
true + 1        // 2 (true = 1)
false + 1       // 1 (false = 0)
"hello" == 5    // false (can't coerce meaningfully)
0 == false      // true (coerces)
0 === false     // false (strict, different types)
```

---

## How to Debug

Use `console.log()` constantly:

```javascript
const x = "5";
console.log(x + 3);        // "53"
console.log(typeof x);     // "string"
console.log(Number(x));    // 5 (explicit conversion)
console.log(typeof Number(x)); // "number"
```

---

## Key Takeaways

1. ✅ Use `const` first, `let` if you reassign, never `var`
2. ✅ Use `===` for comparison, not `==`
3. ✅ Understand type coercion but prefer explicit conversion
4. ✅ Use `console.log()` to debug EVERYTHING
5. ✅ Read error messages carefully

---

## When You're Stuck

1. Add `console.log()` to see what's happening
2. Check the type with `typeof`
3. Read the error message (it usually tells you)
4. If still stuck, check `/learning-material/` for that concept
5. Last resort: ask Claude
