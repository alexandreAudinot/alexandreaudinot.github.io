---
title: "Soudage"
layout: page
image: 
  path: /img/soudage/header.webp
  thumbnail: /img/soudage/thumbnail.webp
  caption: "Picture: A welding station in virtual reality"
---
This project is about teaching students safe arc welding practices and protocols.

<video width="576" height="360" controls>
  <source src="/videos/2025-10-02 18-11-02.mkv" type="video/mp4">
</video>

As a part of the [AIR project](https://projet-air.univ-rennes.fr/), the goal of this application is to add a light VR training at the beginning of the lesson, while still letting students use real welders to practice afterward.

![teacher application](/img/soudage/teacher_application.png "The teacher application used to monitor student progression"){: .align-right}
The teacher is able to manage up to 12 students at the same time using a tablet application that connects to every VR headset. To start the lesson, they can choose from different pedagogical scenarios to give each student the lesson that is best for them. The teacher can then monitor the progress of each student, see the state of their plate and workstation, and see if they commit a mistake or raise their hand.
The network connection originally used Netcode For GameObjects, but was later changed to a direct connection through TCP sockets. The tablet application is made using Unity's UI Toolkit.

![teacher application](/img/soudage/errorSpotting2.png "The student must identify unsafe clothing on the agents"){: .align-left}
When a student start the lesson, the first step will generally be to identify unsafe clothing on some virtual agents standing in the room. They will then be teleported to the welding station, and will have to prepare it, as well as put on the right protection equipement. When the preparations are done, they will weld lines on a plate, while their speed, angle and distance are monitored.
When chosing the pedagogical scenario, the teacher can select different pedagogical guidances or error scenarios. For example, wether to show a list of the equipment to put on, or just a panel that indicates if some are missing. Another example is to let the student weld without gas, or prevent them from doing so.
![teacher application](/img/soudage/scenario.png "An example of Xareus scenario"){: .align-right}

These different possibilities were easy to implement thanks to a local tool developped by the team I worked in: [Xareus](https://xareus.insa-rennes.fr/). Xareus allows the developper to create scenarios via an integrated node-based interface. Scenarios are based on safe [Petri nets](https://www.wikipedia.org/wiki/Petri_net) and can listen to events happenning in the world (an object is grabbed, the student starts welding etc.) and then triggers its own events (show a warning, teleport the user etc.).

More info on the [Rennes University website](https://projet-air.univ-rennes.fr/enseigner-le-soudage-en-realite-virtuelle)
