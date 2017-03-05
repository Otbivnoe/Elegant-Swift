<p align="center">
  <img src="logo.png" alt="Elegant swift"/>
</p>

### A list of elegant swift examples which highlight beauty and grace of swift language.
### Do you have elegant idea? Please, [contribute](https://github.com/Otbivnoe/Elegant-Swift/pulls)! :+1:


## :tada: Closure parameters omission magic: 

*Elegant*:

``` swift
struct Person {
    var name: String
}

let names = ["Carl", "Negan"]
let persons = names.map(Person.init)
```

*Not Elegant*:

``` swift 
struct Person {
    var name: String
}

let names = ["Carl", "Negan"]
let persons = names.map { name in
    return Person(name: name)
}
```

## :tada: `Get` omission: 

*Elegant*:

```swift
class User {
    var age: Int {
        return 20
    }
}
```

*Not Elegant*:

```swift
class User {
    var age: Int {
        get {
            return 20
        }
    }
}
```

## :tada: `Switch` typecast magic:

*Elegant*:

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

*Not Elegant*:

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

## :tada: KVC, KVO keypath: 

*Elegant*:

```swift
addObserver(self, forKeyPath: #keyPath(text), options: .new, context: nil)
```

*Not Elegant*:

```swift
addObserver(self, forKeyPath: "text", options: .new, context: nil)
```

## :tada: Trailing closure: 

*Elegant*:

```swift
UIView.animate(withDuration: 0.3) {
    view.frame = .zero
}
```

*Not Elegant*:

```swift
UIView.animate(withDuration: 0.3, animations: {
    view.frame = .zero
})
```

## :tada: Type omission: 

*Elegant*:

```swift
view.frame = .zero
view.backgroundColor = .red
```

*Not Elegant*:

```swift
view.frame = CGRect.zero
view.backgroundColor = UIColor.red
```
