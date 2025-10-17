# Modern 2D LightRays Documentation

> official documentation of this asset 

If you have any problems or you don't understand something in the docs, you can write to me on my official discord server. It's a server for : 

- bug reports

- feature suggestions

- update reports

- quick fixes 



<font size = "4"> If you already worked with the asset and want to share your thoughts, I encourage you to  <span style = "color : red"> 💖<a href = "https://assetstore.unity.com/packages/slug/259097"> leave a review! </a> 💖 </span> </font>

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

# URP Light 2D 

!> You can turn Light Rays into light sources by enabling the URP Lighting in the inspector:

![logo](images/8.png ':size=600')

!> This will create the Light 2D component with it's shape automatically resembling the light rays shape.

# Particle Systems

### Setup

!> In order to add the particle system you have to check the **enable checkbox** in the Particles section of Light Rays 2D inspector.

![logo](images/9.png ':size=600')

!> Types of particle systems:

![logo](images/10.png ':size=600')

* Surface -> Particles spawn and **float on the surface** of your light rays. 
* Surface Climbing -> Particles spawn and **float up on the surface** of your light rays 
* Top Falling -> Particles spawn from the **top edge** of light rays and **fall**.
* Bottom Climbing -> Particles spawn from the **bottom edge** of light rays and **rise**.

### Changing the values

!> Most significant values of your particle system can be easily changed in the Light Rays 2D inspector:

![logo](images/11.png ':size=600')

!> The Rest can be adjusted in the particle system component under the light rays 2d. 

![logo](images/12.png ':size=600')

![logo](images/13.png ':size=600')

!> You have to keep in mind that the values that are set in the light rays 2d inspector will override the values in this component. Values that will be overriden:

* start speed

* start size

* shape

* spawn rate

* color

* sprite

* noise strength

* lifetime

!> These values can only be changed in the Light Rays 2D inspector.

# Demo Scenes

?> There are multiple **demo scenes** in which you can see how the light rays are set up in certain game scenarios and even copy the light rays objects.

?> The sprites are made by me, so, while I personally wouldn't do that, **you can use them in your projects**.

![logo](images/7.png ':size=1200')

# Optimizing

!> In order to keep the fps count high, you can do the following:

### pc

- Don't have more than 32 full screen light rays objects rendered at the same time

### mobile 

- Don't have more than 8 full screen light rays objects rendered at the same time

- You can uncheck the additional two layers checkbox in the Light Rays tab of Light Rays 2D inspector (rays will look worse but will be ~33% faster)

- Don't use too much light rays with gradient coloring at the same time 

- Control the number of particle systems in one scene

- Don't use URP Lighting or use with caution
