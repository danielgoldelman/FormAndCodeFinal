# Basics

So, you want to look at how some basic shapes work in this program? Very interesting! Maybe you didn't want to actually experiment yourself (although I would highly recommend it, it's pretty fun), or maybe you wanted to see some examples of how this stuff works, or maybe you are on a computer that is Rhino-less. Any way you got here, welcome!

In each directory within `Basics`, you will see how one basic shape was put into the tool and what various outputs were generated. In the interest of making everything a bit more streamlined, the same procedural steps were used in the generation of every shape produced by the tool and put into this repository.

In each folder, you will see two files: a .3dm Rhino file containing the generated curves, and a .ai Adobe Illustrator file that displays the outputs in a straightforward format. 

Here was the procedure:

<table border="3">
<tr>
    <td>1000 pts, 1 mult</td>
    <td>1000 pts, 5 mult</td>
    <td>1000 pts, 10 mult</td>
    <td>500 pts, 5 mult, 3 runs</td>
<tr>
<tr>
    <td>100 pts, 5 mult</td>
    <td>400 pts, 5 mult</td>
    <td>700 pts, 5 mult</td>
    <td>500 pts, 10 mult, 3 runs</td>
<tr>
</table>

So let's explain a few things:

- _ pts = # of points that the original shape was divided into
- _ mult = the multiplication of the distance between neighbors
- _ runs = the number of times the mult slider was run from 0-10 and back before finally getting to the mult number. See `Symbol Animation` for a longer explanation of why this matters.