# F20GA CW1
The course work asked us students to comeup with a creative idea for a TV show, my idea is a tv show about random people playing massive chess pieces against each other, called "Chess Me". The hardest piece to create was the Knight, as with eyes, nose, mouth, ears, and a mane. Other pieces were easier to create as the complexity of pieces decreased.

## Objects and materials

### Chess board
The shape of the chessboard is created simiarly to the pawn, the texture is procedurally generated.
To make the checkers colours we add a checker texture to the material, with the scale of 8 (chess board is 8x8).
To create the wood effect we use a musgrave texture with a noise texture to simulate a grain, the scale and detail are changed to change the shape of the grain.
To make the checkers two different colours we flag two colour ramps to the noise texture, one lightly colourd wood colour, and the other one is a dark colourd wood.
To assign the top of the board this material we select the top face, add the wood-checker material we created and assign it to our selection. The rest of the board is a basic material, with only the roughness changed to make it less reflective.

![Board](https://i.imgur.com/PrN8bZD.png "Board")

### Grass and ground
Grass was creatred using the particle hair system, using the hair length to set the length of the grass. The brownian value was used to randomly change the direction of indivdiual grass, giving the glass a more realistic model. To make the grass be in "patches" of grass we use the childearn property, to control how patchy the grass is we can use three differen variables:the hair number variable, which controler how many grass and therefore groups and childearn of grass there are; change the group size of childearn directly using the render amount; or change the radius field in childearn, changing how close together indivdial grass are. To make grass have varying lengths we use the length variable of the childearn property. To texture the ground we apply a PBR texture taken from https://freepbr.com/materials/dry-dirt-pbr-material/ , this is done using a ground material and adding a image texture shader and applying it to the base colour of our ground material. For the grass we create a new material, Adding a variety of colours using a colour ramp from light green to dark green, we then lower the roughness to make the grass more reflective. As grass is translucent, translucent BSDF shader is added.

![Grass](https://i.imgur.com/cjQZ0hb.png "Grass")

### Chess piece material
It's a simple material aimed to look like a high quality marble-glass chess set. This is achived by lowring the roughness, making the pieces more refelective, transmission is used to controller how opaque the material is. Giving us the marble-glass materail we want.

### Pawn
Using the refrence image in the appendices, the basic shape of the pawn is created by creating a cylinder, scaling it to the base of the refrence, moving the top vertice to align with the base refrence, and then using extrude (to create the basic shape) or insets (to creatre indents) build towards the top. The sphere is creating used a few vertices using extrude, it is then filled with the "grid fill" function(f3), and selected using the more function, allowing us to select our rough sphere, we then use the "to sphere" function which allows us to turn the rough sphere shape into a perfect sphere. When there was not enough gemotry the cut loop tool is used to create the needed vertices, which are then adjusted. This is repeated until our pawn is completed.

![Pawn](https://i.imgur.com/SFrGWEl.png "Pawn")

### Knight
By far the hardest model in this project, taking roughly 4 days to create, this is as this is the most complex piece in the scene.
To create the general shape of the knight, we try to use the same method as the pawn, but with rotation of vertices. this results in a poor general shape.
![Bad horse](https://i.imgur.com/HDX8VHR.png "Bad horse")
It was then redone with the general shape of the horse, the onlt rotation used was for the neck. To have different width front and back vertices are creatred using extrude or insets, and moved on the correct access to move them towards the front.

![Better horse](https://i.imgur.com/Fl00eh5.png "Better horse")

We then adjust vertices to match the general shape more closely with the reference.
The mouth is creatred by deleting the vertices matching the area of the mouth in the reference, those vertices are then joined by creating a loop bridge.

![Horse with a mouth](https://i.imgur.com/E5pyzrC.png "horse with a mouth")

Then the mane of the hourse is creatred by selecting all center faces on the back of the horse that are on the same area as the mane in the refrence.
Then the mane is creatred by extruding along the normals of the selected faces. The mouth verices are also slightly adjusted to match closer with the ref.

![Mane](https://i.imgur.com/HQLmNQj.png "Mane")

The nose and ears are also created by extruding among normals, the ears gets adjusted by scaling moving the top vertices towards the front.

![Ears nose](https://i.imgur.com/9sGsOfh.png "Ears and nose")

We adjust the nose shape by moving the vertices of the nose to make a more circler-nose shaped nose, the general face is more defines by adding more cut loops and resizing them. The eye are creatred by subdivisioning the faces of the eye, and then cutting and bridging to make them more ovel shaped.

![eyes](https://i.imgur.com/aLKWdY3.png "eyes")

We then create an inner flat sphere to create the eyes (using the methods used in the pawn), giving us our final version of the knight.

![horse](https://i.imgur.com/MSqUFut.png "horse")

### Queen
The queen main body is creatred the same way the pawn is. The crown is creatred by creating a different circle, extruding along its normals, and moving parts of it to the bottom using checker deselect. It is then joined with the main body to creatre the queen.

### King
Created the same way as the pawn, for the cross the top we extrude along the sides and bevel to give it a nicer look.

### Bishop
Creatred the same way as the pawn.

### Rock
The rock is created by combining the methods from the knight and chess board. The cut is created using check deselect, giving us a rock shaped head.

## Lighting and compositions
As the scene is outside a sun is added to the top, with putting it more towards the black side to simulate around noon time.

## Render settings
The camera view is adjusted using "camera to view", we then adjust the camera view to include all of our object in the scene.
The scene was rendered using "cycles" with 4096 samples.