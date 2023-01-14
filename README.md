# Atrial Fibrillation Screening App
This is a progressive web-app (PWA) that is designed for individual screening for atrial fibrillation by collecting and analyzing pulse data from finger using the camera of a smartphone.

The intent of this project is to create free tool that can be distributed by health care systems to patients with smartphones. 

Atrial fibrillation is a common heart rhythm that can be asymptomatic, but can increase the risk of stroke. This app could help screen patients to detect asymptomatic atrial fibrillation, allowing treatment to reduce the risk of stroke.

The concept and overall architecture for the app was developed by David T. Linker, M.D. The implementation was developed as a Bioengineering Capstone Project in 2021 by Charlie Bohlin, Matthew Halim and Jeremy Aguirre. 

The atrial fibrillation algorithm is based on algorithms developed by Dr. Linker, ajnd previously covered under US and international patents, which have intentionally been allowed to expire. For a list of the patents, see the the file ALGORITHM.md.

This code is released under the BSD 3-clause license. For details, see the file LICENSE.md

As of now, the app is functional but still has several areas that should be improved on or added prior to deployment. Some of these are simply programming issues, but others require some research. There are several ideas already identified as noted in the To-Do List below.

Also, note that the current code has a feature for development which may or may not be enabled which saves the data to a text file for download. This is for analysis and further development, and should be disabled in a production version.

## To-Do list

### Programming tasks
1. Allow use of main camera rather than selfie camera **Note: selfie camera was chosen because it is easier for users to see the screen with instructions while recording, but main camera may be useful as noted in next point**
2. Allow light on main camera to be illuminated during recording. **Note: Using the light should result in a stronger pulse signal. With the selfie camera, we are dependent on ambient light, and the resulting signal is weaker.**
3. Possibility to send SMS message to a designated facility if AF is detected. **Note: The phone number to send to should probably be hard-coded. The use case is that the app will be downloaded from a health care entity/system, and the number would be known. This would obviate the user needing to known and enter the number.**
4. Include a compressed version of the pulse signal with the SMS message. **Note: Given the slowly changing signal, this can probably be done with a difference signal. Including this will allow someone at the entity to review and determine if the signal is artifact, or possible AF. The feature of downloading the data as text can be used to gather actual data for testing.**
5. User reminders to check pulse periodically
6. Maybe some gamification?

### Research tasks
1. Validation and modification of the AF algorithm for different data sampling frequency
2. Improvement of specificity by using sliding window rather than sequential windows
3. Analysis of errors due to using pulse rather than ECG. There are probably variable phase errors due to an irregular pulse. **Note: This might be studied using data from PhysioNet. If there are records with simultaneous ECG and pulse, any irregularities in the rhythm could be exploited.**
4. If there are significant errors due to using the pulse rather than the ECG, explore ways to mitigate those errors.

Questions/queries:
[Contact](mailto:dtlinker@uw.edu)


