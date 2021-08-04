# Javascript Focus Event
Focus Event in JavaScript triggers when user focuses, i.e., clicks on an element. Using onfocus event handler, you can change element's style like change color, add shadow, etc. Similarly, you can show tooltips or alert boxes to give information about the input field.
## Example of onfocus form event
In the example below, when user focuses, i.e., clicks on the input field, its color changes to green from white. So, what really happens is that when user clicks on input field, the onfocus event gets trigerred. The onfocus handler takes the control and calls the user-definedhighlightInput() function. This function has the code to change the input field's color to green. Function executes and changes input field's color.
ExampleTry this code »


<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript Handling the Focus Event </title>

</head>

<body>

    <script>

        function highlightInput(elm){

            elm.style.background = "lightgreen";

        }    

    </script>

    <input type="text" onfocus="highlightInput(this)">

    <button type="button">Button</button>

</body>

</html>
Note: The value of this keyword inside an event handler refers to the element which has the handler on it. In the example above, it refers to the input field under focus.
## JavaScript Blur Event (onblur)
JavaScript Blur event is opposite of Focus event, it triggers when an element looses its focus. So, blur is a situation when an element gets unfocused after getting focused. The onblur event handler is used to handle this event.
Example of onblur form event
In the example of onblur event, an alert box gets displayed to inform the user that the input field has loses its focus. Notice that in this example the event handler is not calling any user-defined function. It is calling JS's in-built alert() function because we just want to give textual information to the user.

You are free to experiment with the code. Make your functions and try different styles.
ExampleTry this code »


<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnBlur Event </title>

</head>

<body>

 <input type="text" onblur="alert('Text input loses focus!')">

 <button type="button">Submit</button>


</body>

</html>
## JavaScript Change Event (onchange)
JavaScript Change event gets trigerred when user modifies the written or chosen value of a form element. For example: Changing input field's value, changing selection of dropdown list or, changing radio button selection. The onchange event handler is used to handle this event.
Example of onchange form event
In the example of onchange event, a selection list is created. When the user changes the default value of the selection list, the onchange event handler gets trigerred and calls the alert box, as defined in the code. The alert box confirms the selection.
ExampleTry this code »


<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnChange Event </title>

</head>

<body>

   <select onchange="alert('You have changed the selection!');">

    <option>Select</option>

    <option>OnePlus</option>

    <option>Samsung</option>

    </select>

  <p><strong>Note:</strong> Select any option in select box to see how it works.</p>

</body>

</html>
## JavaScript Submit Event (onsubmit)
JavaScript submit event occurs when user clicks on submit button to submit the form. Submit event is generally used to ask for confirmation from user to submit the form. The onsubmit event handler is used to handle this event.
Example of onsubmit form event
The example of onsubmit event also has an alert box popup. The onsubmit event handler gets trigerred when user clicks on the submit button. The alert box warn users that the information entered by them will be submitted to the online server. Try it out.

ExampleTry this code »


<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnSubmit Event </title>

</head>

<body>

  <form action="../index.php" method="post" onsubmit="alert('Form data will be submitted to 

  the server!');">

     <label>First Name:</label>

     <input type="text" name="first-name" required>

     <input type="submit" value="Submit">

  </form>

</body>

</html>
