<div align="center">

## Draw fractal star


</div>

### Description

Draw fractal star recursively using the algorithm in the book by Robert Sedgewick 'Algorithms in C++'
 
### More Info
 
change r to have a denser or lighter pattern . 2..5 okay

assume 800x600 screen res

Draws squares using lines 'b' style.

lower values of r increase the time to draw


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[oigres P](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/oigres-p.md)
**Level**          |Unknown
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Custom Controls/ Forms/  Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__1-4.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/oigres-p-draw-fractal-star__1-2837/archive/master.zip)





### Source Code

```
'From the book by Robert Sedgewick 'Algorithms in C++'
'It is a very useful book. Can you find a non recursive way of doing this?
'Recursion makes progs smaller and elegant whilst also making them
'more difficult to understand ( the implicit stack and unwinding of the calls)
Private Sub Form_Load()
Form1.WindowState = 2 'maximum
Form1.ScaleMode = 3 'pixel
Show
Call star(ScaleWidth \ 2, ScaleHeight \ 2, 90)
End Sub
Private Sub star(x As Integer, y As Integer, r As Integer)
If r > 1 Then
Call star(x - r, y + r, r \ 2)
Call star(x + r, y + r, r \ 2)
Call star(x - r, y - r, r \ 2)
Call star(x + r, y - r, r \ 2)
Call box(x, y, r)
End If
End Sub
Private Sub box(x1 As Integer, y1 As Integer, r1 As Integer)
Line (x1 - r1, y1 - r1)-(x1 + r1, y1 + r1), , B
'Form1.Circle (x1 - r1, y1 - r1), r1
'Line (x1 - r1, y1 - r1)-(x1 + r1, y1 - r1), , B
'Line -(x1 - (r1 \ 2), y1 + r1)
'Line -(x1 - r1, y1 - r1)
'trying to draw triangle instead of sqr- not work accurately
End Sub
```

