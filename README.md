# Basic Algorithm Scripting (FreeCodeCamp) Solutions
 This repository contains my answers to the challenges from FreeCodeCamp's Basic Algorithm Scripting module.

### Celsius to Fahrenheit
```javascript
function convertCtoF(celsius) {
  return fahrenheit = (celsius*(9/5))+32;
};
```

### Reverse a String
```javascript
function reverseString(str) {
    let temp = ``;
    for (let i = str.length-1; i > -1; i--){
    	temp += str[i];
    }
    str = temp;
    return str;
}
```

### Factorialize a Number
```javascript
function factorialize(num){
	if(num == 0){
		return 1;
	} else {
		return num * factorialize(num-1);
	}
}
```

### Find the Longest Word in a String
```javascript
function findLongestWordLength(str) {
	let arr, highest;
	str = str.replace(/[^a-z 0-9]/ig, "");
	arr = str.split(" ");
	
	highest = arr[0];
	for(let i=0; i<arr.length-1; i++){
		if(highest.length<arr[i+1].length){
        	highest = arr[i+1];
    		}
	}
	str = highest;
  	return str.length;
}
```

### Return Largest Numbers in Arrays
```javascript
function largestOfFour(arr) {
  let temp = [];
  for(let i=0; i<arr.length; i++){
      temp.push(Math.max(...arr[i]));
  }
  arr = temp;
  return arr;
}
```
