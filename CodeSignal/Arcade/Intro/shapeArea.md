Below we will define an n-interesting polygon. Your task is to find the area of a polygon for a given n.

A 1-interesting polygon is just a square with a side of length 1. 
An n-interesting polygon is obtained by taking the n - 1-interesting polygon and appending 1-interesting polygons to its rim, side by side. 
You can see the 1-, 2-, 3- and 4-interesting polygons in the picture below.

![area](https://user-images.githubusercontent.com/46931191/105102551-862a6980-5ae1-11eb-9423-f9cab20879e8.png)

```js
function shapeArea(n) {
    if(n <= 1)return 1;
    
    return shapeArea(n-1) + (n-1) * 4 ; 
}
```
