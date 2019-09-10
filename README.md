# Particle-Door-Open
Use an app (IFTTT "DO") to activate an electronic door strike for keyless entry to a building or room.

This project provides the means to unlatch a door using an app on an iPhone or Android device.  It is useful for keyless entry into a building or room, activated locally or from anywhere in the world.

An electronic door strike replaces the standard door strike and allows access when it is activated electrically.  A 12 volt DC door strike is recommended, however the door strike is activated by a relay and can therefore operate on any low voltage DC or AC.  The door knob/lock continues to operate normally.

A Particle Photon (or Core) is used for WiFi connection to the Internet.  A Particle Relay Shield provides the activation electricity to the door strike.  The Relay Shield accepts 12 VDC and regulates this down to 5 VDC to power the Photon and the relays.  The 12 VDC is also used to activate the door strike.  The Relay Shield has 4 relays; only one is used for this project.  The other 3 relays may be used to activate other things in the home or room.  All that is needed is for additional Particle.function() functions to be written to service whatever is connected to these relays, and associated "DO" recipies created.  A PDF "System Overview" diagram and a PDF "Schematic" diagram are included in this repository to further explain the project.

The app that is used to remotely activate the door strike is the "DO" app from IFTTT.com.  A DO button is created using this app which, when tapped, calls a function on the Photon that activates the door strike.  The activation time is set in the DO button recipe and can easily be changed without changing Photon software.

This project and all documentation herein is licensed under a Creative Commons license Attribution-Non-Commercial 4.0.  To view a copy of this license, visit http://creativecommons.org/licenses/by-nc/4.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.  All material is copyright (c) 2016 to Bob Glicksman with terms of use specified in the aforementioned license.

Caution:  This project requires the user to install an electric door strike on a door frame.  Significant carpentry skills and appropriate tools are required to successfully install this product.  Do not attempt this project unless you have access to the necessary tools and skill set.  A sample video about installation of a similar door strike in a wooden door frame can be viewed at:  https://www.youtube.com/watch?v=dImYdCY89CM. 

## Update: 9/09/19
Added an Android app to replace the IFTTT DO button.  The Android app was created in MIT App Inventor 2 and
uses the Team Practical Projects Particle_App_Template, which can found at:

https://github.com/TeamPracticalProjects/Particle_App_Template

The Hardware and Firmware remain the same.  To use this app, simply load the .apk file onto your Android device 
and tap on this file to install it.  When you initially open the app, you will have to go to the Setup screen and
enter your Particle user name and password where indicated and then search for devices.  Select the Particle
Photon device that you are using for this project from the popup list and then exit Setup.  Your device
should now be permanently selected (until you change it again in Setup) and you can tap the OPEN button to open
your door with the duration (in milliseconds) indicated in the textbox to the left of the button.  The default
duration is 2 seconds (2000 milliseconds) but you can change this by typing in the number of milliseconds 
that you desire.  The app will limit your choice to 10 seconds (10,000 ms) maximum.

