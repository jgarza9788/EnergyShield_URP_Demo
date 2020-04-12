<!--
Version: 1.0
-->

EnergyShield_URP
-------------------------------------
[Asset Store Link](http://u3d.as/1Q2q)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->

<!--TOC-->


## Contact  

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)  
Alternate Website: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  


## Description Features

Displays an energy shield/force field effects when impacted by projectiles, or raycasts.

* Easily customizable effect. Size, Color, * Speed, etc.
* Renders on simple and complex meshes.
* Simultaneous impact points support.
* Support for culling and non-culling.
* Distortion and Color!
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!


## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

## Overview/Setup 

The Energy Shield is a Shader, with an optional C# Script.
The C# Script manages the collision effects that can be displayed on the shield.

![Imgur](https://i.imgur.com/bfl3yBTs.png)
![Imgur](https://i.imgur.com/rCBpdkis.png)
![Imgur](https://i.imgur.com/cwIDn8Js.png)
![Imgur](https://i.imgur.com/LlIKb95s.png)
![Imgur](https://i.imgur.com/v6dwwZos.png)
![Imgur](https://i.imgur.com/B74O7I6.gif)

## Scripts 

### EnergyShieldManager.cs
Description:  
This Script Creates/Updates the shader to render the energy shield impacts.


CollisionTags:  
Object Tags used to detect if a collision has occured.

Speed:  
The speed at which the impacts update

Color:  
The color of the impacts over time

Size:  
The size of the impacts over time

Thickness:  
The thickness of the impact over time

Impacts:  
this stores the data for each impact

FlipZ:  
some models need their Z axis flipped


### EnergyShieldManagerExtension.cs

If the Collider and the Renderer is on different components this can transfer the point of the impact to the EnergyShieldManager.


### Other Scripts
The Other scripts are basically just used for the Demos.

AlwaysFace.cs:  
Turns the gameObject to face the Target.  

DestroyAfter.cs:  
Destroys an object after a set period of time.  
Used in the projectiles.

Rotate.cs:  
Used to rotate the camera.

ShootOnClick.cs:
Controls the shooting of rays and projectiles.


## Shaders 

### EnergyShield_base.shadergraph
This is the EnergyShield shader.
I'll be adding and modifying this into different styles.

rim:  
this is how much of the edge will glow

offset:  
this is how much of the intersections will glow

normal_add:  
this is good if you want an edge between the model and the shield

max_normal:  
this is how much the normal will shift during the impact

...

## FAQs 

### Why Are Collisions Not Being Detected?
One reason why a collision is not being detected is because the shield is a child of an object with a rigidbody component. I'm calling this the "Rigidbody_ShieldChild" Problem. The solution to this problem is to have a script on the parent object that will detect the collision (Aka use the OnCollisionEnter method) and trigger the shield effect to occur.



