# Memoization

**Reference Video:** https://www.youtube.com/watch?v=WbwP4w6TpCk&ab_channel=WebDevSimplified


**Without Memoization**
```
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
