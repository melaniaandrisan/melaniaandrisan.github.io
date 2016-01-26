---

published: true
layout: post
date: "2016-01-15 23:30:10 +0200"
categories: Jekyll
title: "Swift - Reading in trying - The Swift programming language book"

---

Looking at Swift after so many months of "no programming" is very cool because is a very easy language to learn and without so many restrictions.

The usual formats from C and c# are almost the same, but you need to be careful at indentation.

`x=1+1` in not the same with `x = 1 + 1` the first will give you an error and the second one will work.

Some other things that I noticed:
* there is no `;` at the end of a line
* variables can be declared with explicit type but is not necessary `var` is enough.  
* "This is a variable in a String\(variable)"   
* The `if..else`, `for`, `while` `repeat..while` work as usual just that `if` will evaluate just a bool expression.  
* `for i in 0..<10` is the same with `for var i = 0; i < 4; ++i`   

  < Use `..<` to make a range that omits its upper value, and use `...` to make a range that includes both values.”


* use `func` to declare a function
`func greet(name: String, day: String) -> String`

A very comprehensive list of Swift functions functionality can be found on [objc.io](https://www.objc.io/issues/16-swift/swift-functions/)
