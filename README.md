node-red-contrib-astrodata
=============

[![NPM version](https://badge.fury.io/js/node-red-contrib-astrodata.svg)](http://badge.fury.io/js/node-red-contrib-astrodata)

This package contains two node-red nodes to calculate astronomical data for a given position.


This is an extented version of tlindener/node-red-contrib-rcswitch with support of different switch types, tristate and binary strings.

The implementation based on https://github.com/marvinroger/node-rcswitch. The supported switch types are described there.

Node bindings for the [rcswitch RaspberryPi port (pin)](https://github.com/r10r/rcswitch-pi).

It should be compatible with all versions of Node.js starting from 0.10.x.

## Requirements

* The nodes have no special reqirements and should work with node-red 0.12 and newer.

The node astrodata dayvalues calculates astonomical data for the current day. Set longitude and Latitude of the place in decimal form and height of the place in meters in the properties dialog. s dialog.
The msg object also contains the attributs msg.sunAstronomicalTwilightMorning, msg.sunNauticalTwilightMorning, msg.sunCivilTwilightMorning, msg.sunRise, msg.sunTransit, msg.sunSet, msg.sunCivilTwilightEvening, msg.sunNauticalTwilightEvening, msg.sunAstronomicalTwilightEvening, msg.sunSign, msg.moonRise, msg.mondkulmination, msg.moonSet , msg.moonPhaseNumber, msg.moonPhase and msg.moonSign.
The msg object also contains the attributs msg.sunDistance in km. msg.sunDistanceObserver in km msg.sunDeclination in Grad msg.sunAzimut in Grad msg.sunAltitude in Grad msg.sunDiameter msg.moonDistance in km msg.moonDistanceObserver in km msg.moonDeclination in Grad msg.moonAzimut in Grad msg.moonAltitude in Grad msg.moonDiameter and msg.MoonAge in Grad for the current time.
All other attributes ob the input msg object will be passed to the output msg object.

The node astrodata sunposition calculates sun position for the current time. Set longitude and Latitude of the place in decimal form and height of the place in meters in the properties dialog.
Set longitude and Latitude of the place in decimal form in the properties dialog.
The msg object also contains the attributs msg.sunDistance in km. msg.sunDistanceObserver in km msg.sunDeclination in Grad msg.sunAzimut in Grad msg.sunAltitude in Grad msg.sunDiameter msg.moonDistance in km msg.moonDistanceObserver in km msg.moonDeclination in Grad msg.moonAzimut in Grad msg.moonAltitude in Grad msg.moonDiameter and msg.MoonAge in Grad. All other attributes ob the input msg object will be passed to the output msg object.