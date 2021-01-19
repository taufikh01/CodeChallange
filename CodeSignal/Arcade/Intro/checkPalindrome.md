Given the string, check if it is a palindrome.

```js
function checkPalindrome(inputString) {
    const reverse = inputString.split('').reverse().join('');
    return inputString === reverse;
}
```
