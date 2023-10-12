# Basic Algorithm Scripting (FreeCodeCamp) Solutions
 This repository contains my answers to the challenges from FreeCodeCamp's Basic Algorithm Scripting module.

### Celsius to Fahrenheit
```javascript
function convertCtoF(celsius) {
  return fahrenheit = (celsius*(9/5))+32;
};
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
