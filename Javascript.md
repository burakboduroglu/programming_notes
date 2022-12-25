### Javascript Array Methods

- #### -> **Map:**
  The map() method creates a new array with the results of calling a provided function on every element in the calling array.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.map(function (val) {
  return val * 2;
});
```

---

- #### -> **Filter:**
  The filter() method creates a new array with all elements that pass the test implemented by the provided function.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.filter(function (val) {
  return val % 2 === 0;
});
```

---

- #### -> **Reduce:**
  The reduce() method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.reduce(function (acc, val) {
  return acc + val;
}, 0);
```

---

- #### -> **Every:**
  The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.every(function (val) {
  return val % 2 == 0;
});
```

---

- #### -> **Some:**
  The some() method tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.some(function (val) {
  return val > 5;
});
```

---

- #### -> **Sort:**
  The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

```javascript
let arr = [12, 2, 34, 14, 5, 86, 17, 8, 91, 10];
let newArr = arr.sort(function (a, b) {
  return a - b;
});
```

---

- #### -> **Reverse:**
  The reverse() method reverses an array in place. The first array element becomes the last, and the last array element becomes the first.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.reverse();
```

---

- #### -> **Concat:**
  The concat() method is used to merge two or more arrays. This method does not change the existing arrays, but instead returns a new array.

```javascript
let arr1 = [1, 2, 3, 4, 5];
let arr2 = [6, 7, 8, 9, 10];
let newArr = arr1.concat(arr2);
```

---

- #### -> **Slice:**
  The slice() method returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included) where begin and end represent the index of items in that array. The original array will not be modified.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.slice(2, 5);
```

---

- #### -> **Splice:**
  The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.splice(2, 5);
```

---

- #### -> **Join:**
  The join() method joins all elements of an array into a string.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newStr = arr.join('-');
```

---

- #### -> **Split:**
  The split() method is used to split a string into an array of substrings, and returns the new array.

```javascript
let str = '1-2-3-4-5-6-7-8-9-10';
let newArr = str.split('-');
```

---

- #### -> **Push:**
  The push() method adds one or more elements to the end of an array and returns the new length of the array.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.push(11);
```

---

- #### -> **Pop:**
  The pop() method removes the last element from an array and returns that element. This method changes the length of the array.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.pop();
```

---

- #### -> **Shift:**
  The shift() method removes the first element from an array and returns that removed element. This method changes the length of the array.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.shift();
```

---

- #### -> **Unshift:**
  The unshift() method adds one or more elements to the beginning of an array and returns the new length of the array.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.unshift(0);
```

---

- #### -> **Includes:**
  The includes() method determines whether an array includes a certain value among its entries, returning true or false as appropriate.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let bool = arr.includes(5);
```

---

- #### -> **IndexOf:**
  The indexOf() method returns the first index at which a given element can be found in the array, or -1 if it is not present.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let index = arr.indexOf(5);
```

---

- #### -> **LastIndexOf:**
  The lastIndexOf() method returns the last index at which a given element can be found in the array, or -1 if it is not present. The array is searched backwards, starting at fromIndex.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 5, 10];
let index = arr.lastIndexOf(5);
```

---

- #### -> **Find:**
  The find() method returns the value of the first element in the provided array that satisfies the provided testing function. Otherwise undefined is returned.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.find(function (val) {
  return val === 5;
});
```

---

- #### -> **FindIndex:**
  The findIndex() method returns the index of the first element in the array that satisfies the provided testing function. Otherwise -1 is returned.

```javascript
let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let newArr = arr.findIndex(function (val) {
  return val === 5;
});
```

---

✅ If you like this article, you can give me a star on. 😎
Thanks for reading. 🙏
