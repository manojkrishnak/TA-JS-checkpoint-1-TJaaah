1. Using loops take 10 inputs from user and find the average of all the numbers.
>function avgOfNumbers(){
  let values = {};
  let sum =0;
  for(let i=1; i<=10; i++){
    values["num"+i] = +prompt("enter number");
  }
  for(var key in values){
    if(values.hasOwnProperty(key)){
      sum += values[key];
    }
  }
  console.log(sum, (Object.keys(values).length))
  return (sum/(Object.keys(values).length))
}
 
2. What will be the output of the code below

```js
let i = 0;
while (i < 3) {
  println('hi');
  i++;
}
```
//ReferenceError: println is not defined

3. Write a function named `getEvenSum` that accepts a parameter `max`. Return the sum of all even numbers. The value of max should default to 10.
>function getEvenSum(max = 10){
  let sum = 0;
  for(let i =1; i<=max; i++){
    if(i % 2 == 0){
      sum += i;
  }
  }
  return sum;
}
getEvenSum(20)

4. Write a function named `getOddSum` that accepts a parameter `max`. Return the sum of all odd numbers. The value of max should default to 10.
>function getOddSum(max = 10){
  let sum = 0;
  for(let i =1; i<=max; i++){
    if(i % 2 !== 0){
      sum += i;
  }
  }
  return sum;
}
getOddSum(20)

5. Write a function named `getProductOfDigits` that accepts a parameter `num`. It returns the product of all the digits in the number.

- If the input value is less than 0 return `not a valid input`
- For example if the input is `123` output should be `6`.
>function getProductOfDigits(num){
    let stringifiedNum = String(num);
    let productOfNums = 1;
    for(let i=0; i<stringifiedNum.length; i++){
      productOfNums = productOfNums * stringifiedNum[i]
    }
    return productOfNums;
}

getProductOfDigits(123);

6. What will be the output of the following code below in multiple conditions? Explain with reason?

```js
function check(num) {
  if (num > 5) {
    return 'Bigger than 5';
  }

  if (num < 5) {
    return 'Smaller than 5';
  }

  return num;
}

check(10); // Bigger than 5
check(1); // Smaller than 5
check(5); // Smaller than 5
```

7. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === 'Arya') return 'You are arya';
  if (name === 'John') return 'You are john';
  return 'Who are you';
}

getOutput('Arya'); // you are arya is returned and anything after return is not executed and ignored.
getOutput('John'); // you are arya is returned and anything after return is not executed and ignored.
getOutput(); // who are you is returned and nothing is printed in console
```

8. What will be the output of the following code given below? Explain the reason?

```js
function getOutput(name) {
  if (name === 'Arya') console.log('You are arya');
  if (name === 'John') console.log('You are john');
  return 'Who are you';
}

getOutput('Arya'); // You are arya gets printed in the console and who are you is returned
getOutput('John'); // You are arya John printed in the console and who are you is returned
getOutput(); // who are you is returned and nothing is printed in console
```

9. Can a function have multiple return statement? Give one example if possible and explain the reason.

10. What is the difference between `for` loop and `while` loop. What are the different place you can use them? Explain with example.
>for loop is used when we dont know the no of values on which the loop has to run, whereas in while loop we give the condition in the while loop so that till the time the condition is valid the loop keeps on running. 
In foor loop syntax itself we have place to increment the value and in the while loop if we dont increment the value it goes to infinite loop
