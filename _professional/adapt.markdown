---
title: "Adapt"
layout: page
image: 
  path: /img/adapt/header.webp
  thumbnail: /img/adapt/thumbnail.webp
  caption: "Picture: A simulated track for power wheelchairs"
---
![adapt platform](/img/adapt/IMG_0819.jpg "The adapt mechanical platform"){: .align-right}
Adapt is an Interreg project in collaboration with the UK that aims to help people with disabilities. One way is by adding sensors to any power wheelchair to aid its navigation. The part I worked on, however, is a power wheelchair VR simulator with a custom-made physical platform that can rotate to simulate accelerations and even bumps on the road.

The challenge of this project was to make a realistic physics simulation, and link it to a physical platform at high frequency using ROS ([www.ros.org](https://www.ros.org/)). In order to have realistic haptic feedback, we tried using the Bullet physics engine to achieve 400Hz, but then went back to PhysX since we concluded that using it at 100Hz was enough.
<br/><br/>
To test our simulator, we built a track for wheelchairs out of wood and cardboard and made the same one virtually. We made wheelchair-bound patient try both to ocmpare them, and I made a replay tool for this purpose.
<video width="576" height="360" controls>
  <source src="/videos/2020-01-31_17-13-48.mp4" type="video/mp4">
</video>

More info on the [INRIA website](https://team.inria.fr/rainbow/fr/adapt-simulator/)
