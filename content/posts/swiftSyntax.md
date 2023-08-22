+++
draft = false
date = 2023-08-21
title = "Swift Cheatsheet"
description = ""
tags = ["Swift","IOS development","OOP"]
+++

* [Basics](#basics)
* [OOP](#oop)

## Basics
1. Data Types
```swift
 let intVar : Int = 10
 let doubleVar : Double = 10.5
 let boolVar : Bool = true
 let stringVar : String = "Hello, World!"
 ```

 2. Conditional Statements
 ```swift
 if boolVar {
    print("It is True!")
 } else{
    print("It is False!")
    }
 ```

 3. Loops
 ```swift
    //for loops:
    for i in range 1...5 {
        print(i)
    }
    //while loops:
    i = 0
    while i < 5 {
        print(i)
        i += 1
    }
 ```

4. Use `let` for constants and `var` for variable (Using `let` is always a good idea)

5. Functions
```swift
    // like go, first comes with variable name,then comes after with data type
    func add(a Int,b Int) -> Int {
        return a + b;
    }
```

## OOP
1. Constructor or Initializer:
    ```swift
    class Car: Vehicle {
        var color: String

        init(wheels: Int,color: String) {
            self.color = color
            super.init(wheels: wheels)
        }

        convenience init() {
            self.init(wheels: 4, color: "Red")
        }
    }

    let myCar = car() // use convenience init
    ```

2. Protocols (similar to interface in Java)
    ```swift
    protocol Runnable {
        func run()
    }

    class Human: Runnable {
        func run() {
        print("Human runs on two legs")
        }
    }

    class Cheetah: Runnable {
        func run() {
        print("Cheetah runs very fast!")
        }
    }
    ```

3. Extensions 
   ```swift
   extension Int {
    var squared: Int {
        return self * self
        }
    }

   let fourSquared = 4.squared  // Outputs: 16
   ```