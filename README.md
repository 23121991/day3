# day3
ques:1.for the given json iterate (for loop,for in loop)
ans:
for loop:
var arr=[18,19,20,21,23,24,25,26];
for (var i=0;i<arr.length;i++){
if (arr[i]%2==0)
console.log(arr[i]);
}
for in loop:
var person = {
   name: "Nick",
  rname: "sravan",
   age: 26
}; 
for (let x in person) {
   console.log(x + ": "+ person[x])
}
ques:2.difference between windows screen and document?
ans:
Window is the main JavaScript object root, aka the global object in a browser, and it can also be treated as the root of the document object model. You can access it as window.

window.screen or just screen is a small information object about physical screen dimensions.

window.document or just document is the main object of the potentially visible (or better yet: rendered) document object model/DOM.

    window is the execution context and global object for that context's JavaScript
    document contains the DOM, initialized by parsing HTML
    screen describes the physical display's full screen
Briefly, with more detail below

    window is the execution context and global object for that context's JavaScript
    document contains the DOM, initialized by parsing HTML
    screen describes the physical display's full screen
window

Each browser tab has its own top-level window object. Each <iframe> (and deprecated <frame>) element has its own window object too, nested within a parent window. Each of these windows gets its own separate global object. window.window always refers to window, but window.parent and window.top might refer to enclosing windows, giving access to other execution contexts. In addition to document and screen described below, window properties include

    setTimeout() and setInterval() binding event handlers to a timer
    location giving the current URL
    history with methods back() and forward() giving the tab's mutable history
    navigator describing the browser software

document

Each window object has a document object to be rendered. These objects get confused in part because HTML elements are added to the global object when assigned a unique id. E.g., in the HTML snippet

<body>
  <p id="holyCow"> This is the first paragraph.</p>
</body>

the paragraph element can be referenced by any of the following:

    window.holyCow or window["holyCow"]
    document.getElementById("holyCow")
    document.querySelector("#holyCow")
    document.body.firstChild
    document.body.children[0]

screen

The window object also has a screen object with properties describing the physical display:

    screen properties width and height are the full screen

    screen properties availWidth and availHeight omit the toolbar

The portion of a screen displaying the rendered document is the viewport in JavaScript, which is potentially confusing because we call an application's portion of the screen a window when talking about interactions with the operating system. The getBoundingClientRect() method of any document element will return an object with top, left, bottom, and right properties describing the location of the element in the viewport.
ques:3.create a own resume in js on data format?
anes:<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Create your own resume data in JSON format
    </h1>
    <script src="script.js"></script>
</body>
</html>
var json = [{
    "id" : "raja1", 
    "msg"   : "For the given JSON iterate over all for loops (for, for in, for of, forEach)",
    "task" : "zen portal task",
    "mail": "rajarat6@gmail.com"
},
{
    "id" : "saravanan", 
    "msg"   : "For the given JSON iterate over all for loops (for, for in, for of, forEach)",
    "task" : "zen portal task",
    "mail": "rajarat6@gmail.com"
}];
//for loop
for(var i = 0; i < json.length; i++) {
    var obj = json[i];

    console.log(obj.id);
    console.log(obj.msg);
    console.log(obj.task);
    console.log(obj.mail);

}
//for Each
json.forEach(function(obj) { console.log(obj.msg); });

//for In
for (var key in json) {
if (json.hasOwnProperty(key)) {
  console.log(json[key].id);
  //console.log(json[key].msg);
 
}
}
//for Of
let text = "";
for (let x of json[key].id) {
 text += x; 
}
 console.log(text);



