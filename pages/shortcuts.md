# Shortcuts

Blender is all about shortcuts.
Yes, menus exists bu uut... Think of it like a game, you don't use menus to jump or move, you use your keyboard ! Same in Blender, doing it all by menus is waaaaaay to long.

We will cover here some of the most used shortcuts.
If you are looking for the "shorcut version" of a menu, just hover over it and Blender will show you the shortcut ! (In most cases)

## Basics

### Rotate point of view
Middle mouse button click, then move your mouse.
([Don't have a mouse with a middle button ?](./emulate_mouse.md))

### Select an object
left click (did you really needed me for that ?)

### Move an object
**G** (G for Grab)

### Rotation
**R**

### Scale
**S**

### Important note
Moving, Rotating and Scalling can be counter intuitive at the begining because they all depend on your field of view. This can seems unnatural. But, Blender has you covered ! You can snap your modification to one (or many) axes of the world (X, Y or Z)
Try it ! Select an object, press G, THEN press X (or Y, or Z). The object will move only on the selected axis.

Press `SHIFT + [X,Y,Z]` to select both BUT the axis given.

## Selection
You can select an object with `Left Click`
If you want to select many objects, you can use `Shift`

### Active element
You should notice if you select more that one object that one of them is surrounded by a larger orange than the others, it's because it is the **active** object, and the others are the **selected** objects. This mean that if you need to see some properties (like the position of the current object by example), these will be the selected object's ones. Same if you need to copy some properties in-between objects, it will go from the active object to the selected ones.

<p align="center">
    <img src="../assets/selection_active.png" width=50%">
</p>

*The cube and the torus are selected, but the sphere is active.*
If you need to change your active object, just deselect it then select it again (always pressing shift).

## Edition Mode
You can switch to Edition Mode with `TAB`
On edition mode, you can see vertices, edges and faces, all of this is explained in the main workshop page.
Note that `CTRL-Z` takes effect both on your selection and your actions, so you can always recover your selection / modification if needed.

To select an edge, a face or a vertice, just click on it.
If you have transparency mode activated, you should see points placed on the center of all the faces (in faces mode). You need to click on them to select a face, because otherwise transparency makes things ambiguous.

In some not so rare cases, two vertices are perfectly aligned in the edition mode. Without transparency you can only select the nearest, but with transparency the selection can be random. So, to select both vertices, use rectangle selection by left clicking somewhere and dragging on your vertices. Both will be selected !

<p align="center">
    <img src="../assets/selection_vertices.png" width=32%">
    <img src="../assets/selection_edges.png" width=32%">
    <img src="../assets/selection_faces.png" width=32%">
    <img src="../assets/selection_vertices_trsp.png" width=32%">
    <img src="../assets/selection_edges_trsp.png" width=32%">
    <img src="../assets/selection_faces_trsp.png" width=32%">
</p>

### Advanced selection
If you want to select many vertices, edges or faces, you can use `Shift`
If you want to select all vertices connecting one vertices to an other, use `CTRL`
If you want to select many vertices at the same time, **click and drag** to do a box selection :
<p align="center">
    <img src="../assets/selection_shift.png" width=32%">
    <img src="../assets/selection_ctrl.png" width=32%">
    <img src="../assets/box_selection.png" width=32%">
</p>

*Shift, Ctrl and Box selection*
(Works with vertices, but also edges and faces)

[<<< Back to the main page](../README.md)
