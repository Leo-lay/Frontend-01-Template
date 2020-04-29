### convertStringToNumber
```
function convertStringToNumber(str, hex = 10) {
    if(hex < 2 || hex > 16) return NaN
    var chars = str.split('');
    var number = 0;
    var i = 0;
    while(i < chars.length && chars[i] !='.') {
        number = number * hex;
        number += chars[i].codePointAt(0) - '0'.codePointAt(0);
        i++;
    }
    if (chars[i] == '.') { i++; }
    var fraction = 1;
    while(i < chars.length) { 
        fraction = fraction / hex;
        number += (chars[i].codePointAt(0) - '0'.codePointAt(0)) * fraction;
        i++;
    }
    return number ;
}
```
### convertNumberToString
```
var radix='0123456789abcdef'
function convertNumberToString(number, hex = 10) {
    if(isNaN(number) || hex < 2 || hex > 16) return NaN;
    var integer = Math.floor(number)
    var fraction = number - integer;
    var str = ''
    while(integer > 0) {
        str = radix[integer % hex] + str;
        integer = Math.floor(integer / hex);
    }
    if (fraction === 0) return str;
    str += '.'
    while(fraction > 0) {
        fraction *= hex;
        str += radix[Math.floor(fraction)]
        fraction = fraction - Math.floor(fraction)
    }
    return str;
}

```
### 根据课上老师的示范，找出 JavaScript 标准里所有的对象，分析有哪些对象是我们无法实现出来的，这些对象都有哪些特性？写一篇文章，放在学习总结里。
- 全局对象
- 
