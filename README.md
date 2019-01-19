### stackman
---
https://github.com/watson/stackman

```
npm indtall stackman
```

```js
var stackman = require('stackman')()
var err = new Error('Opps!')
stackman.callssites(err, function(err, callsites){
  if(err) throw err
  callsites.forEach(function(callsite){
    console.log('Error occured in at %s line %d',
      callsite.getFileName(),
      callsite.getLineNumber())
  })
})

stackman.callsites(err, function() {})
console.log(err.stack)
```

```
```


