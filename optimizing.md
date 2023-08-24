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