### Summary
The popular 2048 game made for the TI graphing calculators. Something I made during a particularly boring day in class.

### Demo
![controls](http://38.media.tumblr.com/e85941ae3a92ab670ce086855bc2977b/tumblr_inline_nd0urpQMmJ1t2vup9.gif)

### Controls
![controls](http://i.gyazo.com/a2918b335567431566e919718c316acd.png)

### How it works
I use a matrix to represent the number grid. I have 4 methods, `xUp`, `xDown`, `xLeft`, `xRight`, which are called depending on which direction the user inputs. When called, the function adds the numbers from the grid into 4 lists (the function reads the matrix horizontally, if `xLeft`/`xRight`, or vertically, if `xUp`/`xDown`). `xMerge` is then called. This method accepts the 4 lists, and contains a nested for loop which properly adds up the numbers so as to simulate the “combining” effect from the original game. After `xMerge` is called, the original `x(Left/Right/Up/Down)` method continues on, and copies the list back into the matrix, which is then updated for the user to see.

