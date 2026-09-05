# A brain Frick interpreter
The project is a simple brainfrick interpreter, it includes an coding input where you input code, a regular imput used with "," and an output which outputs the cell's value in according to ascii (technically according to utff-8 I think), it also includes 16 cells to visualise the process and a tick speed input (how fast every symbol is executed).

Brain *Frick is a popular eso-lang which is fairly simplistic with a total of 8 symbols.

It executes the code by looping through every character and just a bunch of if statements.
using the symbol ">" will go to the next cell (Left>Right & Top>Bottom, like reading a book) if the current cell is the last one (16) it will go back to the first cell (1).
using the symbol "<" will go to the cell before if the current cell is the first one (1) it will go to the last cell (16).
"+" & "-" are pretty simple, + will add 1 to the cell value (if its 255 it will set the cell value to 0), - will subtract one from cell value (if was 0 it will make it 255).
"," is used to take the next input in the input thing and set the cells value to the ascii character value.
"." outputs the cells value into the output text box, so if the cells value was 120 it would output "x".

"[" and "]" are a bit more confusing & hard to explain so I'll explain with an example of how they are used
if the code was like
+++++[>++<-]
it will make the first cell's value 5, then start the loop with "[", go to the next cell (2), add two to the cell, go back to the first cell (cell 1, which has the value of 5), then subtract one from it (cell 1 = 4 now) then it will repeat the loop of ">++<-" (or next cell +2, back a cell, subtract one) until the first cell (cell 1) has the value of 0
the finishing result of the example code "+++++[>++<-]" will leave cell one as the current cell (highlighted one), cell 2 will have the value of 10 and all other cells will have the value of 0

"[" shows the code were the start of the loop is then "]" shows where the end of the loop is.

After a loop you can just continue with whatever brainfrick code you want So if you wanted to make it output two you could do:
++++++++++[>+++++<-]>.
(sets first cell to 10, then adds 5 every loop so cell 2 = 50 then goes to cell two and outputs)

This project was kinda just made for fun as a first proper website and interpreter, It ended up being quite less complicated then I was execting tbh.

(also side note, the green button that says "Run Code" will start the code and the pink button saying "STOP CODE!" will stop executing the code, to restart the execution of the code just click run again.)



*its not actually brainfrick but I rather call it Brain Frick then brain fuck
