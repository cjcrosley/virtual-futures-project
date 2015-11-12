# A Fractal Community
## Building a Flexibile Model for Urban Visioning
---

### Step One: Create dimensional module and fractal steps

![](images/step1 final.png)

#### Summary
This step will define the locations and rotations of the communities in the model. It will also determine the size and extent of the underlying fractal grid that will be used to construct the communities. 

####Inputs (Blue Groups)
- **Transit Paths** - A curve or list of curves representing the transit network connecting all communities in the model.
 - We will not use the Transit Paths in this step, but we set them now for convenience. They will be used in step three. 
- **Boolean Toggle** - Use the Primary Rotation supplied below if set to True. If False, a random rotation will be supplied. 
- **Primary Rotation** - A list of numbers representing degrees of rotation corresponding to each of the communities in the model. 
- **Community Centers** - A list of points representing the center point of each community.
- **Cell Prime X** - The base modular dimension of the x-axis.
- **Cell Prime Y)** - The base modular dimension of the y-axis.
- **Base** - The base number for the fractal doubling.
- **Room Exponent** - The exponent used to calculate the Room size from the Cell size.
- **Block Exponent** - The exponent used to calculate the Block size from the Room size.
- **Community Exponent** - The exponent used to calculate the Community size from the Block size.

#### A Primer on Fractals

>"A fractal is a natural phenomenon or a mathematical set that exhibits a repeating pattern that displays at every scale. It is also known as expanding symmetry or evolving symmetry" [^1]

To examples of fractals that relate well to what we're doing here are the [Seirpinski Carpet](https://en.wikipedia.org/wiki/Sierpinski_carpet) and the [Apollonian Gasket](https://en.wikipedia.org/wiki/Apollonian_gasket).

![](images/fractals.png)

The Seirpinsky Square is constructed by subdividing a square into a grid of 9, discarding the center, and repeating the pattern to the remaining squares in the grid. In this way, the pattern can repeat infinitely and is present at every scale. 

#### The Fractal Grid

In this project we will use a similar principle to construct our fractal grid and, consequently, the urban grid. 

We will start by defining a cubic module or cell that will serve as the "prime factor" [^2] of dimensions in the project. While, these dimensions do not need to be prime numbers for the model to work, it is useful to think of them as prime numbers conceptually. You could also compare this module to a cell, a pixel, an atom, or a grain of sand. It is the smallest unit. 

The Cell is defined by is X, Y, and Z-axis in feet. These variables are called Cell Prime X, Cell Prime Y, and Cell Prime Z, see inputs above. We will use X=3, Y=2, and Z=1. 

The Base variable represents the number of times the Cell will be duplicated or divided in each iteration of the pattern.  

The Room, Block, and Community Exponent variables indicate the number of iterations the pattern will go through in order to define a Room, Block, or Community.

$$
Number\ of\ Prime\ Cells = Base ^ {Exponent}
$$

To find an X-axis or Y-axis dimension the Cell Prime value is multiplied the total number of repetitions: 
$$
Width = Cell\ Prime \times Base ^ {Exponent}
$$



###Citations:

[^1] [ Wikipedia, Fractal.](https://en.wikipedia.org/wiki/Fractal)

[^2] [Prime Factorization](http://www.mathsisfun.com/prime-factorization.html)
