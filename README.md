# Programming Notes
As I learn more about Javascript and web programming, I'd like to keep an archive of takeaways, tips & tricks, and any other interesting information that I pick up through developing projects, working through tutorials, and reading articles and documentation.

## Table of contents
- [CSS](#css)
- [HTML](#html)
- [JavaScript](#javascript)
- [Visual Studio Code](#visual-studio-code)


## CSS
---
- Reset default browser styles, the asterisk is the `universal selector` and since it's the highest selector, its styles are applied to all elements
```
* { 
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
- Apply common styles to multiple elements
```
.class1, .class2, .class3{
    ... styles ...
}
```
- Apply style to an item within an element
```
.container svg {
 
}
```
- **still looking into this one..** Relative and absolute positioning : set the parent element to `display: relative` then declare the child's `display: absolute`, so then you have the freedom to position the element as you'd like (initially will just position the child elem in direct center w/out modifying top/bottom/left, etc.) 
```
.player-container{
    position: relative;
}

.player-container svg {
    position: absolute;
    height: 50%;
    top: 50%;
    left: 50%;
}
```
- How to make buttons look **clickable**
```
button {
    cursor: pointer;
}
```
- How to get the perfect `border radius`, set the height and width of element to same dimensions
```
.sound-picker button{
    border: none;
    height: 120px;
    width: 120px;
    border-radius: 50%;
    padding: 30px;
}
```
- How to create hover effects e.g. `button hovering`
```
.time-select button {
    color: white;
    background: none;
    /* transition is applied to the hover */
    transition: all 0.5s ease;
}

.time-select button:hover{
    color: black;
    background: white;
}
```
- `nth-child` call selects the nth child element of the parent (according to what value of n is passed in) and type does not matter. The e.g. below shows how to select the 1st and 2nd button of a class and style them. This selector seems advantageous when you want to style a certain set of elements w/in its parent but they dont have ids and you need to fetch them individually
```
/* retrieve the 1st button */
.sound-picker button:nth-child(1){
    background: #497281;
}

/* retrieve the 2nd button */
.sound-picker button:nth-child(2){
    background: #a14f49;
}
```
- How to fix an `img` to fit perfectly in center of an element e.g. button by setting height to 100 %
```
button img{
    height: 100%;
}
```
## HTML
---
- `data-* attributes` : custom data attribute that can be applied to HTML elements, this is useful when I need a custom attribute e.g. data-time, data-sound, that I want to manipulate in JS


## JavaScript
---
- Use `querySelector` to select an element from the DOM. And `querySelectorAll` to select an array of multiple elements
```
const song = document.querySelector('.song');
const timeSelect = document.querySelectorAll('.time-select button');
```
- Brower's Developer Tools shortcut <kbd>F12</kbd>
- Using `forEach` on an `array` to pass in a `eventListener`:
```
    sounds.forEach(sound => {
        sound.addEventListener('click', function(){
            ... do stuff ...
        });
    });
```
- `arrow function` - have no names and can be used for quickly defining functions
```
    play.addEventListener('click', () =>{ // no arg arrow function
        .. do stuff .. 

    });
```
- Immediately invoke a function - this function is invoked as soon as your script starts up
```
const app = () =>{

};

app();
```
## Visual Studio Code
---
### Shortcuts
- Generate boilerplate HTML code : hold <kbd>Shift</kbd>+<kbd>1</kbd> and press <kbd>Tab</kbd>
- Div shortcut generator : type `.className` and press <kbd>Tab</kbd>

