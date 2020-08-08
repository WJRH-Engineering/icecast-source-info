# WJRH Remote Broadcasting
WJRH Engineering has enabled DJs to broadcast remotely. This guide provides setup instructions and recommendations for broadcasting a remote live show to WJRH 104.9 FM. 

## How It Works
WJRH Engineering has setup an Icecast server to host remote broadcasts. Icecast is an open source streaming standard that is widely used among internet radio broadcsters. More information about Icecast can be found at [https://icecast.org/](https://icecast.org/). DJs will need to run software to generate an Icecast source that will be relayed by the WJRH Icecast server to listeners and to main station's broadcast.

![Icecast Stream Structure per mount point](https://lh3.googleusercontent.com/proxy/OI2e8wE529ZBGwqpBfHAHtVki5aAjqdqlfoZrwfo4Y_MaNAXzbJMSIPMv-d2TUO7uPyleVqGinCLaz38aPEfLtlCI5D6AA)

Every WJRH program in the schedule will have a unique mount point on the WJRH Remote Broadcast Icecast server. DJs may remotely broadcast an internet program at any time. Remote broadcasts will only be relayed to the main station during your scheduled program time.

This guide will provide setup instructions to create Icecast sources on your computer for use in broadcasting to WJRH. The instructions in this guide have been tested by WJRH Engineering. DJs are free to use any method to create Icecast sources.

## Setup
In order to broadcast remotely, DJs must be able to create Icecast sources. This is done using an Icecast soruce client. There are many Icecast source client. The options discussed in this guide have been tested by WJRH Engineering and were selected for general usage. DJs may use whatever Icecast source client they prefer.

### Icecast Mount Point Settings
Every program will have a uniquie mount point. Use the following settings in your Icecast souce client.

|Setting|Value|
|-------|-----|
|mount|*Program shortname (Teal API)*|
|username|**source**|
|password|*Provided by WJRH Engineering*|

WJRH Engineering will provide mount, username, and password to broadcasters upon request.

Note that only one person may connect to a mount on the Icecast server at a time. You will need to coordinate with the members of yoour program to decide who will generate the Icecast source for each episode. This person generating the Icecast source will be referred to as the broadcaster. Audio from colloborators will need to be added to the mix by the broadcaster.


### Recommended Icecast Source Client
WJRH Engineering recommend the broadcast using this tool (butt) program for generating an Icecast source. Butt is available for Windows, Mac, and Linux. 

1. Please download butt at [https://danielnoethen.de/butt/](https://danielnoethen.de/butt/). 

![https://danielnoethen.de/butt/](images/butt/install-setup/webpage.jpg)

![https://danielnoethen.de/butt/](images/butt/install-setup/webpage-download-links.jpg)


2. Install butt.

3. Run butt.

![butt-startup](images/butt/install-setup/butt-startup.jpg)

4. Open butt settings.

![butt-settings-main-default](images/butt/install-setup/butt-settings-main-default.jpg)

5. To add the WJRH Icecast serve, click Add.

![butt-settings-main-server-add](images/butt/install-setup/butt-settings-main-server-add.jpg)

6. Fill out the server information replacing your-program-name, your-mountpoint, and your-password for your WJRH program. If you are unsure about this information, please contact WJRH Engineering.

![butt-settings-main-server-add]-example(images/butt/install-setup/butt-settings-main-server-add-example.jpg)

By default, butt will only broadcast audio input devices, such as the built in microphone on your computer. To broadcast from audio programs on your computer (e.g. Spotify), a virtual mixer will need to be used.

### Recommended Virtual Mixer

#### Windows 
WJRH Engineering recommends using VoiceMeeter as the virutal mixer. 

Download VoiceMeeter at [https://www.vb-audio.com/Voicemeeter/](https://www.vb-audio.com/Voicemeeter/).

A more complex version of VoiceMeeter Banana is a more complex version of VoiceMeeter that provides additional audio inputs and outputs. It can be downloaded at [https://www.vb-audio.com/Voicemeeter/banana.htm](https://www.vb-audio.com/Voicemeeter/banana.htm).



### Optional
[https://www.vb-audio.com/Cable/index.htm](https://www.vb-audio.com/Cable/index.htm)

## Examples
WJRH Engineering knows that all shows are different. Here are some recommended ways to implement common show elements using the recommended setup on a Windows Computer.

### Case 1 - Computer Audio Output
Icecast Source Client: butt
Virtual Mixer: VoiceMeeter

Audio Inputs
- Computer Audio Output

Audio Outputs
- Main mix for Icecast source
- Audio for Broadcaster (speakers/headphones)

### Case 2 - Single Microphone
Icecast Source Client: butt
Virtual Mixer: VoiceMeeter

Audio Inputs
- Broadcaster Microphone

Audio Outputs
- Main mix for Icecast source
- Audio for Broadcaster (headphones)

### Case 3 - Single Microphone with Computer Audio Output
Icecast Source Client: butt
Virtual Mixer: VoiceMeeter

Audio Inputs
- Broadcaster Microphone
- Computer Audio Outout

Audio Outputs
- Main mix for Icecast source
- Audio for Broadcaster (headphones)

### Case 4 - Single Microphone with Program Specific Audio Channel
Icecast Source Client: butt
Virtual Mixer: VoiceMeeter + Virtual Audio Cable

Audio Inputs
- Broadcaster Microphone
- Program Audio Output

Audio Outputs
- Main mix for Icecast source
- Audio for Broadcaster (headphones)

### Case 5 - Single Microphone with Collaborator Skype Audio
This setup will show how to create a mix in VoiceMeeter to support collaborators over Skype.

Icecast Source Client: butt
Virtual Mixer: VoiceMeeter Banana + Virtual Audio Cable

Audio Inputs
- Broadcaster Microphone
- Skype Audio Output

Audio Outputs
- Main mix for Icecast source
- Audio for Broadcaster (headphones)
- Audio for Skype Collaborators

### Case 6 - Single Microphone with Collaborator Audio and Program Specific (may be only able to do computer audio output for free (can be done if buying the dual virtual audio cable) Audio Channel 



## Recording & Song Logging
We will continue to use Teal to record shows and log songs. If your will be remote streaming to the main station, Teal will work exactly the same if you were in the studio in Hogg Hall and your recording will be available automatically on Teal.

All remote streams will be recorded reguardless of whether they are relayed to the main station. Contact WJRH Engineering for a copy of remote broadcast. PLease include your show's name, the mountpoint used, and date and time of broadcast.
