# LF9

**Brand**: Brandless

**Product**: Dashcam

**Model**: LF9 Pro

**Wifi**: HiDvr_*

**Product Links**:
 - https://www.aliexpress.com/item/1005001569438534.html
 - https://www.dhgate.com/product/lf9-pro-dash-cam-1080p-night-vision-car-dvr/884732017.html?skuId=1140075696569122859
 - https://www.electronicpro.co.za/products/lf9-pro-1080p-full-hd-car-dvr-wifi-night-vision-170-degree-wide-angle-dash-cam-app-voice-control-g-sensor-dash-camera-recorder
 - https://www.lazada.sg/products/noyafa-dash-cam-1080p-car-dvr-for-car-camera-black-camera-dashcam-24-hour-parking-monitoring-loop-recording-lf9-pro-i3101144848.html
 - https://www.lazada.sg/products/lf9-pro-driving-recorder-dash-cam-1080p-hd-car-dvr-wide-angle-lens-gsensor-parking-monitoring-wifi-smart-voice-i3270955235.html
 - https://shopee.sg/LF9-WiFi-Dashcam-1080P-Night-Vision-Car-Dash-Cam-24h-Parking-Monitor-2K-Car-Camera-Recorder-Car-Accessories-i.265065378.28453064504

## Finding 1 - CVE-2025-6532: Unauthenticated Access of Livestream and Download of Video Recordings

**Description**: Once connected to the dashcam, an attacker can dump all video recordings via http://192.168.0.1:80/$filename without any http-level authentication. To obtain a list of video recording filenames, the following steps need to be performed via API calls:

 - register the client
 - check work state
 - stop work mode
 - get directory capabilities
 - fetch file list

![image](https://github.com/user-attachments/assets/f86966ad-52aa-4734-a92d-7efc778699d1)

The livestream can also be fetched directly without further authentication at rtsp://192.168.0.1:554/livestream/1

**Vulnerability Type**: Incorrect Access Control

**Vendor of Product**: HiDvr

**Affected Product Code Base**: LF9 Pro

**Affected Component**: Video storage and live feed

**Attack Type**: Remote

**Impact Code execution**: False

**Impact Information Disclosure**: True

**Attack Vectors**: An attacker connected to the dashcam's network can access the live feed and dump all sensitive video recordings.

**Has vendor confirmed or acknowledged the vulnerability?**: No

**Product Images**:

![image](https://github.com/user-attachments/assets/bf3ea064-7c3d-4598-b0db-427028a5b8d5)

![image](https://github.com/user-attachments/assets/c9a17bf2-a521-49e9-b1a2-0c03d89fef51)

![image](https://github.com/user-attachments/assets/94ee4c2e-e980-4257-aaea-6598d16b7d7d)
