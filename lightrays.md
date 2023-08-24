# Light rays 2D setup 

### Setting up the URP Rendering Pipeline

!> Modern 2D Light Rays work only with the **Universal Render Pipeline** 

?>If you don’t know how to set it up, check out this 1 minute YouTube tutorial:

https://www.youtube.com/watch?v=pjpcitJim04 (UNITY 2020 LTS and lower)

https://www.youtube.com/watch?v=BCR2xQ7jWMU (UNITY 2021 LTS and higher)

### Linear color space

!> Make sure that your **Color Space is set to Linear** : 

![logo](images/1.png ':size=600')

### Creating Light Rays

!> Creating light rays is really easy. Just choose the **create** dropdown option in the **Light Rays 2D tab**. 

![logo](images/2.png ':size=600')

?>Light Rays 2D Object will appear in the scene

![logo](images/3.png ':size=600')


### Changing Light Rays shape

!> In order to change the size of light rays you can **resize the transform**.

!> You can also **edit the corners** of our light rays quad: 

* Go to the Quad section of Light Rays 2D inspector.

![logo](images/4.png ':size=600')

* Now you can either edit the vertices by **changing the values in the inspector**, or by **dragging the verticies in the scene view** (recommended).

![logo](images/5.png ':size=600')

### Changing Light Rays look

!> The look of our rays is highly customizable. The options that are used for changing the look of your light rays are placed under the light rays tab.

![logo](images/6.png ':size=600')

!> **Let's go over the most important ones.**

> **Sorting Layer** sorting layer of our rays, when they are used in 2d scene.

> **Final alpha** is used to change the final alpha value of our summed rays alpha.

> **Sliders under the final alpha** are used to change the alpha of each light ray layer. These layers are later combined to create the final image.

> **Densities** are used to change the density of each light ray layer. With smaller density, the singular rays look bigger. 

> **Speeds** are used to change the speed of each light ray layer.

> **Falloffs** are used to adjust the light rays alpha falloff from each side of the quad. 

> **Harder Edges** are used to create harder edges by smoothsteping each light rays layer.

> **Colors** are used to color the light rays. Each Color corresponds to the quad corner. The final color is achived by interpolating the corners. If you want the rays to have one stable color on the whole surface, set the four color fields to the same color.