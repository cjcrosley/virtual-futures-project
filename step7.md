# A Fractal Community
## Building a Flexibile Model for Urban Visioning
---

### Step Seven: Construct rooftop articulation
![](images/7-Rooftop articulation.PNG)
#### Summary
This step will calculate the number of stories for each room in the block that are needed to create the desired rooftop articulation. 

#### Inputs
- Block Rectangles 
- Block Fractal Step
- Room Center Points
- Floor to Floor Height
- Actual Floor Area Budget

### Generate Form
Any form could be generated here, however the one we have chosen has three inward sloping sides and one, north, upward sloping face. This form represents an articulation for rainwater collection and stack ventilation. 

This is accomplished with the four corner points of the center point of each block. We create four triangles by taking two adjacent corner points and a center point. Create a list of four sets of two adjacent corner points by shifting the list of corner points by one and matching it with the unshifted list. Then create three low center points and one high center points. Merge all lists together and use the Surf4Pt node. Join the resulting set of surfaces. 

### Calculate Number of Stories
Calculate the number of stories for each room by projecting the room center point to the created articulation surface. Then round the distance of the projected point to a factor of the Floor to Floor Height and divide by the Floor to Floor Height. The result is an integer that represents the number floors for each Room module in a Block.

### Calculate Remaining Floor Area Budget
