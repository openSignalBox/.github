# openSignalBox

## Introduction

openSignalBox is a suite of software and hardware designs in development which can drive authentic simulations of railway signalling for many applications. It is a free and open source effort and is intended to inspire a community of users and developers to contribute and improve the suite.

## Software

The openSignalBox project is based around core software of the same name. This software can be thought of as a traditional signalbox simulator, but it is much more powerful by way of modularity, cross-device support and of course open-source design, which allows improvements and upgrades to occur at a much faster rate and to continue for a longer period after release.

The modular nature of the software means that it can suit a variety of applications, not only supporting full signalbox simulations. These include, for example:

* Linking two restored block instruments on two mantle pieces far away from each other over the internet, accurately repeating bell codes and block indicators using small single board computers (e.g. Raspberry Pi Zero) and an interface board.
* Providing virtual interlocking between a physical or virtual lever frame and points and signals on a model railway control bus.
* Simulating route-relay interlocking for panel or IECC interfaces.
* Full signalbox simulator for any size of lever frame, including fringing to virtual lever frames across the internet for joint simulation sessions. Options for spatial sound of trains passing, physical rumbling of the floorboards or frame, and 3D simulation of nearby locations (e.g. level crossing CCTV). Connection to live train locations and timetables for signalboxes facing existing railway lines.

A really useful feature of the simulation engine is that it uses real layouts internally to calculate movements and allows the user to trace this layout from old/current maps or drawings using a web interface. Signalling equipment like signals and track circuits and virtual locations like platform stopping points can be annotated at this stage.

An online database of layouts, traction formations and other items will be made available to share and contribute to so that users can spend more time adding to the community rather than repeating existing work.

The openSignalBox software is a modular framework written in Python 3 with a web frontend and an efficient event-driven core. The backend is written using FastAPI, based on Starlette, and runs on a scalable ASGI server such as uvicorn or hypercorn. The front-end is written with Vue. The software uses modern standard practice and should be easy to modify and extend, by openSignalBox users or contractors. Modules can be written in any language and both the framework configuration and message APIs follow compatibility standards such as OpenAPI. For barebones usage of modules it is also planned to be able to import them into a Python program with a core library and no web frontend.

## Hardware

As the project is a free effort, there is emphasis to support off-the-shelf hardware interfaces so that there is no vendor lock-in and ensuing support problems. A good example is the support of cheap industrial Modbus relay and input modules which have many different vendors online.

Where it is useful, the openSignalBox project will release custom hardware designs to efficiently interface with certain signalling items which cannot be driven from a basic relay. An example of this is the Bell Interface Board, which provides four channels of simultaneous input and output to allow a conventional block bell line to be connected to the simulator.

## Support

It is intended that once established, the openSignalBox community will self-support to an extent, but until then a small team of experts will be available to provide support on an ad-hoc basis. This support will be at the discretion of the available experts and they are free to charge for their work as they see fit (typically depending on the nature of the support and the person/entity requesting it - e.g. charity, individual or business). The source code for new modules written as a result of support will normally be required to be submitted to the openSignalBox project for others to use, but this requirement can be waived in special circumstances if it would reveal interfaces to sensitive IP.

Typical support requests might be:

* A new code module to interface to your custom software.
* Support for a new protocol, e.g. Loconet for model railways.
* Installation and commissioning of a full hardware interface and PC system for a preserved signal box or museum.
* Development of new hardware to interface with a custom piece of signalling equipment (e.g SSI modules).

It is important to note that the open source nature of the project means that users are never forced to pay for support and can source it from wherever they wish, including general software developers as the code follows standard practices.

## Licensing

openSignalBox will always remain free and open source, so please check the license details for each component to ensure you are compliant. If no license is specified, code authored by the project (openSignalBox) is licensed by the GNU AGPL version 3 and hardware by the CERN-OHL-W version 2.

The designs are free to be used for commercial purposes, but as the licenses are reciprocal this means any modifications or improvements to the source must be made available for others to access free of charge. In addition, some components of openSignalBox (the more fundamental ones) will require you to include the phrase "powered by openSignalBox" in a user visible location. This requirement is detailed in the relevant components.

Due to the modular nature of the software, it is possible for users to create their own modules under a different license (or none at all), but we encourage copyleft licenses where possible and if you want the module to be hosted on the main repository then you'll need to use a compatible license. Please get in touch for details or wait for more specific information to be given here when the software is released.

## Team

The openSignalBox project was started by [@elstanto](https://github.com/elstanto) (Laurence Stant), and features a growing team of dedicated volunteers who are working towards an initial release in 2024. If you would like to get involved with the project, either as a developer or a future user, please contact us at [info@opensignalbox.org](mailto://info@opensignalbox.org).
