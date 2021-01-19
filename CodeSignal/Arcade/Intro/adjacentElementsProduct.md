Given an array of integers, find the pair of adjacent elements that has the largest product and return that product.

```js
function adjacentElementsProduct(inputArray) {
    let largestProduct = inputArray[0] * inputArray[1];
    for(let i=0; i < inputArray.length ; i++){
        if(inputArray[i] * inputArray[i+1] > largestProduct){
            largestProduct = inputArray[i] * inputArray[i+1]
        }
    }
    return largestProduct
}

```
