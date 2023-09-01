## ❤️ Variable Scopes

➔  [var/let/const-global and local scope](https://chat.openai.com/share/640ec4bd-763a-4967-878b-0ca8bf65e0c9)

## 🧡 Variable shadowing

➔ [var/let/const-shadowing](https://chat.openai.com/share/640ec4bd-763a-4967-878b-0ca8bf65e0c9)  <br/>
➔ var variable creates global memory allocation box <br/>
➔ let and const creates seperate memory allocation box for **specific scope global and local**

```
function test(){
    var a = "aaaa";
    let b = "bbbb";
    const c = "cccc";
    
    if(true)
    {
        var a = "new aaaa";
        let b = "new bbbb";
        const c = "new cccc";
        
        console.log(a); //new aaaa
        console.log(b); //new bbbb
        console.log(c); //new cccc
    }
    
    console.log(a); //⚡new aaaa
    console.log(b); //bbbb
    console.log(c); //cccc
    
}
test();
console.log(a,b,c); //ERROR - out of scope

```

## 💛 illegal shadowing
➔ declaring in same scope
```
var a;
var a; // can be declared in *same scope*

let b;
let b; // error

const c;
const c; // error
```
➔ illegal shadow
```
var a = "hello";
let b = "bye";
const c = "kem cho";

function test(){
  let a = "hiii";      // ✔️ var can be shadowed by let so var > let
  var b = "goodbye";   // ❌ ERROR = var > let so let cannot be shadowed by var
}
```
