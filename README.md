# Home_assistant_backup
backup of the hA Config

This is my HA config, with titbits borrowed from various other Git HA repos.

Most of the scripts are stright forward, but the one thing i wanted to do was create a heating system, that would integrate with Alexa.

My heating system consists of a number of items.
1. <B>Input_Number </B> - used to set the temperature for the various times the heating activates.
      Morning - the scheme for first thing in the morning, when we're all getting ready to go to work etc.
      Between cycles - used during the day, and overnight.
      Evening - for when we all get home.
2. <b>Input Boolean </B> - used to set Vacation modes, and school holiday modes
3. <b>sensors </b>.
  A temperature sensor to guage the front room temperature (my home has an all or nothing heating system)
  A heating mode sensor, to return the name of the 'in use' heating mode
4. <B> input_select </B> - used to set the times for the heating periods.
5. <b>Automations </b> - active when the time = input_select time. 
   during this period, any change to the Input number sliders is pushed across to the climate control, which activate if below the target temperature
 6. <b> Alexa Intents </B> as an intent, requesting 'Doris' to set the temperature, 
    automatically recognises the current heating period, and sets the temperature accordingly. (using the output of the sensor template)
    
Feel free to hack away at what i've done and propose changes, as i am all self taught, and no expert!
