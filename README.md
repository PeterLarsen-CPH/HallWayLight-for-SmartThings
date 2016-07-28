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
             You can add a button controller to activate/deactivating the app, e.g. if you don't need the light for a period.

* Limitations and missing things:

            The way the app checks for ownership, is by checking whether the bulbs level has changed or not. 
            The reason for doing it that way and not by atomic-state, is that groovy on smartthings, doesn’t really
            support threading and therefore very often lead to race-conditions.
            
            The four periods of the day, have been hardcoded:
             DAY => sunrise to sunset
             EVENING => sunset to 23:00pm, friday and saturday to 23:59pm
             MORNING => sunrise to 6:00am, saturday and sunday to 7:45am
             NIGHT => the time betwwen EVENING and MORNING

 * Of other things planned…:

            *Support of setting colors.
            *Support of controlling outlet switches, e.g. when the level reaches maximum.
            *Option to leave light as it is if already on or if the level of light is already higher than it otherwise would be set to. 
            This is useful if you have more than one sensor to control a light bulb and you want different levels of light depending on which sensor activating the light.
