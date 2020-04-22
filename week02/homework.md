### 写一个正则表达式 匹配所有 Number 直接量
```
const numberReg = /^((0)|(\.\d+)|([1-9]+)|([1-9]*\.\d+)|(0[xX][0-9a-fA-F]+)|(0[bB][0-1]+)|(0(o|O)[0-7]+)$/
```

### 写一个 UTF-8 Encoding 的函数
```
function UTF8Encoding(str) {
    if(!str) return
    return str.splite('').reduce(s => { return `\\u${s.charCodeAt().toString(16)}`})
}
```

### 写一个正则表达式，匹配所有的字符串直接量，单引号和双引号
```
看了winter大佬的正则感觉有点变态 不写了！！！！
```