## `Fetch API:`
- The Fetch API is a JavaScript interface that allows for making network requests in a modern and flexible way.

```javascript
fetch("https://jsonplaceholder.typicode.com/users")
    .then(resp => resp.json())
    .then(console.log)
```
- This code block uses the Fetch API to make a GET request to the URL "https://jsonplaceholder.typicode.com/users", which returns a JSON response containing an array of user data.
- The `then()` method is used twice to handle the response: the first `then()` method converts the response to a JSON object, and the second `then()` method logs the JSON object to the console.

## `Promise:`
- A promise is a JavaScript object that represents an eventual result of an asynchronous operation.
```javascript
const promise = new Promise((resolve, reject) => {
    if(true){
        resolve("RESOLVE WORKED!!!")
    } else {
        reject("REJECT WORKED!!!")
    }
})
promise.then(result => console.log(result))
```
- This code block creates a new Promise object that takes a function as an argument with resolve and reject functions as parameters.
- The if statement checks whether a condition is true or false, and if true, the resolve function is called with a message.
- The then() method is used to handle the resolved value of the promise and logs it to the console.

## `ASYNC Function:`
- An async function in JavaScript allows you to write asynchronous code that looks like synchronous code, making it easier to read and understand.
```javascript
async function fetchUsers(){
    const resp = await fetch(urls[0]);
    const data = await resp.json();
    console.log(data);
}
fetchUsers();
```
- This code block declares an `async` function `fetchUsers()` which makes an asynchronous network request using the Fetch API to the URL stored in the `urls` array. The `await` keyword is used to wait for the response from the request and then for the response body to be converted to a JSON object. 
- Finally, the JSON object is logged to the console using `console.log()`. The `fetchUsers()` function is then called to execute this asynchronous operation.

## `More Example About This Topic:`
### `Example-1:`
```javascript
const urls = [
    "https://jsonplaceholder.typicode.com/users",  //users
    "https://jsonplaceholder.typicode.com/albums", //albums
    "https://jsonplaceholder.typicode.com/photos"  //photos
]

// With Promise
Promise.all(urls.map(url =>
    fetch(url).then(resp => resp.json())
)).then(arr => {
    console.log("Users: ", arr[0]);
    console.log("Albums: ", arr[1]);
    console.log("Photos: ", arr[2]);
}).catch("Errorrrrr!!!!");

```

### `Example-2:`
```javascript
const urls = [
    "https://jsonplaceholder.typicode.com/users",  //users
    "https://jsonplaceholder.typicode.com/albums", //albums
    "https://jsonplaceholder.typicode.com/photos"  //photos
]

// With ASYNC-AWAIT
try {
    const getData = async function() {
        const [users, albums, photos] = await Promise.all(urls.map(url => fetch(url).then(resp => resp.json())))
        console.log("Users: ", users);
        console.log("Albums: ", albums);
        console.log("Photos: ", photos);
    }
    getData();
} catch (err) {
    console.log("Errorrrr!!!");
    console.log(err);
}
```