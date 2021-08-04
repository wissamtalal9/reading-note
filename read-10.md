# JavaScript Debugging
Errors can (will) happen, every time you write some new computer code.

## Code Debugging
Programming code might contain syntax errors, or logical errors.

Many of these errors are difficult to diagnose.

Often, when programming code contains errors, nothing will happen. There are no error messages, and you will get no indications where to search for errors.

Searching for (and fixing) errors in programming code is called code debugging.

## JavaScript Debuggers
Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.

Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

## The console.log() Method
If your browser supports debugging, you can use console.log() to display JavaScript values in the debugger window:
Example
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>

<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>

</body>
</html>
Tip: Read more about the console.log() method in our JavaScript Console Reference.

## Setting Breakpoints
In the debugger window, you can set breakpoints in the JavaScript code.

At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.

After examining values, you can resume the execution of code (typically with a play button).

## The debugger Keyword
The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function.

This has the same function as setting a breakpoint in the debugger.

If no debugging is available, the debugger statement has no effect.

With the debugger turned on, this code will stop executing before it executes the third line.

Example
let x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;

## Major Browsers' Debugging Tools
Normally, you activate debugging in your browser with F12, and select "Console" in the debugger menu.

Otherwise follow these steps:
## Chrome
Open the browser.
From the menu, select "More tools".
From tools, choose "Developer tools".
Finally, select Console.

## Firefox
Open the browser.
From the menu, select "Web Developer".
Finally, select "Web Console".
## Edge
Open the browser.
From the menu, select "Developer Tools".
Finally, select "Console".
## Opera
Open the browser.
From the menu, select "Developer".
From "Developer", select "Developer tools".
Finally, select "Console".
## Safari
Go to Safari, Preferences, Advanced in the main menu.
Check "Enable Show Develop menu in menu bar".
When the new option "Develop" appears in the menu:
Choose "Show Error Console".
## Did You Know?
Debugging is the process of testing, finding, and reducing bugs (errors) in computer programs.
The first known computer bug was a real bug (an insect) stuck in the electronics.

## debugger
The debugger statement invokes any available debugging functionality, such as setting a breakpoint. If no debugging functionality is available, this statement has no effect.
## Syntax
debugger;
For Example
Using the debugger statement
The following example shows code where a debugger statement has been inserted, to invoke a debugger (if one exists) when the function is called.

function potentiallyBuggyCode() {
    debugger;
    // do potentially buggy stuff to examine, step through, etc.
}
When the debugger is invoked, execution is paused at the debugger statement. It is like a breakpoint in the script source.

# Manage exceptions with the debugger in Visual Studio
An exception is an indication of an error state that occurs while a program is being executed. You can tell the debugger which exceptions or sets of exceptions to break on, and at which point you want the debugger to break (that is, pause in the debugger). When the debugger breaks, it shows you where the exception was thrown. You can also add or delete exceptions. With a solution open in Visual Studio, use Debug > Windows > Exception Settings to open the Exception Settings window.

Provide handlers that respond to the most important exceptions. If you need to know how to add handlers for exceptions, see Fix bugs by writing better C# code. Also, learn how to configure the debugger to always break execution for some exceptions.

When an exception occurs, the debugger writes an exception message to the Output window. It may break execution in the following cases when:

An exception is thrown that isn't handled.
The debugger is configured to break execution before any handler is invoked.
You have set Just My Code, and the debugger is configured to break on any exception that isn't handled in user code.
## Tell the debugger to break when an exception is thrown
The debugger can break execution at the point where an exception is thrown, so you may examine the exception before a handler is invoked.

In the Exception Settings window (Debug > Windows > Exception Settings), expand the node for a category of exceptions, such as Common Language Runtime Exceptions. Then select the check box for a specific exception within that category, such as System.AccessViolationException. You can also select an entire category of exceptions.

