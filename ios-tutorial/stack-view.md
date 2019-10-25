---
PermaID: 10020020
---

# Create Flexible Layouts with Stack Views

## Stack Views

Stack views let you leverage the power of Auto Layout, creating user interfaces that can dynamically adapt to the device's orientation, screen size, and any changes in the available space. 

 - A stack view takes two or more view objects and then stacks them either horizontally or vertically. 
 - The stack view manages the layout of all the views in its arranged Subviews property. 

### Adding Stack Views

So, let's create a new Single View App and call it **StackLayoutDemo** and add four labels on each corner.

<img src="images/stacklayout1.png">

Previously, we fixed this problem using Auto Layout constraints, so now we will fix it with stack views. Now first we want to take the top two controls across the top and put them in a stack view. Select the Top Left and Top Right labels.

<img src="images/stacklayout2.png">

Choose Editor > Embed In > Stack View menu option. Now you can see in the Document Outline that the top two labels are now inside a stack view, but both labels are next to each other. 

We want this stack view to span the available width of whatever device and whatever orientation we are running on, and this is where setting up Auto Layout constraints is still essential.

<img src="images/stacklayout3.png">

The best option for adding constraints for a stack view is using the Add New Constraints option at the bottom of the storyboard which is highlighted in above image.
 
<img src="images/stacklayout4.png">

Let's add manual constraints by clicking the red dotted line to the top, left and right, which is going to connect it to the Safe Area, 16 points from the left, and 16 points from the right.

<img src="images/stacklayout5.png">

Click Add 3 Constraint button, and now they don't seem to be laid out very attractively, and that's to do with the distribution that's happening within this stack view. Go to the Attributes Inspector. 

<img src="images/stacklayout6.png">

In the Distribution drop-down, select Equal Spacing. Now repeat the same steps for bottom labels as well by adding manual constraints.

<img src="images/stacklayout7.png">

Again in Attributes Inspector, select the Equal Spacing option in Distribution dropdown list. If you change to landscape mode, we have a more available width, so the stack views expand, and the views inside them are distributed out, and it just works.

<img src="images/stacklayout8.png">

Similarly, if you change the view to iPad Pro, you will see the same view.

<img src="images/stacklayout9.png">
