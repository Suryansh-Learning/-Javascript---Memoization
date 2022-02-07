# Memoization

**Reference Video:** https://www.youtube.com/watch?v=WbwP4w6TpCk&ab_channel=WebDevSimplified


**Without Memoization**

```javascript
function square(n) {
    let result = 0;
    for (let i=1; i <= n; i++) {
        for (let j=1; j <= n; j++) {
            result +=1;
        }
    }
    return result;
}
```

**With Memoization**

```javascript
const prevValues = [];

function square(n) {
    if (prevValues[n] != null) {
        return prevValues[n];
    }
    let result = 0;
    for (let i=1; i <= n; i++) {
        for (let j=1; j <= n; j++) {
            result +=1;
        }
    }
    prevValues[n] = result;
    // console.log(prevValues);
    return result;
}
```


**Without Memoization**

```javascript
function fib(n) {
    if (n <= 2) { 
        return 1;    
    } else {
        return fib(n-1) + fib(n-2);
    }
}
```


**With Memoization**

```javascript
function fib(n, prevValues = []) {
    if (prevValues[n] != null) {
        return prevValues[n];
    }
    let result;
    if (n <= 2) { 
        result = 1;    
    } else {
        result = fib(n-1) + fib(n-2);
    }
    prevValues[n] = result;
    return result;
}
```
