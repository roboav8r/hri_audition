# hri_audition
A repo for audition and auditory analysis software for my Ph.D. research in human-robot interaction and human-robot teaming.

A lot of this will be application-specific, but if you have specific questions feel free to reach out to me.

LAST UPDATED: March 2023

## Prerequisites
Install Julius speech recognition engine:
https://github.com/julius-speech/julius

## Current hardware setup
Azure Kinect microphone array

## Usage
Dummy ROS message to send for HARK sound source locations:
```
rostopic pub -r 10 /speaker_source_loc hark_msgs/HarkSource "header:
  seq: 0
  stamp:
    secs: 0
    nsecs: 0
  frame_id: ''
count: 1
exist_src_num: 1
src:
- {id: 0, power: 1.0, x: 0.5, y: 0.0, z: 0.0, azimuth: 0.0, elevation: 0.0}" 

```

## TODO / Future Work
General usability
- ROS launch files for sensors and HARK network

Add hardware:
- 16soundsUSB array - use with Kinect array?

Functions I am working on implementing:
- Speaker localization provided by separate LiDAR/Visual ROS tracking node to HARK network
- Automatic Speech Recognition using Kaldi, Julius, or CMUSphinx
- Background noise classification/scene estimation with Python node
