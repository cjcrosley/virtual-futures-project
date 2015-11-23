# A Fractal Community
## Building a Flexibile Model for Urban Visioning
---

### Step Five: Discard specific Rooms and Blocks

#### Summary
Until this point we have been manipulating data and tree structures in a fairly abstract way that is difficult to visualize. In this step we will discard the rooms in the urban grid that we are not interested in order to create a functional urban pattern.

#### Inputs
- Room Rectangles
- Room Center Plane
- Transit Curves
- Growth Boundary
- Total Steps - Room Exponent + Block Exponent + Community Exponent (use 9)
- Room X-axis Length
- Room Y-axis Length


### Block Boundary Rectangles
The previous step created the groups of rooms that represent individual blocks. Now, we will create boundary rectangles to represent those blocks. We calculate the fractal step of the block by finding the length of the branch path for each block (because each iteration of the fractal pattern creates an additional branch). Then use the formula outlined in step one to calculate the dimensions of the rectangle.

### Pathways
One set of rooms we would like to discard are the rooms along the boundary rectangles in order to create a street grid. Take two opposite corners of each room and test if those points fall on the boundary curve for that rooms block. Then, create a Boolean OR statement that will be True if either point touches the curve.

![](5-street grid.PNG)

### Internal Alleys
Next we will create internal alleys. This step will involve creating a diagonal internal pathway instead of creating four smaller blocks. 

![](5-internal alley.PNG)

### Arbitrary Pathways


![](5-transit paths.PNG)

### Courtyards


![](5-courtyard.PNG)

### Growth Boundary


![](5-growth boundary.PNG)

### Dispatch by NOR


![](5-urban pattern.PNG)