> [!CAUTION]
> This project is in extremely early phase of development. If you are reading this, I have not done anything concrete with this project, purely some note taking and proofs-of-concepts. I have done my research and I believe my idea is possible, but that is just a theory. If this project doesn't work out, I will mark this repo as an archive just in case. Until then, this repository solely exists as documentation of information relating to adapting a raspberry pi into a Q10 chassis.

# Blackberry Pi CM4
Blackberry Q10 Raspberry Pi CM4 Retrofit

## Introduction
This project was inspired by finding an old phone in a drawer. One with a real keyboard that slid out. From this, I started searching online to see if people were still using phones like this in the year 2025, and surely enough, I fell upon the dumphone community. As someone who has been focused on keeping my screen time to a minimum, the vision of the dumbphone community resonated with me. The problem was that there simply aren't that many dumphones that work anymore, especially in the US.

Current contenders for modern dumbphones are the likes of the Qin F21/F22, Unihertz Titan series, and some miscellaneous flip phones. There are also some more bespoke custom dumbphones, however these have their own quirks that make them a hard sell to some people. One of the coolest older phones I was seeing online was the Blackberry Q10 and Classic. In some parts of the world, these are still fully functional, making them a great way to get into the dumbphone world and experience those amazing Blackberry keyboards. Problem is, despite supporting 4g LTE, the Q10 and Classic do not support VoLTE, which is absolutley necessary to make calls in the US. This severely hampers the functionality of these phones here in North America.

Another challenge is app support. A lot of people simply can't go the dumbphone app because of support for their communications apps. In the US, most people are fine with SMS (for some reason that's beyond me) but RCS is gaining traction, especially since it is now natively supported by apple devices. The challenge is that in other countries, Whatsapp is by far the most common form of communication, and it is simply a no-go to give up support for Whatsapp. Those who are privacy conscious use Signal as a form of communication, which also requires a relatively modern build of Android. Beyond communication apps, there is also the desire to have access to banking apps, 2 factor authentication apps, music streaming, bluetooth support, etc. 

So I started thinking: what if I could put a Raspberry Pi in a Q10 chassis? A CM4 would be plenty small enough to fit inside, and it would be able to run modern Android, support modern communication services, and with a cellular modem should be able to connect to modern cellular infrastructure. A custom build of Android would allow for tons of customizability, allowing dedicated dumbphone enthusiasts to make the phone as dumb or as smart as they desire. And so I started researching a little bit, fully expecting to hit some insurmountable challenge that would make this completely infeasible. But as I researched, I found solutions to some of the biggest challenges, and I slowly started to realise that this has a chance of being successful. 

## Project Objectives
The objective of this project is to provide a drop in replacement mainboard for the Blackberry Q10 that will allow for a Raspberry Pi Compute Module 4 to run Android. This would bring this awesome little phone into this decade and would make it usable as a daily driver phone, especially in areas such as the US where VoLTE is a requirement for phone calls and 3g networks are practically phased out. 

Here is a list of desired features:
- Drop in replacement: little to no modification of any component inside the Q10. Should be fully reversible if one so desires.
- Modern Android: should be running a modern build of Android and be able to update. LineageOS is the current plan to provide this.
- Hardware Keyboard and Touch Support: The hardware keyboard on the Q10 should be functional and the touchscreen should be working as well. No cheating with a keyboard operated cursor.
- 4g LTE connectivity: use modern, relatively fast, cellular infrastructure.
- Google Play Support: native google play support so that apps can be easily downloaded and run with the latest versions. Focus will be on communication apps such as Signal, Whatsapp, etc.
- RCS Support: be able to send and receive RCS messages instead of relying on SMS as a crutch.
- VoLTE Support: be able to make and receive calls on modern cellular networks.
- Use existing hardware buttons for power/volume controls.
- Use existing speakers and headphone jack for audio. Use a decent DAC so that wired headphones can be used.
- USB C charging: one cable to rule them all, also USB 2.0 OTG support.
- 8 hour of battery life in a normal day of use: doesn't need to be able to stream videos all day, but should at least be able to handle moderate use without needing to be charged.
- Forward compatibility with CM5
