# generate-cpf
Code JS to generate fake CPF Brazil

Link: https://toolzinho.com/tool/generate-cpf

```js
generate(punctuation) {
    let n = 9
    let n1 = random(n)
    let n2 = random(n)
    let n3 = random(n)
    let n4 = random(n)
    let n5 = random(n)
    let n6 = random(n)
    let n7 = random(n)
    let n8 = random(n)
    let n9 = random(n)
    let d1 = n9*2+n8*3+n7*4+n6*5+n5*6+n4*7+n3*8+n2*9+n1*10
    d1 = 11 - ( mod(d1,11) )
    if (d1>=10) d1 = 0
    let d2 = d1*2+n9*3+n8*4+n7*5+n6*6+n5*7+n4*8+n3*9+n2*10+n1*11
    d2 = 11 - ( mod(d2,11) )
    if (d2>=10) d2 = 0
    let ret = ''
    if (punctuation) ret = ''+n1+n2+n3+'.'+n4+n5+n6+'.'+n7+n8+n9+'-'+d1+d2
    else ret = ''+n1+n2+n3+n4+n5+n6+n7+n8+n9+d1+d2
    
    return ret
  }
  random(n) {
    return Math.round(Math.random()*n)
  }

  mod(dividend,divider) {
    return Math.round(dividend - (Math.floor(dividend /divider)*divider));
  }
``` 
