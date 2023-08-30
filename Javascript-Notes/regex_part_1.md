# Regular Expressions Cheat Sheet PART - 1

Regular expressions are a powerful tool for matching patterns in text. This blog post will introduce some of the basic syntax for regular expressions and how to use them in JavaScript.

## Creating a Regular Expression

There are two ways to create a regular expression in JavaScript. The first is to use the `RegExp` constructor:

```javascript
let text = "Programming is my favorite thing to do in the world.";

let regex1 = new RegExp("Programming");
let regex2 = /Programming/;

// .test()
console.log(regex1.test(text)); // true
console.log(regex2.test(text)); // true

// .exec()
console.log(regex1.exec(text)); // ["Programming", index: 0, input: "Programming is my favorite thing to do in the world."]
console.log(regex2.exec(text)); // ["Programming", index: 0, input: "Programming is my favorite thing to do in the world."]

// .match()
console.log(text.match(regex)); // ["Programming", index: 0, input: "Programming is my favorite thing to do in the world."]

// .search()
console.log(text.search(regex)); // 0

// .replace()
console.log(text.replace(regex, "Coding")); // Coding is my favorite thing to do in the world.

// .split()
console.log(text.split(regex)); // ["", " is my favorite thing to do in the world."]

// /\s/
console.log(text.split(/\s/)); // ["Programming", "is", "my", "favorite", "thing", "to", "do", "in", "the", "world."]
```

`.test()` returns a boolean value indicating whether or not the regular expression matches the text.
`.exec()` returns an array containing the matched text, the index of the match, and the input string.
`.match()` returns an array containing the matched text, the index of the match, and the input string.
`.search()` returns the index of the first match.
`.replace()` returns a new string with the matched text replaced by the second argument.
`.split()` returns an array of strings split at the matched text.
`/\s/` is a regular expression that matches whitespace characters.

> exec and match are the same, but `match` is a string method and `exec` is a RegExp method.

### Flags

Regular expressions can also have flags. Flags are added to the end of the regular expression and change the behavior of the regular expression. Usage of flags is demonstrated below:

- /pattern/flags
- new RegExp("pattern", "flags")

Flags

- `g` - global, match all instances of the pattern
- `i` - ignore case, match regardless of case
- `m` - multiline, match across multiple lines

```javascript
let text = "Programming is my favorite thing to do in the world.";
let regex1 = /o\s/;

console.log(text.match(regex1)); // ["o ", index: 13, input: "Programming is my favorite thing to do in the world."]

let regex2 = /o\s/g;

console.log(text.match(regex2)); // ["o ", "o "]

let regex3 = /G\s/gi;

console.log(text.match(regex3)); // ["g ", "g "]
```

Explanation of the above code:

- `regex1` matches the first instance of the pattern.
- `regex2` matches all instances of the pattern.
- `regex3` matches all instances of the pattern regardless of case.

## Recommended Resources

Regex Pal is a great tool for testing regular expressions: https://www.regexpal.com/

## Wildcards

Wildcards are characters that match any character. The wildcard character is `.`. The following example demonstrates the use of the wildcard character:

```javascript
let text = "Programming is my favorite thing to do in the world.";
let regex1 = /w.r/g;

console.log(text.match(regex1)); // ["wor"]

let regex2 = /w\./gi;

console.log(text.match(regex2)); // ["w."]
```

Explanation of the above code:

- `regex1` matches any character between `w` and `r`.
- `regex2` matches any character between `w` and `.`.

```javascript
let text = "He is holding his hat in his hand.";
let regex1 = /h../g;

console.log(text.match(regex1)); // ["hol", "his", "hat", "his", "han"]

let regex2 = /h../gi;

console.log(text.match(regex2)); // ["He ", "hol", "his", "hat", "his", "han"]
```

## Control Characters

- `\t` is a tab character
- `\n` is a newline character
- `\r` is a carriage return character
- `\v` is a vertical tab character

## Using Character Sets

```javascript
let text1 = "Gray, Grey, Grab";
let regex1 = /Gr[ae]y/g;

console.log(text.match(regex1)); // ["Gray", "Grey"]

let text2 = "Programming is my favorite thing to do in the world.";
let regex2 = /[aei][ w]/g;

console.log(text2.match(regex2)); // "e " -> from "favorite", "e " -> from "the"
```

## Specifying Ranges

```javascript
let text1 = "1 11 a b c abc";
let regex1 = /[1-6a-z]/g;

console.log(text1.match(regex1)); // ["1", "1", "a", "b", "c", "a", "b", "c"]

let text2 = "13-20";
let regex2 = /[10-20]/;

console.log(text2.match(regex2)); // ["1","2","0"]
```

## Excluding a Character Set

```javascript
let text1 = "1 2 33 123 12 93 85 abcd";
let regex1 = /[^0-9]/;

console.log(text1.match(regex1)); //  a b c d and all spaces
```

## Shorthand of Character Set

- `\d` -> [0-9]
- `\w` -> [a-zA-Z0-9_]
- `\s` -> [ \t\r\n]

```javascript
let text1 = "1 2 33 123 12 93 85 abcd";
let regex1 = /\d/g;

console.log(text1.match(regex1)); // ["1", "2", "3", "3", "1", "2", "9", "3", "8", "5"]

let text2 = "Programming is my favorite thing to do in the world.";
let regex2 = /\w/g;

console.log(text2.match(regex2)); // ["P", "r", "o", "g", "r", "a", "m", "m", "i", "n", "g", "i", "s", "m", "y", "f", "a", "v", "o", "r", "i", "t", "e", "t", "h", "i", "n", "g", "t", "o", "d", "o", "i", "n", "t", "h", "e", "w", "o", "r", "l", "d"]

let text3 = "Programming is my favorite thing to do in the world.";
let regex3 = /\s/g;

console.log(text3.match(regex3)); // [" ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " ", " "]
```

- `\D` -> [^0-9]
- `\W` -> [^a-zA-Z0-9_]
- `\S` -> [^ \t\r\n]

```javascript
let text1 = "1 2 33 123 12 93 85 abcd";
let regex1 = /\D/g;

console.log(text1.match(regex1)); // [" ", " ", " ", " ", " ", " ", " ", "a", "b", "c", "d"]
```

## Repetitions

- `*` -> It used to match 0 or more times
- `+` -> It used to match 1 or more times
- `?` -> It used to match 0 or 1 time

### Greedy and Lazy Matching

`Greedy matching` is the default behavior of regular expressions. Greedy matching means that the regular expression will match as many characters as possible. `Lazy matching` means that the regular expression will match as few characters as possible.

```javascript
let html = "<h1>Heading</h1><p>Paragraph</p>";
let h1Regex = /<h1>.*<\/h1>/;

console.log(html.match(h1Regex)); // ["<h1>Heading</h1>"]
```

### Specifying the Repetition Amount

- `{n}` -> It used to match exactly n times
- `{n,}` -> It used to match at least n times
- `{n,m}` -> It used to match at least n times and at most m times

```javascript
let text1 = "Programming is my favorite thing to do in the world.";
let regex1 = /\w{3,5}/g;

console.log(text1.match(regex1)); // ["Program", "ming", "favor", "ite", "thing", "world"]
```

### Example

- Validate phone numbers, check to see if it matches these formats:
  - (nnn)-nnn-nnnn
  - nnn.nnn.nnnn
  - nnn-nnn-nnnn
  - nnnnnnnnnn
  - (nnn)nnnnnnn

`Solution`:

```javascript
let phoneNumber = 555 - 444 - 3333;
let regex = /\(?\d{3}\)?-?\d{3}-?\d{4}/;

console.log(phoneNumber.match(regex));
```

`Explanation`: /\(?\d{3}\)?-?\d{3}-?\d{4}/

- `\(?` -> It matches 0 or 1 time "("
- `\d{3}` -> It matches exactly 3 times digit
- `\)?` -> It matches 0 or 1 time ")"
- `-?` -> It matches 0 or 1 time "-"
- `\d{3}` -> It matches exactly 3 times digit
- `-?` -> It matches 0 or 1 time "-"
- `\d{4}` -> It matches exactly 4 times digit

If you have any recommendations or feedback, please feel free to reach out to me on comment. However Part-2 will be coming soon. Stay tuned.

## Follow me on GitHub

[GitHub](https://github.com/burakboduroglu)
