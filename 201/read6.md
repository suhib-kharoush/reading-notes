# object literals:
### creating an object:
- literal notation:
- literal notation is the easiest and most popular way to create objects.

### accesing an object and dot notation:
- you access properties or methods of an object using dot notation.
- you can also access properties using square brackets.

### creating an object:
- constructor notation:
- the new keyword and the object constructor create a blank object.

# document object model:
### caching dom queries:
- methods that find elements in the DOM tree.

### accessing elements:
- DOM queries may return one element, or they may return a Nodelist,
which is a collection of nodes. 

### get element by Id:
- Selects an individual element given the value of its i d attribute .
The HTML must have an id attribute in order for it to be selectable.

### query Selector(css selector):
- Uses CSS selector syntax that would select one or more elements .
This method returns only the first of the matching elements. 

### get elements by Class name:
- Selects one or more elements given the value of their cl ass attribute.
The HTML must have a cl ass attribute for it to be selectable.
This method is faster than querySe 1ectorA11 () . 

 - When a DOM method can return more than one element, it returns a
Nodelist (even if it only finds one matching element).

- If you add HTML to a page using i nnerHTML (or several jQuery methods),
you need to be aware of Cross-Site Scripting Attacks or XSS; otherwise,
an attacker could gain access to your users' accounts.
 

