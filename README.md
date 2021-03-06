HMT
======

![HMT logo](https://github.com/andrew-lowell/HMT/blob/master/hmt_logo_01.png)

**Houdini Music Toolset**, extends the users' capabilities into the domain of music composition.
**[HMT Demonstration](https://vimeo.com/425382356/a4a52d71c1)**

HMT makes use of Houdini's powerful geometry and simulation processing in a set of new tools and workflows specifically designed for music. It uses point clouds and attributes within the graphical 3D environment to perform sequencing tasks present in music composition packages. It uses CHOPs as a back-end to import or export MIDI file data either to the midi file format, or directly to a MIDI port. It allows for artists or composers to make use of powerful simulation tools and Houdini's open node-based architecture normally dedicated to producing photorealistic simulations of natural phenomenon and apply the same tools if desired to manipulating or generating patterns of notes.

Because of the modular and node based nature of the toolset present in HMT, and that it adheres when possible to existing Houdini conventions, it allows users to easily develop their own workflows and tools for music creation or processing.

* * * * *

### Installation:

Download the desired release directly from the [releases page](https://github.com/andrew-lowell/HMT/releases) and extract it to your hard drive or network share.

**Plugin (17.5+ only)**
Create a folder inside your Houdini preferences directory (where the houdini.env typically lives) called "packages", and place the HMT.json file from the HMT download into that folder. Then edit HMT.json and change the "HMT" variable to match the install path.

***This toolset does not produce sound,*** it acts as a sequencer and sends MIDI data to an audio application or MIDI file. Most professional or popular music programs will support a MIDI port which can be used to then trigger real-time sound and instruments. See the [supplementary software page](https://github.com/andrew-lowell/HMT/blob/master/SOFTWARE_LINKS.md) for more on getting your system up and running.

**OS Support (Full functionality Windows only)**
While the toolset is based entirely in Houdini and will perform it's sequencing functions regardless of operating system, the MIDI Output CHOP will only perform live/real-time export to a MIDI channel on the Windows operating system. When Apple/Linux are supported this page will be updated. Exporting to MIDI files is supported on all operating systems.


* * * * *
### Workflows:
* **[Software Connectivity Flowchart](https://github.com/andrew-lowell/HMT/blob/master/hmt_workflows.pdf)**
* **[Supplementary Software](https://github.com/andrew-lowell/HMT/blob/master/SOFTWARE_LINKS.md)**


* * * * *

### Usage basics:
* **[Introduction and Demonstration](https://vimeo.com/425382356/a4a52d71c1)**

***Tutorial Links***
* **[00 Installation and Sound Check](https://vimeo.com/416777838/0fd198367a)**
* **[01 Simple Note](https://vimeo.com/416991416/ce039a640a)**
* **02 Note Patterns** ***(Coming soon)***
* **03 MIDI IO** ***(Coming soon)***
* **04 Time Adjustment** ***(Coming soon)***
* **05 Timing Setup** ***(Coming soon)***
* **06 Pitch Setup** ***(Coming soon)***
* **07 Duration Setup** ***(Coming soon)***
* **08 Panning Setup** ***(Coming soon)***
* **09 Velocity Setup** ***(Coming soon)***
* **10 Timing Distortion** ***(Coming soon)***
* **11 Velocity Impulse** ***(Coming soon)***
* **12 Modal Setup** ***(Coming soon)***
* **13 Modal Assignment** ***(Coming soon)***
* **14 Velocity Impact** ***(Coming soon)***
* **15 Velocity Distance** ***(Coming soon)***
* **16 Doppler Setup** ***(Coming soon)***
* **17 Doppler Application** ***(Coming soon)***

***Shelf Tools***
* **MIDI IO Setup**: This will create a MIDI Output to a `.midi` file. Then downstream read the same file in and play it back through a live MIDI channel (Windows only).
* **Random Notes**: This setup is useful to observe the necessary point attributes being assigned manually then output through a live MIDI channel.
* **Mode Progression**: The mode progression setup is useful because there is a certain order of operations and mode attributes necessary upstream to produce the `i@note` attribute downstream. First the mode attributes are assigned based on mode, octave, base note, and mode progression. Then the final `i@note` attribute is computed and output through a live MIDI channel.
* **Sound Check**: This will create test spacial MIDI composition with visualization and play it back through a live MIDI channel (Windows only).

For more detailed examples, see the [provided examples](https://github.com/andrew-lowell/HMT/tree/master/examples) folder for Houdini (.hip) files.

* * * * *

### Technical Specifications:
[Geometry attributes used by HMT](https://github.com/andrew-lowell/HMT/blob/master/ATTRIBUTE_SPECS.md)

* * * * *

### Developers:
**HMT (Houdini Music Toolset)** is developed and maintained by ***Andrew Lowell***. 

* * * * *

### Notice:
This software is provided AS-IS, with absolutely no warranty of any kind, express or otherwise. We disclaim any liability for damages resulting from using this software.
