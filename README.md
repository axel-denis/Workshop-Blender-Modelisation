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
Since this is the perfect case, we'll begin with this ! Find in the [reference](./reference/) folder the reference image of the Companion Cube. Our case will be very easy, Side, Top and Front are the same, this is a perfectly symetrical cube ! Don't bother to add 3 reference image on the 3 main axis, just add one, align it with an axis, that's all you need.

<style>
.green {
    color: green;
    display: inline-flex;
    font-weight:700;
    font-size: 30px;
}
.floatright {
  float: right;
}
</style>

##### Need help on the process ?
We will decompose it in smaller parts :
- Add an image ! We showed you how to add an object. An image is an object ! Summon the Add Object menu, and look for Image > Reference.
- Align your image with an axis ! The easiest way is to reset its rotation with `ALT+R`.
- Now, move it on the good axis. ([Need a reminder ?](./pages/shortcuts.md))
- Final step, scale your reference to match the cube ! For this, align your view to the good axis with the direction ball. Just click on the axis that you want. ![](./assets/axis.png)
  Now you should see something like the first image. Scale the image (and not the cube, the cube is PERFECT) to match the cube. Exactly like you can see on the second image.
  <p align="center">
    <img src="./assets/before_scale.png" width="300">
    <img src="./assets/after_scale.png" width="300">
  </p>

Tadaaam ! Great, you have your reference image !
