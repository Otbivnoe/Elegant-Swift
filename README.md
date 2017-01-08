<p align="center">
  <img src="logo.png" alt="Elegant swift"/>
</p>

### A list of elegant swift examples which highlight beauty and grace of swift language.
### Do you have elegant idea? Please, [contribute](https://github.com/Otbivnoe/Elegant-Swift/pulls)! :+1:


## :tada: Closure parameters omission magic: 

### Elegant:

``` swift
struct Person {
    var name: String
}

let names = ["Carl", "Negan"]
let persons = names.map(Person.init)
```

### Bad:

``` swift 
struct Person {
    var name: String
}

let names = ["Carl", "Negan"]
let persons = names.map { name in
    return Person(name: name)
}
```

## :tada: `Switch` typecast magic:

### Elegant:

``` swift
func anyIsInt(any: Int) {}
func anyIsString(any: String) {}

let any: Any = "Any variable"

switch any {
case let any as String: anyIsString(any: any)
case let any as Int:    anyIsInt(any: any)
default: break
}
```

### Bad:

``` swift 
func anyIsInt(any: Int) {}
func anyIsString(any: String) {}

let any: Any = "Any variable"

switch any {
case is String: anyIsString(any: any as! String)
case is Int:    anyIsInt(any: any as! Int)
default: break
}
```
