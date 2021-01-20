Given a sequence of integers as an array, determine whether it is possible to obtain a strictly increasing sequence by removing no more than one element from the array.

Note: sequence a0, a1, ..., an is considered to be a strictly increasing if a0 < a1 < ... < an. Sequence containing only one element is also considered to be strictly increasing.

```js
function almostIncreasingSequence(sequence) {
    let max = Math.pow(-10, 5);
    let secondmax = Math.pow(10, 5);
    let strike = 0;
    sequence.map(val=>{
        if(val > max){
            secondmax = max;
            max= val;
        }else if(val > secondmax){
            max = val;
            strike++;
        }else{
            strike++
        }
    })
    return strike <= 1 ;
}
```
