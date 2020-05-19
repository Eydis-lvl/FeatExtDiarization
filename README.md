# Prosody feature extraction with speaker information
This Praat script is designed as a submodule to be used with the diarization annotation tool XXX. The script takes as input a audio file and a corresponding .rttm file with speaker annotations. The script calculates the prosodic features Pitch, Harmioncity and Intensity from the audio input. The features extracted are collected in time steps of 0.01 seconds, paired with the corresponding speaker information from the .rttm file. The output is stored in a Features\<filename>.txt file. Features are extracted for the entire audio file and collected for voiced as well as unvoiced sections.

## Requirements
* Praat non GUI version is sufficient
* Judy's diarization tool


### Parameter settings
The features extracted and their parameter settings are 

* Pitch: Time steps=0.01 s, Pitch floor=75 Hz, Pitch ceiling=600 Hz
* Harmonicitiy: Time steps=0.01 s, Pitch floor=75 Hz, Silence threshold = 0.1, Number of periods per window=4.5
* Intensity: Minimum pitch=75 Hz, Time step=0.01 s


### Speaker information
Speaker information is retrieved from an rttm file, assumptions are that the format of the files does not change form the following:

			SPEAKER Fréttirkl1900-5004310T0 <NA> 0.10 0.12 <NA> <NA> SpeakerTag <NA> <NA>

Assumptions are that the timing information is aligned from the beginning between the audio and .rttm files.

Output is a .txt file containing information 

			Time[s]	Pitch [Hz]	Harmac	Intensity	Speaker nr.		
			6.520	132.410		6.091	80.373		SpeakerTag1

			
### Credits

Developer

Eydis Huld Magnusdottir - eydishm@ru.is

This is part of the Language Technology Program by The Icelandic Government through Almannaromur
