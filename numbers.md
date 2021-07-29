#CONVERTING AND CHECKING NUMBERS#

1. Converting strings to number without using "Number"
- console.log(typeof +'23');

2. Extracting numbers from a string using parsing (The string must start with numbers)
- console.log(Number.parseInt('1423px'));

3. parseInt only extracts the integer part of the Number
- console.log(Number.parseInt('2.5px'));

4. parseFloat extracts floating numbers (decimal numbers) 
- console.log(Number.parseFloat('2.5px'));

5. isFinite is the best way to check if a value is a number or not
- console.log(Number.isFinite(+'23/0'));



#MATH AND ROUNDING#

1. Square root 
- console.log(Math.sqrt(25));
- console.log(25 ** (1/2))

2. Cubic root
- console.log(27 ** (1/3))

3. Maximum Number
- console.log(Math.max(2, 5, 45, 54, 6));

4. Minimum Number
- console.log(Math.min(2, 5, 45, 54, 6));

5. Generate Random Numbers (To get values between 1 and 6)
- console.log(Math.floor(Math.random() * 6) + 1)

6. Rounding Integers (Cuts off the decimal numbers => 44)
- console.log(Math.trunc(44.5454));

7. Rounding Up Integers (Converts to the nearest whole number => 45)
- console.log(Math.round(44.5454));
- console.log(Math.ceil(44.8454));

8. Rounding Down Integers (Converts to the nearest whole number => 45)
-console.log(Math.floor(44.8454)); //floor works in all situations unlike trunc

9. Rounding decimals (toFixed(Number of decimals after the integer))
- console.log((2.5).toFixed(0));
- console.log((2.5).toFixed(6));


#THE REMAINDER OPERATOR (%)#

console.log(5 % 2);

//Find an even number 
const number = 32;
const evenNumberChecker = (num) => {
  const even = num % 2 === 0? `${num} is an even number`: `${num} is not an even number`;
  console.log(even)
}
evenNumberChecker(number);




#WORKING WITH BigInt (Big Numbers)  ===> BigInt(number) or 23434234n#

//53bits
//64bits

const hugeNumber = 23904823312n;
console.log(typeof hugeNumber)

const num = 328239432423423423;
console.log(typeof BigInt(num));



#CREATING DATES#

1. Generate current date values

const today = new Date();
console.log(today.getDate())
console.log(today.getDay())
console.log(today.getFullYear())
console.log(today.getHours())
console.log(today.toISOString()) 
console.log(today.getTime())  //Time stamp (1970)

2. Parsing custom date values

const now = new Date('31 November, 1995');
console.log(now)
