# Codigo iOS Development Configuration and Coding Standards Guidelines

### How do we define or name the variables ? 

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

- You can declare many `protocol`s as you want in the .swift file. But make sure the functions and the properties that you declared inside the protocol is meaningful and associated with that `protocol`.

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
      
**6. Function Defination**

Functions are self-contained chunks of code that perform a specific task. You give a function a name that identifies what it does, and this name is used to “call” the function to perform its task when needed.

- Please start `func` name with lowercased letter

- If you want to name the `func` as task program

      func fetchData()
      func setUpView()
      
