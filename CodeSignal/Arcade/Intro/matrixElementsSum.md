After becoming famous, the CodeBots decided to move into a new building together. Each of the rooms has a different cost, and some of them are free, but there's a rumour that all the free rooms are haunted! Since the CodeBots are quite superstitious, they refuse to stay in any of the free rooms, <b>or any of the rooms below any of the free rooms.</b>

Given matrix, a rectangular matrix of integers, where each value represents the cost of the room, your task is to return the total sum of all rooms that are suitable for the CodeBots (ie: add up all the values that don't appear below a 0).

```js
function matrixElementsSum(matrix) {
   let row = matrix.length;
   let col = matrix[0].length;
   
   let sum = [...matrix[0]];
   let prevroom = matrix[0];
   for(i=1; i<row; i++){
       for(j=0;j<col; j++){
           if(matrix[i-1][j] < 1){
               prevroom[j] = 0;
           }
           if(prevroom[j] != 0){
               sum.push(matrix[i][j]);
           }
       }
   }
   return sum.reduce((a,b)=> a+b);
}

```
