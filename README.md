 *	Description:
 
 		  This app is called “Hallway Light” as it is meant for places where you often pass through and 
 		  therefore don’t need much light to find your way.  On the other hand, if you stay in the room a
 		  little bit longer, you would probably like to have more light.

 		  The main difference between this app and Smart Light by SmartThings, is that this app allows
 		  you to control the lights in more ways, like the minimum and maximum levels of light
 		  depending on evening/morning and night settings and detecting if other apps have taken control
 		  over the lights and therefore should leave the lights as they are etc.
 
 *	Compared to Smart Light by SmartThings, this app solves the following problems:

 		  Color of LIFX bulbs is not handled very well (e.g. Warm White does not work at all).
 		  Start and end times does (or did?) not work in Smart Light.
 		  Destinctions between evening and night settings in one app.
 		  Definition of a ownership concept, where the app can detect if other apps is used to set the lights.
 		  Better control of levels of lights than just on/off.
 		  Adding more than one contact/motion sensors.

* Limitations and missing things:

     The app hasn’t been tested yet with other bulbs than LIFX, but that will change very soon.
     The way the app checks for ownership, is by checking whether the bulbs level has changed or not. 
     The reason for doing it that way and not by atomic-state, is that groovy on smartthings, doesn’t really
     support threading and therefore very often lead to race-conditions.

     I know this may be a problem when dealing with a mix of different brands of light bulbs, so I plan to 
     add the possibility of selecting those bulbs, where the ownership should be tested up against.

 * Of other things planned…:

     Support of setting colors
     Support of controlling outlet switches, e.g. when the level reaches maximum
