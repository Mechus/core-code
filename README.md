# core-code
Core Code bootcamp

### Tuesday 11/01/2022
- Java language is compiled or interpreted?  
**Java es lenguaje compilado e interpretado.**

- Create an algorithm to calculate the equivalent of your local currencty to USD  
**Ingresar monto de moneda local  
Validar si monto es valido  
Si no es valido mostrar error y terminar  
Si monto es valido consultar equivalencia de moneda local a 1 dolar  
Dividir monto de moneda local dentro de equivalencia a 1 dolar 
Mostrar monto total en dolares**

- Why is pseudocode helpful?  
**Es importante para tener un boceto de la idea o algoritmo que queremos transformar en el lenguaje que deseamos implementar, asi poder identificar mejor la idea para optimizar y tener un codigo mas limpio.**

- Create a pseudocode to calculate the aproximated age of a user base on the year they born  
**INICIO PROGRAMA  
DECLARAR listadoUsuarios, anioActual  
LEER listado  
GUARDAR (listadoUsuarios,listado);  
LEER añoActual  
GUARDAR (anioActual,añoActual);  
RECORRER listadoUsuarios  
  CALCULAR anioActual - anioNacimiento  
  MOSTRAR CALCULO  
FIN RECORRER  
FIN PROGRAMA**

- Why are flowcharts important to us as developers?  
**Son importantes para documentar y planificar la construccion de funciones que se implementan dentro de nuestro codigo. Tambien para plasmar de forma grafica la idea del algoritmo que deseamos implementar.**


### Wednesday 12/01/2022
- Translate the year you where born to binary, decimal and hexadecimal  
**1994 -> 11111001010**  
1994 / 2 = 997 + 0  
997 / 2 = 498 + 1  
498 / 2 = 249 + 0  
249 / 2 = 124 + 1  
124 / 2 = 112 + 0  
62 / 2 = 31 + 0  
31 / 2 = 15 + 1  
15 / 2 = 7 + 1  
7 / 2 = 3 + 1  
3 / 2 = 1 + 1  
1 / 2 = 0 + 1  
 
**1994 -> 7CA**  
1994 / 16 = 124 , 10 -> A  
124 / 16 = 7 , 12 -> C  
7 / 16 = 0 , 7 -> 7  

- Translate 51966 into hexadecimal and binary
**51966 -> 1100101011111110**  
51966 / 2 = 25983 + 0  
25983 / 2 = 12991 + 1  
12991 / 2 = 6495 + 1  
6495 / 2 = 3247 + 1  
3247 / 2 = 1623 + 1  
1623 / 2 = 811 + 1  
811 / 2 = 405 + 1  
405 / 2 = 202 + 1  
202 / 2 = 101 + 0  
101 / 2 = 50 + 1  
50 / 2 = 25 + 0  
25 / 2 = 12 + 1  
12 / 2 = 6 + 0  
6 / 2 = 3 + 0  
3 / 2 = 1 + 1  
1 / 2 = 0 + 1  

**51966 -> CAFE**  
51966 / 16 = 3247 , 14 -> E  
3247 / 16 = 202 , 15 -> F  
202 / 16 = 12 , 10 -> A  
12 / 16 = 0 , 12 -> C  


- Create a program to add two numbers given by the user
```
.data
	title: .asciiz "\nPrograma para realizar sumas de 2 numeros\n"
	result: .asciiz "\nEl resultado de la suma es: "
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
.text
	main:
      		li $v0, 4
      		la $a0, title
      		syscall
      		
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0

		add $t2, $t0, $t1
		
      		li $v0, 4
      		la $a0, result
      		syscall
		
		li $v0, 1
		move $a0, $t2
		syscall
```

- Create a program that display your name
```
.data
	title: .asciiz "\nPrograma para mostrar mi nombre\n"
	result: .asciiz "\nMi nombre es: Edgar Nemecio Ortiz Barrientos"
.text
	main:
      		li $v0, 4
      		la $a0, title
      		syscall
      				
      		li $v0, 4
      		la $a0, result
      		syscall
		
		li $v0, 1
		move $a0, $t3
		syscall
```


### Thursday 13/01/2022  
- Search for real word applications of Javascript  
Gmail, Facebook, Twitter, Outlook, Atom, VSCode


### Tuesday 18/01/2022. 
- Multiply  
```
function multiply(a, b){
 return a * b
}
```

- ASCII Total  
```
function uniTotal (string) {
 let total = 0;
  for(let i = 0; i<string.length; i++){
    total += string.charCodeAt(i);
  }
  return total
}
```

- get character from ASCII Value  
```
function getChar(c){
  return String.fromCharCode(c);
}
```

- Binary Addition. 
```
function addBinary(a,b) {
 return (a+b).toString(2);
}
```

- Student's Final Grade. 
```
function finalGrade (exam, projects) {
  if(exam > 90 || projects > 10)return 100;
  else if(exam > 75 && projects >= 5) return 90;
  else if(exam > 50 && projects >= 2) return 75;
  else return 0;
}
```


### Wednesday 19/01/2022. 
- Holiday VIII - Duty Free  
```
function dutyFree(normPrice, discount, hol){
  return Math.floor(hol/(normPrice*(discount/100)));
}
```

- Twice as old 
```
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs(dadYearsOld-(2*sonYearsOld));
}
```

- Valid Spacing 
```
function validSpacing(s) {
  let newS = s.trim();
  if(s != newS)return false;
  if(newS.search(/\s\s+/) > 0)return false;
  return true;
}
```

- Fake Binary 
```
function fakeBin(x){
 return x.replace(/[0-4]/g,'0').replace(/[5-9]/g,'1')
}
```

### Thursday 20/01/2022. 
- Exclamation marks series #2: Remove all exclamation marks from the end of sentence. 
```
function remove (string) {  
  return string.replace(/!+$/, '');
}
```

- Vowel remover. 
```
function shortcut (string) {
  return string.replace(/[aeiou]/g,'');
}
```

- Rock Paper Scissors!  
```
const rps = (p1, p2) => {
  if(p1 === p2) return 'Draw!';
  switch(p1){
    case 'scissors':
      if(p2 === 'paper') return 'Player 1 won!';
      return 'Player 2 won!';
    case 'paper':
      if(p2 === 'rock') return 'Player 1 won!';
      return 'Player 2 won!';
    case 'rock':
      if(p2 === 'scissors') return 'Player 1 won!';
      return 'Player 2 won!';
    default:
      return 'Error';
  }
};
```

- Persistent Bugger.  
```
function persistence(num) {
   let strNum = num.toString();
   let long = strNum.length;
   let newNum = 1;
   if(long <= 1) return 0;
   for(let i = 0; i < long; i++){
     newNum = newNum * strNum[i];
   }   
   return persistence(newNum) + 1;
}
```

### Monday 24/01/2022. 
- Who likes it?   
```
function likes(names) {
  // TODO
  let l = names.length;
  if(l <= 0) return 'no one likes this';
  if(l == 1) return names[0] + ' likes this';
  
  let result;
  for(let i = 0; i < l-1; i++){
    result = result ? result + ', ' + names[i] : names[i];
    if(i >= 1) break;
  }
  result = l > 3 ? result + ' and ' + (l-2) + ' others' : result + ' and ' + names[l-1];
  
  return result + ' like this';
}
```

- Bit Counting   
```
var countBits = function(n) {
  // Program Me
  return [...n.toString(2)].filter(x => x == 1).length;
};
```

- Decode the Morse code   
```
decodeMorse = function(morseCode){
  //your code here
  let allSentence = '';
  let words = morseCode.trim().split(/\s\s\s/g);
  for(let i = 0, l = words.length; i < l; i++){
    let newWord = words[i].split(' ');
    allSentence += allSentence ?  ' ' : '';
    for(let j = 0, l2 = newWord.length; j < l2; j++){
      allSentence += MORSE_CODE[newWord[j]];
    }
  }
  return allSentence;
}
```


### Tuesday 25/01/2022. 
- Your order, please   
```
function order(words){
  // ...
  return words.split(' ').sort((a,b) => {
    let aIndex = a.match(/[0-9]/g);
    let bIndex = b.match(/[0-9]/g);
    return aIndex[0] < bIndex[0] ? -1 : 1;
  }).join(' ');
}
```

- Counting Duplicates   
```
function duplicateCount(text){
  //...
  let count = 0;
  while(text[0]){
    let finds = text.match(new RegExp(text[0], "gi"));
    if(finds && finds.length > 1)count++;
    text = text.replace(new RegExp(text[0], "gi"),'');
  }
  return count;
}
```

- Simple Pig Latin   
```
function pigIt(str){
  //Code here
  let arrStr = str.split(' ');
  for(let i = 0, l = arrStr.length; i < l; i++){
    if(!arrStr[i].match(/[!¡¿?,;.:]/g)){
      let temp = [...arrStr[i]];
      temp.splice(0,1);
      arrStr[i] = temp.join('') + arrStr[i][0] + 'ay';
    }
  }
  return arrStr.join(' ');
}
```

### Wednesday 26/01/2022. 
- Valid Parentheses   
```
function validParentheses(parens) {
  // your code here ..
  let arrTMP = [];
  for(let i = 0, l = parens.length; i < l; i++){
    let caracter = arrTMP[arrTMP.length - 1];
    if(parens[i] == '(') arrTMP.push(parens[i]);
    else if(caracter == '(' && parens[i] == ')') arrTMP.pop();
    else return false;
  }
  return arrTMP.length ? false : true;
}
```

- Convert string to camel case   
```
function toCamelCase(str){
 return str.split(/[-_]/).reduce((a,b)=> a += a ? b[0].toUpperCase() + b.substring(1) : b[0]);
}
```

- Unique In Order   
```
var uniqueInOrder=function(iterable){
  //your code here - remember iterable can be a string or an array
  iterable = Array.isArray(iterable) ? iterable.join('') : iterable;
  let arrTMP = [];
  while(iterable[0]){
    arrTMP.push(isNaN(iterable[0]) ? iterable[0] : +iterable[0]);
    iterable = iterable.replace(new RegExp('^['+iterable[0]+']+'),'');
  }
  return arrTMP;
}
```

### Thursday 27/01/2022. 
- Fold an array   
```
function foldArray(array, runs)
{
  let arrNew = array.slice();
  for(let i = 0; i < runs; i++){
    let middle = (arrNew.length % 2) ? Math.floor(arrNew.length / 2) : Math.ceil(arrNew.length / 2);
    for(let j = 0; j < middle; j++){
      console.log(arrNew[j],arrNew[arrNew.length-1-j]);
      arrNew[j] = arrNew[j] + arrNew[arrNew.length-1-j];
    }
    arrNew.splice(arrNew.length-middle);
  }
  return arrNew;
}
```

- Encrypt this!   
```
var encryptThis = function(text) {
  // Implement me! :)
  return text.split(' ').map((x) =>{
    if(x.length == 1) return x.charCodeAt(0);
    else if(x.length == 2) return x.replace(x[0],x.charCodeAt(0));
    else return x.charCodeAt(0) + x[x.length-1] + x.substring(2, x.length-1) + x[1];
  }).join(' ');
  
}
```

- Format a string of names like 'Bart, Lisa & Maggie'. (retired)   
```
function list(names){
  if(names.length == 0) return '';
  else if(names.length == 1) return names[0].name;
  else if(names.length == 2) return names.map(x => x.name).join(' & ');
  else return names.map((x,i) => {
    return (i < names.length-1) ? x.name: ' ';
  }).join(', ').replace(/[,\s]+$/,' ') + '& ' + names[names.length-1].name;
}
```



### Tuesday 01/02/2022. 
- Find the odd int  
```
function findOdd(A) {
  //happy coding!
  for(let i = 0, l = A.length; i < l; i++){
    let result = A.filter(x => x === A[i]);
    if(result.length % 2)return A[i];
  }
}
```

- Stop gninnipS My sdroW!  
```
function spinWords(string){
  //TODO Have fun :)
  return string.split(' ').map(x => x.length >= 5 ? [...x].reverse().join('') : x).join(' ');
}
```

### Wednesday 02/02/2022. 
- Array.diff  
```
function arrayDiff(a, b) {
  console.log('====');
  for(let i = 0, l = b.length; i < l; i++){
    if(a.includes(b[i])) a = a.filter(x => x != b[i]);
  }
  return a;
}
```

- Create Phone Number  
```
function createPhoneNumber(numbers){
  return "(" + numbers.splice(0,3).join('') + ") " + numbers.splice(0,3).join('') + "-" + numbers.splice(0,4).join('');
}
```

### Thursdat 03/02/2022. 
- Detect Pangram  
```
function isPangram(string){
  //...
  let result = new Set([...string.toLowerCase().replace(/[0-9.,\/#!$%\^&\*;:{}=\-_`~()\s]+/g,'')]);
  return result.size == 26 ? true : false;
}
```

- Find the missing letter  
```
function findMissingLetter(array)
{
  for(let i = 0, l = array.length; i < l; i++){
    let findWord = array[i].charCodeAt()+1;
    if(findWord != array[i+1].charCodeAt()) return String.fromCharCode(findWord);
  }
}
```

- Find the unique number  
```
function findUniq(arr) {
  // do magic
  return +arr.filter( (value) => { return arr.indexOf(value) == arr.lastIndexOf(value) } );
}
```

- Find the unique string  
```
function findUniq(arr) {
  // do magic
  let newArr = arr.map(a => {return [...new Set(a.toLowerCase())].sort().join('')}); 
  for(let i = 0; i < newArr.length; i++){ 
    if(newArr.indexOf(newArr[i]) == newArr.lastIndexOf(newArr[i])) return arr[i];
  }
}
```

- Find The Unique  
```
function findUniq(arr) { 
  console.log(arr);
  return arr.filter( (value) => { return arr.indexOf(value) == arr.lastIndexOf(value) } )[0];
}
```
