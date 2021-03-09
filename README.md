# Realtime_EEG_Resting

## Software Requirements

- [BrainVision-RDA](https://github.com/brain-products/LSL-BrainVisionRDA/releases/tag/v1.13.1)<br>

- [python 3.9.1](https://www.python.org/downloads/)<br>

- [OpenVibe3.0.0](http://openvibe.inria.fr/downloads/)

## Data Stream
 
Brainvision Recorder -> RDA -> Brainvision-RDA -> LSL -> Open-Vibe acquisition server -> Open-Vibe Design
 

## Start Signal Streaming

Acquistion Device (接收EEG的電腦)

1. Open BrainVisionRecorder
2. In the Configuration > Preferences …, select the Remote Data Access tab and tick the Enable Remote Data Access box
3. Forward port 51244 to the PC if needed (RDA’s default port: 51244)
4. Fill in the RDA server address (Acquisition Device IP/127.0.0.1 if localhost) and select 51244(Brain Vision Recorder) as source and click Link.

## Start Acquisition
Signal processing Device **Note that this may have to be in the same LAN as the LSL server(PC that Brain Vision RDA is installed on) to work(need to be tested)

1. Open OpenViBE Acquisition Server
2. Select LabStreamingLayer(LSL) (unstable) in the Device section
3. Click the Driver Properties, if the Brain Vision RDA in previous step is working normally, it should automatically fill the signal stream field
4. Click Connect
5. open OpenViBE Designer
6. Load the .xml file 
