# Codigo iOS Development Configuration and Coding Standards Guidelines

### Rules for Objects, Variables, Protocol, Functions declaration and naming? 

**1. Variables Defination (`let` and `var`)**

- Please name the variable and constant as simple as possible and make it easy to understand. And please use `_`,`-`,`&`,`$` as **low** as possible.

- All the variables first word should start with lowercased. And the next further words can start with capitalized.

      var thisIsNewVariable = 123456

- Dont use `_`**(underscore)** on start of the variable naming.


**2. Flag Defination**

- Flags variable should start with `is`, `has` and verbs such as `needs`, `starts`.  

      var isPresented: Bool?
      var hasStarted: Bool?
      var needsToReloadImmediately: Bool?
      var startRequestImmediately: Bool?

- Flags are also the main part of the business logic in development. So, make sure you name it **meaningful** to each appropriate task you want to control.
      

**3. Object Defination**

- Please end with `Data` for object representation of your stored data object.
```
var newsData = NewsData()
var testData = VisitData()
var degreesData = DegreesData()
var teamData = TeamData()
```

**4. Protocol Defination**

A `protocol` defines a blueprint of methods, properties, and other requirements that suit a particular task or piece of functionality.

- You can declare many `protocol`s as you want in the .swift file. But make sure the functions and the properties that you declared inside the protocol is **meaningful** and associated with that `protocol`.

- Start `protocol` name with uppercased letter.
```
      protocol ReusableView: class {
            static var defaultReuseIdentifier: String { get }
      }
```

**5. Class and Struct Defination**

- `class` and `struct` name should be started with uppercased letter same as `protocol`.

      class MyReusableDemoVC: UIViewController {}
      class Car {}
      struct Car {}
      
**6. Function Defination **

Functions are self-contained chunks of code that perform a specific task. You give a function a name that identifies what it does, and this name is used to “call” the function to perform its task when needed.

- Please start the function name with lowercased letter

- If you want to name the `func` as task program, you can start the function name with **Verbs**
```
      func fetchData()
      func setUpView()
```

- If you want to name the `func` as check program, you can start the function name with `is`, `did`
```   
      func isSubscribe()
      func isFetchCompleted()
      func isValidationSuccess()
```      

- Don't pass `parameters` to the function unless it was used. Make sure you name the `parameters` **meaningful** because `parameters` which used inside the function are really important to be understand by the developers who is passing and debugging those.


- If the `parameter` names that you declared are need to know for those who is going to access that function, don't use `_(underscore)` in front of that `parameter`. So, they will know at least which things to pass when they call that function.
```
      func checkSubscription(_ hexStringGeneratedByApple: String,_ productName: String) // This is WRONG
      func checkSubscription(hexStringGeneratedByApple: String, productName: String) // This is CORRECT
```

- If you are declaring the function which required a lots of parameters and going to use it everywhere, **DON'T CREATE `parameters`!**. Use object parameter instead of declaring single parameter.

- Don't declare **Acccess Control** in front of the function name unless it was needed. **Access Controls** are required only when you want to control that function on the class which was extended on many class files. 

      https://docs.swift.org/swift-book/LanguageGuide/AccessControl.html
      
- 





      
