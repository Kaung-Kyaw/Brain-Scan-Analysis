# Brain-Scan-Analysis
This repository contains the lab diary and key results for finding regions of brain activation. 
The lab diary may be too large to open in GitHub and will likely need to be downloaded locally. The project focused on finding regions of brain activation for the Standard Hemodynamic Response Function (HRF). The theoretical data of how it would hypothetically look like was modelled using EEG data convoluted with the HRF. 

Next, the brain fMRI data had to be masked to cancel out the noise (cranium and regions outside of the head) to leave behind only brain pixels. This then gave us a time evolution of each pixel in the brain scan, which was comparable to the experimental fMRI data. The characteristic door knob shape was found, which is believed to be responsible for motor control. This correlated well with the subject in the data have a motor response. 
