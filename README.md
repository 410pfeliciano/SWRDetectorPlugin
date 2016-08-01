# Sharp Wave Ripple Detector 

Sharp Wave Ripple Detector for open-ephys plugin-GUI. It is built to work in Windows. It is based off of the PhaseDetector module available, but fundamentally has a different purpose. It triggers an event  upon detection of a sharp wave ripple complex, according to the method by [Stark et al.](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4393648/):

* compute the RMS value of two running windows, long (2s) and short (8 ms), of band-pass filtered (80-250 Hz) signal
* when RMSShort > k * RMSLong for continuous 8ms, trigger an event, with k a float constant input by user into GUI (threshold constant)
* event-on time can be input by user in GUI (event stimulation time)

## Installation

Copy the SWRDetectorPlugin folder into the plugin folder of your GUI. Then build as described in the [wiki](https://open-ephys.atlassian.net/wiki/display/OEW/Windows)
