# WLED-HomeAssistant
Some configuration.yaml and Node Red flows to used to control WLED

These are a work in progress and still need some/much refinement,

WLED_Dashboard: Mostly working except you cant save presets yet. You can set primary and secondary colors, choose presets and power it on and off. I also included an info screen that shows whats currently running, so if you choose a preset it will show you the current info on it.

WLED_RGB_ALEXA_EFFECTS: this uses the "node-red-contrib-alexa-local" Alexa-Local node to communicate to Alexa. NO extra Alexa Skills required and NO account linking required to use this node. How this work is you place the Alexa-Local in your flow and give it a name, then tell alexa to search for new devices. once she finds them they are treated as lights. then you just say "Alexa Preset 1 on" or "Alexa turn on Preset 1". The first 3 nodes in this flow also have extra nodes called "Solid", "Halloween", and "Christmas". I have set the presets in WLED to be the 3 previously named presets and so you can then say "Alexa Christmas Lights on" or "Alexa Turn on Solid Lights" or "Alexa Solid Lights on". you can change them all to named devices or leave them at "Preset 1" and so on.

WLED_Dashboard:	this is a NodeRed flow that creates a nodered dashboard that includes many of the functions of the WLED app. including Speed, Intensity, presets, power, primary color, secondary color and a host of infomation to see whats actually running when you press a preset.

WLED_RGB_LIGHTS.txt:	this code is a NodeRed Flow that creates many of the features needed to run the WLED lights. including all the presets and palettes, effect speed, intensity speed and feedback

configuration.yaml.txt:	creates a MQTT light with all the WLED effects included. This yaml also creates an input_boolean that actually isnt used by the preset buttons included in this post. It also creates a effect_list and a palette_list for use in a pulldown.

wled_preset_buttons.yaml:	these preset buttons is a Plugin Button Card from the HASSIO Community for Lovelace. Button Card is located here http://hassio.local:8123/community and can be installed after you install HACS https://hacs.netlify.com/installation/manual/   Once installed you can create a horizontal place the code in it for a nice looking small footprint set of 16 presets
