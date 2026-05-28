# Ardumower

## Rationale
This is my personal copy of Ardumower repository; I'm trying for fun to "brain transplant" an old Husqvarna Automower 230ACX that's still working except for mainboard. Currently (May 2026) it still isn't operational. I'm not interested in GPS/no guide wire feature, as I have already installed one and my garden is very, very complicated and covered by trees. Frankly, I thought the mayor challenge with Ardumower was to control brushess 2 poles mower motor (it seems no BLDC advertise this usecase). After trying to build the firmware, I discovered the true problem was with it. 
Wheel motors not working regardless of settings, ADC values nonsense, communication hangs, PFOD menus breaking and dancing settings, and much more.
After having a look at the code, I discovered it's a mess. One problem is due to an understandable reason: the code was modified by many people, each one with a specific hardware; to fix own issue, often one would break others. For instance, the option for choosing a motor controller didn't read power if another was selected. Another thing I realized is that someone took a current measurement for a parameter - so if you adjust it on remote control you see it going up and down with motor load.
Apart from this, Azurit is a complex piece of software, embedding many customized library functions, hard to fully understand.

So I had to options: throw it away with the hardware, or try playning with it, leveraging Vibe Coding. I'm an old school C programmer, my notions of object oriented are spotty, so here I am. This repository is here for me; if someone is playing with it as well, use it as you like.

Warning: I can only test one specific hardware. However, I've not deleted code for other hardware; maybe I'll do it, maybe I'll simply mark it somehow as "untested". 

## Documentation from original Ardumower/Azurit project.

## Description
Develop an open source robotic lawn mower (HW+SW reference platform)

## Project site
http://www.ardumower.de

## Wiki site
http://wiki.ardumower.de

## This repository contains
* Ardumower robot code (Arduino code)
* Ardumower perimeter sender code (Arduino code)
* Ardumower PCB schematics (PDF, KiCAD)
* Ardumower simulator (requires CodeBlocks - see installation details here:  http://wiki.ardumower.de/index.php?title=Sensor_fusion#SLAM_simulation)
* Ardumower tests (MC33926, DS1307, LM386, HCSR04, GY-80, ESP8266, HB200A, MPU9150, HC-05, PfodApp)

## License
Ardumower (www.ardumower.de)
<br>Copyright (c) 2015-2017 by Uwe Zimprich
<br>Copyright (c) 2014-2015 by Stefan Manteuffel
<br>Copyright (c) 2014 by Walter Crauwels
<br>Copyright (c) 2013-2015 by Sven Gennat
<br>Copyright (c) 2013-2017 by Alexander Grau
<br>Copyright (c) 2014 by Maxime Carpentieri
<br>Copyright (c) 2015-2017 by Juergen Lange    

Private-use only! (you need to ask for a commercial-use)
 
The code/schematics/PCB files are open: you can modify it under the terms of the 
GNU General Public License as published by the Free Software Foundation, 
either version 3 of the License, or (at your option) any later version.

The code/schematics/PCB files are distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

Private-use only! (you need to ask for a commercial-use)

