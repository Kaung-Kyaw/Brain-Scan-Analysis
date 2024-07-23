# Brain-Scan-Analysis
This repository contains the lab diary and key results for finding regions of brain activation. 
The lab diary may be too large to open in GitHub and will likely need to be downloaded locally. The project focused on finding regions of brain activation for the Standard Hemodynamic Response Function (HRF). The theoretical data of how it would hypothetically look like was modelled using EEG data convoluted with the HRF. 

Next, the brain fMRI data had to be masked to cancel out the noise (cranium and regions outside of the head) to leave behind only brain pixels. This then gave us a time evolution of each pixel in the brain scan, which was comparable to the experimental fMRI data. The characteristic door knob shape was found, which is believed to be responsible for motor control. This correlated well with the subject in the data have a motor response. 

\newline
Sections: [Modelling Theoretical Data - EEG](#EEG-Data-Boxcars), [Modelling Theoretical Data - Convolution](#Convolution-of-EEG-with-the-Hemodynamic-Response-Function), [Masking to Clean fMRI Data](#Cleaning-fMRI-data), [Results](#Regions-of-Brain-Activation)

## Modelling Theoretical Data 
### EEG Data Boxcars
Firstly, we needed to model the theoretical data of how the HRF would look like if it is indeed associated with the stimulus response. The EEG data would be associated with the stimulus response in the brain as it shows when the action is being performed. The response can be seen as a time of activation, duration then deactivation, resulting in box cars. 

|![12123 Boxcar 1th element Duration](https://github.com/user-attachments/assets/aaa5c000-2c45-4e93-a271-61844ae3a54d)|
|:--:|
|Box car of the 1st element duration alone for a subject|


|![image](https://github.com/user-attachments/assets/445246bd-ddec-4e18-a124-184b420be16a)|
|:--:|
|Box cars of the whole stumulus responses for a subject|

### Convolution of EEG with the Hemodynamic Response Function 
The hypothetical function for a stimulus response has been proposed as the Hemodynamic Response Function (HRF). This can now be convoluted with the EEG to visualise how the function would look like if it is actually associated with the stimulus response.

|![image](https://github.com/user-attachments/assets/03f3938f-dfdb-4672-a153-8259097300d8)|
|:--:|
|The Standard Hemodynamic Response Function|

|![image](https://github.com/user-attachments/assets/200bfd17-6b20-4b3a-863d-e9e8f9c8f728)|
|:--:|
|Regressor of the HRF convoluted with the HRF|

The HRF has a peak that goes above baseline, and a trough (post-stimulus dip) that goes below baseline. The project explored correlation with both aspects of this property. 

## Cleaning fMRI data
There is a bad signal to noise ratio for the fMRI data. This led to the cranium and other regions being included in the image, when it should not be there. This needed to be cleaned up by masking the rows and columns of the voxels - leaving behind only slices of the brain. Each slice of the brain contains in total 294 instances in time with 3 second intervals, this will be useful for using each pixel as a time series for comparison later on. 

|![image](https://github.com/user-attachments/assets/7cd38314-e91c-457d-ab99-f5efc07e1618)|
|:--:|
|Brain Image|

|![image](https://github.com/user-attachments/assets/90300c3f-3b3f-4c86-800a-2bd26894dbdd)|
|:--:|
|12 Slices of the brain showing the regions of the brain from top to bottom (left to right)|


|![image](https://github.com/user-attachments/assets/eef0cd05-3e73-4c29-9403-c7faf15721df)|
|:--:|
|Masked Image of the brain for improving signal to noise|


## Regions of Brain Activation
The experimental fMRI data can then be correlated with the regressor as given above. This will show regions of brain activations with the HRF associated to the stimulus response. 
|![image](https://github.com/user-attachments/assets/d232cea5-3803-4ed7-8577-c754d55699bb)|
|:--:|
|Correlation for showing regions of activation for HRF truncated for post-stimulus dip| 

|![image](https://github.com/user-attachments/assets/85164553-d14a-4bb2-bb62-0ee88c2fbead)|
|:--:|
|12 Slices of the brain showing regions of correlation with the standard HRF|


There is a characteristic doorknob shape, believed to be associated with motor control, and the brain is predominantly active on the left-hand side from analysing the images. Since subject was performing motor activities with the hand throughout the experiment, it is in agreement with what we are witnessing! 



