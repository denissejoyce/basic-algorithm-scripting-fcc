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

### Confirm the Ending
```javascript
function confirmEnding(str, target) {
  return (str.slice(str.length-target.length)==target);
}
```

### Repeat a String Repeat a String
```javascript
function repeatStringNumTimes(str, num){
    if(num <= 0){
        return "";
    } else {
        return str + repeatStringNumTimes(str, num-1);
    }
}
```

### Truncate a String
```javascript
function truncateString(str, num) {
  return (str.length <= num) ? str
  : str = (`${str.slice(0, num)}...`);
}
```

### Finders Keepers
```javascript
function findElement(arr, func) {
  let num = 0;
  for(let elem of arr){
      if (func(elem)){
          return num = elem;
      }
  }
  return undefined;  
}
```

### Boo Who
```javascript
function booWho(bool) {
  return (typeof(bool) === "boolean") ? true : false;
}
```

### Title Case a Sentence
```javascript
function titleCase(str) {
    str = str.toLowerCase().split(" ");
    for(let i=0; i<str.length; i++){
        str[i] = str[i].charAt(0).toUpperCase().concat(str[i].slice(1));
    }
    return str.join(" ");
}
```

### Slice and Splice
```javascript
function frankenSplice(arr1, arr2, n) {
  let temp = arr2.slice(0);
  temp.splice(n, 0, ...arr1);
  return temp;
}
```

### Falsy Bouncer
```javascript
function bouncer(arr) {
  return arr.filter((arr) => (!!arr));
}
```

### Where do I Belong
```javascript
function getIndexToIns(arr, num) {
  if(arr.indexOf(num) < 0){
      arr.push(num);
  }
  return arr.sort(sortAscend).indexOf(num);
}

function sortAscend(a,b){ return a - b; }
```

### Mutations
```javascript
function mutation(arr) {
  let arr1 = arr[0].toLowerCase().split(""),
      arr2 = arr[1].toLowerCase().split("");
  for(let item of arr2){
      if(arr1.indexOf(item) < 0){
          return false;
      }
  }
  return true;
}
```

### Chunky Monkey
```javascript
function chunkArrayInGroups(arr, size) {
  let temp = [];
  for(let i=0; i<arr.length; i+=size){
      temp.push(arr.slice(i, i+size));
  }
  return arr = temp;
}
```
