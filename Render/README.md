# F20GA CW1
The course work asked us students to comeup with a creative idea for a TV show, my idea is a tv show about random people playing massive chess pieces against each other, called "Chess Me". The hardest piece to create was the Knight, as with eyes, nose, mouth, ears, and a mane. Other pieces were easier to create as the complexity of pieces decreased.

## Objects and materials

### Pawn
Using the refrence image in the appendices, the basic shape of the pawn is created by creating a cylinder, scaling it to the base of the refrence, moving the top vertice to align with the base refrence, and then using extrude (to create the basic shape) or insets (to creatre indents) build towards the top. The sphere is creating used a few vertices using extrude, it is then filled with the "grid fill" function(f3), and selected using the more function, allowing us to select our rough sphere, we then use the "to sphere" function which allows us to turn the rough sphere shape into a perfect sphere. When there was not enough gemotry the cut loop tool is used to create the needed vertices, which are then adjusted. This is repeated until our pawn is completed.

![Pawn](https://i.imgur.com/SFrGWEl.png "Pawn")

### Knight

### Queen

### King

### Bishop

### Rock

### Chess board

### Grass and ground
Grass was creatred using the particle hair system, using the hair length to set the length of the grass. The brownian value was used to randomly change the direction of indivdiual grass, giving the glass a more realistic model. To make the grass be in "patches" of grass we use the childearn property, to control how patchy the grass is we can use three differen variables:the hair number variable, which controler how many grass and therefore groups and childearn of grass there are; change the group size of childearn directly using the render amount; or change the radius field in childearn, changing how close together indivdial grass are. To make grass have varying lengths we use the length variable of the childearn property. To texture the ground we apply a PBR texture taken from https://freepbr.com/materials/dry-dirt-pbr-material/ , this is done using a ground material and adding a image texture shader and applying it to the base colour of our ground material. For the grass we create a new material, Adding a variety of colours using a colour ramp from light green to dark green, we then lower the roughness to make the grass more reflective. As grass is translucent, translucent BSDF shader is added.

![Grass](https://i.imgur.com/cjQZ0hb.png "Grass")

## Lighting and compositions
## Render settings