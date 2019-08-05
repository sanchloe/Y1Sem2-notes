# ASP.NET Web Pages - Tutorial 
- uses Razor markup with C# or VB code
  - razor is a simple **markup syntax**
  
example :
``` html
<!DOCTYPE html>
<html>
<body>
     <h1>Hello Web Pages</h1> 
     <p>The time is @DateTime.Now</p>
</body>
</html>
```

- VB code blocks are enclosed in **@Code...End Code**
- inline expressions (variables or functions) start with @
- Variables are declared with the **Dim keyword**
- VB code is not code sensitive
- VB files have the extension *.vbhtml*

```VB
<!--single statement block-->
@Code 
dim myMessage = "Hello World"
End Code

<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block-->
@Code
dim greeting = "Welcome to our site!";
dim weekday = DateTime.Now.DayofWeek;
dim greetingmessage = greeting & "Here is Huston it is " & weekday
End Code

<p>The greeting is: @greetingmessage</p>
```

# Hiding Sensistive Information
- use underscores to prevent files from being browsed from the web.
-  _header.cshtml _footer.cshtml _Layout.cshtml
- _AppStart is to keep sensitive info
