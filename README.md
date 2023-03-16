# Workshop-Blender

## How to install Blender
- Windows
- Linux

### Windows
The process is very simple :
Just go to [blender.org](www.blender.org/download/) and click `Download Blender`
(This workshop is intended on Blender 3.4.x)

### Linux
If you have snap :
`snap install blender --classic`
and execute it by typing `blender` in your terminal

If not :
Just go to [blender.org](www.blender.org/download/) and click `Download Blender`
(This workshop is intended on Blender 3.4.x)
Extract the zip folder and execute the `blender` file.


## First try
Is it your first time using Blender ? Look at this beautiful UI !
Now, first things first, try to move around the famous Default Cube that you see on your screen.
Remember our live modeling for that, use your mouse as we showed.
([Need a reminder ?](./pages/shortcuts.md))

## Serious business
No need to wait, we'll directly go deeper into Blender !
So, we want to make this beautiful cube, right ? The first part of the creation process is to setup references and / or to do the "blocking" part.

The blocking part is when you create the overall form of your objective with very simple meshs. You are just trying to match global proportions. Thus, when you will be creating your final more advanced mesh, you will have guidelines, and you will not wait until the end to discover that your proportions are messed up !

The references part is used when you are trying to recreate an existing object (this is the case here !). The goal is to add and align at least 3 images of the object you are trying to create : Top, Front, Side. Then, when you'll be doing your modeling, your goal will be to reproduce what you see, and it will be easier to align your mesh parts to match the wanted visual !
Since this is the perfect case, we'll begin with this ! Find in the [reference](./reference/) folder the reference image of the Companion Cube. Our case will be very easy as Side, Top and Front are the same, this is a perfectly symetrical cube ! Don't bother to add 3 reference image on the 3 main axis, just add one, align it with an axis, that's all you need.

##### Need help on the process ?
We will decompose it in smaller parts :
- Add an image ! We showed you how to add an object. An image is an object ! Summon the Add Object menu, and look for Image > Reference. (Download the image here : [reference](./reference/ReferenceFace.png))
- Align your image with an axis ! The easiest way is to reset its rotation with `ALT+R`.
- Now, move it on the good axis. ([Need a reminder ?](./pages/shortcuts.md)). It's better for the reference not to intersect the cube.
- Final step, scale your reference to match the cube ! For this, align your view to the good axis with the direction ball. Just click on the axis that you want.
  Now you should see something like the first image. Scale the image (and not the cube, the cube is PERFECT) to match the cube. Exactly like you can see on the second image.<br/>
<p align="right">
    <img src="./assets/axis.png" width="75">
</p>
  <p align="center">
    <img src="./assets/before_scale.png" width="300">
    <img src="./assets/after_scale.png" width="300">
  </p>

Tadaaam ! Great, you have your reference image !

## Let's start modeling !
The main structure of the Companion cube is indeed a cube, but we already have this one. We will now add more geometry to create the corners of our cube.

For this, start by creating a new cube ([Need a reminder ?](./pages/shortcuts.md)) and scale it down a little just to differenciate the two cubes.

Now we want to move this new cube to one corner of our main cube. We have more than one solution for this. All are pretty simple when you're used to them, but can be difficult at first, so let's do it one step at a time.

**Press N** : this will toogle a new menu that display useful data about the selected object. The first field is "Position". If you haven't edited your cube, it's position should be (0,0,0).
Note that you can also edit the data here, and knows what ? Our main cube (should) have a side of two metters ! (Our cube is exactly 2m\*2m\*2m tall). I'm not an math expert, but if we could move our cube 1m in all directions, it should be exactly on a corner of our main cube. GUESS WHAT ? YEAH WE CAN DO THAT. Just select every position field in this menu, and set it to 1. Tadaaaaaaaam, ahahah our cube is exactly where it should be !
Buuuut, I hear you asking, "what if", what if our main shape is not a cube, have not an easy dimension, and what if I can't move my cube just one metter in all axes... How can I do ?
Well, there is a very used method that you can learn [here](./pages/pointerMove.md). It's not on this main page because I wanted it to be pretty simple, but I strongly advise you to learn it, this is the real way to snap objects to a precise location in Blender.

So, now, let's match this new cube to the reference image. Snap your view to an axis, and use **G** and **S** to move and scale your li'l cube.

#### mettre image ici

Now, just don't forget that you moved you cube only on one axis, because of your point of view. Use the **N** menu (it's called the *Sidebar* by the way) to change the location of the missing axis.

## Modifiers
Their is at least three differents main tools of Blender that we will discover today. You have already discovered the main viewport, to add and move objects. We will now cover the Modifiers, and we will finish by the Edition mode.

### What are the Modifiers ?

Modifiers are like a set of littles programs that you can execute on your mesh.
Modifiers can be added and removed at anytime, this is their main strenght. They do not modify the real structure of your mesh, only the final one.
Let's start with an example, on the left you can see a sphere, and on the right you can see a sphere with the [Subdivision Surface Modifier](https://docs.blender.org/manual/en/latest/modeling/modifiers/generate/subdivision_surface.html). (I strongly advise you to check this page.)
![](./assets/subdivision_modifier.png)
As I said, the strenght of modifiers is that they are not definitive, this is called **non destructive modeling**. I can at all time change my mind and disable this modifier, and recover my low poly sphere.
Thanks to this, if I enter the edit mode (we will see this later on), I will see and edit the original (simple) shape of the sphere, and the modifier will be reexecuted after.
<p align="center">
    <img src="./assets/subdivision_modifier2.png" width="60%">
</p>

There is plenty of modifiers in Blender, you can check the doc [here](https://docs.blender.org/manual/en/latest/modeling/modifiers/index.html).
Today, we are going to use the [Mirro modifier](https://docs.blender.org/manual/en/latest/modeling/modifiers/generate/mirror.html). Because, as I said before, our cube is symetrical. So it corners are too.
Select the corner, then, on the right of your screen, locate the modifiers tab. ![](./assets/modifiers_tab.png)
<p align="center">
    <img src="./assets/modifiers_tab2.png" height="500">
    <img src="./assets/mirror_modifier.png" height="500">
</p>
Now, with the corner selected, click `Add Modifier` > `Mirror`

Oh, waw, no difference "before / after" ! Why ?!
Simply because the corner is a symetrical cube, and is mirrored onto itself. We need to change his mirror point. To do that, click the pipette icon and click on your main large cube to select it. Now you should see spawn another corner. But, we want 8 of them, not two, so we need to mirror them on all axis and not just one. You can do that by selecting all the buttons in the "Axis" field. (shift)

Great ! Now you should have something like this :
#### mettre image ici

## Edition mode
#### Introduction to the selection mode :
The edition mode is the heart of Blender, because, well, it enables you to edit meshs ! Select the corners of your Companion Cube, and press `TAB` to enter Edit Mode.
Now, you should see your cube differently. At each corner, you can see a point (called a vertex). Between them, you can see edges, and all of them create what's called a face.
You should already now the following if you listened to the live modeling, but if not, I'll explain it here quickly :
You need to master the differents selections modes to be productive in the edition mode. As I said, a mesh is composed by vertices, edges that connects vertices, and faces that are composed of edges. You can change your selection mode by clicking on 1,2 or 3 (NOT on the numpad). Or, by clicking on this menu on the top left : ![](./assets/selection_modes.png)
Selections modes are cross compatibles to the smaller ones, let me explain.
If you select a face in face mode, you can switch back to edge or vertex mode, because a face is the "largest" selection possible. On the other hand, if you select only one edge or one vertex, switching to face mode will discard your actual selection.
Know that `CTRL-Z` incudes the selection, so if you discard something at one point, you can `CTRL-Z` it back.

#### Let's do it
Edition mode enables you to shape your mesh the way you want with the help of a lot of tools. *If you want to test what I am going to say, why not create a new mesh and test edition mode on it ?*
The mains tools to work with are in fact tools that you already know : Move (**G**), Rotate (**R**) and Scale (**S**).
Another tool is the Extrusion Tool, that you can activate by selecting a face (in fact you can also do it with a vertex or an edge, but let's keep it simple), and pressing **E**. You will be able to make what's is called an extrusion (yeah tools are correctly named). Just click when you're finished and hop, new face ! We are not really going to use it today, but it's a monument too great to be missed.
The last one we are going to discover today is the Bevel tool.
Select an edge of your test mesh, and click **B**. Move your mouse and click when finished. Bam, flat bevel ! Want a round bevel ? `CTRL-Z` and do it another time, but this time scroll with your mouse wheel (slowly) to increase subdivisions.
Just after you made your bevel, notice the little menu at the bottom left of your screen. If you open it, you have a lot of options that will be very useful when we will want to make more complex bevels.

Now, follow this video give a real shape to the corners of your cube.

![](./assets/bevel_cube_edges.mp4)
