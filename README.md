# Group-B User Input
#### Instructions
- __Geometric Generative Art as Inspiration__
  - Move the mouse slowly over the large circles
  - Press and release the mouse repeatedly and slowly on the screen or any large circle
  - Press 'a' and 'd' on the keyboard
  - Move around or press the mouse after clicking 'd'

#### Details of individual approach to animating the group code
- __TASK: User Input(Incorporate mouse or keyboard inputs for animation)__
  - When the mouse moves over the large circles, the radius will decrease, and when the mouse leaves, the radius will return to its original value.
  - When you press and release the mouse, the elements within the dotted-line circles will change sizes independently. There are two patterns: the yellow dots will shrink first, while the white dotted lines with rounded ends will expand first, creating a breathing effect.
  - when press ‘a’ on the keyboard, all of the large circles will change to black, emphasizing the elements within them. Enjoy the different atmosphere by moving the mouse around as the large circles turn black.
#### References of Inspiration
Through research, I identify artworks that align with my desired visual expression for the visual design of the group project, providing an impression reference for my sketches.


![alt text](Inspiration%201.jpg)
![alt text](Inspiration%202.jpg)
#### Technical explanation
  - By measuring the distance between the mouse cursor (mouseX, mouseY) and objects' position (x, y), I add a dynamic interaction for both the large circles and inner circles. Their radii can smoothly change when the mouse gets closer and smoothly return to original size as the mouse moves away, using the linear interpolation lerp(). 
  - By adding keyPressed() function to the large circles, they can change color by pressing 'a' and 'd' on the keyboard.
  - For the interaction of doted-line circles with linear interpolation (lerp()) to make a gradually transition, mouseIsPressed is true when the mouse is pressed, mouseIsPressed is false when the mouse is not pressed, which control the value of stroke weights, creating an interaction of stroke weight transition depending on the mouse state.
  - I draw the dotted circles by function drawDotsAroundCircle() for three of the large circles. Their locations are align with the location of the corresponding large circles by identifying circle.xScale and circle.yScale. To add mouse interaction, I set the dot size as dotSizeFactor that can be controlled in mousePressed() function.
  - I faced challenge that the code of ConcentricCircle and DotLayers from the group part didn't work when I work on individual task. As I couldn't find the solution that there may be some conflict between the code, I draw these two elements by myself in the individual part.