# A brain Frick interpreter
...


# How does it work & how did I make it?
We will start with the basics
there is a textarea for the brainfrick code input I assigned it a class and id like so
<textarea class="inputs"; id="BFinput">
the class I dont use in the project currently but id I do use.
Next is the style I set position to absolute then I used top, left, height, width styles to all change where and how big it is.
I set resize to none in styles aswell this prevents it from being resized, I also set border to 0 else it has a weird looking border.
other then that I set colours in style, then placeholder outside of styles.

In the <script>
part of the code it starts by defining all the functions,
the part
```  
window.addEventListener("DOMContentLoaded", () => {
  const btn = document.getElementById("StopRun");
  if (btn) {
    btn.addEventListener("click", StopRunning);
  }
  });

  function StopRunning(){
    Running = false
  }
  ```
  is to set up for the stop button

  ```
  function wait(ms) { 
    return new Promise(resolve => setTimeout(resolve,ms));
  }
```
is for setting up the delay for the tick speed input.

then main code starts, start run first thing we do is set running to true so we know its running,
then we reset all cells (16) to value 0 and to be the correct colour
after we make most the variables me need
code & delay are just directly from the inputs so code will be the code you entered, delay will be the tickspeed/delay you entered
Currentcell is the cell the highlighted cell when you click start
old cell is the cell it was before you did < or >,
Cinval is kinda like how [i] is used to track the run loops but its to track what input your on, ea it starts at 0 which is the first one, if you do "," in the code it goes to 1 so it knows what input your on.
Cinput is the input but its also help to see how long the input text is.

then we set the first cell's colour to change so we know which cell the current cell is
then we set the BFouput to "" (this just makes it empty/cleared from last run)


# processing the BF
Coming into this project I didnt really know much about what to do but it ended up working by the end.

## +
