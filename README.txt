It is very important to note that to get this feature extractor working properly, this is what you will need.

Max/Msp patch called Bark extractor_25 inputs
Processing 1 classifier output message This changes the screen color to match the class received
// Works with 1 classifier output, any number of classes
The purpose of this patch is utilise the microphone built into the computer. The patch then listens for changes in tone and pitch by way of the analyzer and OSC object.
Wekinator is then used to train the different pitches, timbres and tones to make the output processing patch change colour due to the changes in pitch of your voice
The model that was used to train was a First order difference (velocity).This was used on each of the different recorded inputs
The type of project this would be useful for assisting in is one where you are wanting to analyse different vocal pitches in terms of timbre and tone, through a visual means.
So for someone to build this feature extractor:
Max/Msp patch (Bark extractor available from the Wekinator bundle package
Tristan Jehan’s analyser (placed in a Max search path
OSC objects also downloaded and placed in the Max search path.
Wekinator to be listening on port 6448 (default)
Wekinator output port 12000 (default)
Wekinator input helper is used to change the first order difference for the different inputs.
Once you have everything open and communication between the Wekinator and the Max patch is working you can begin recording audio samples with you own voice or you could feed in via the mic different sounds. You then have to train the Wekinator with your different values to change colour in the Processing Classifier patch. That is it!
Pablo
