# Driver Gaze Detection in Static and Moving Vehicles

## Overview
Driver Gaze Detection in Static and Moving Vehicles is my Undergraduate project aimed at developing a comprehensive system for monitoring and analyzing driver gaze behavior in varying driving conditions. The project utilizes the Pupil Invisible Eye tracker device in conjunction with installed cameras to capture eye movements and head positions of drivers within vehicles. The primary objective is to differentiate between driver gaze patterns in static environments and while driving.

## Objective
The main goal of this project is to enhance the understanding of driver gaze behavior and its implications in different driving conditions. Specifically, the project aims to:

- Develop algorithms for detecting and tracking driver gaze movements across designated windshield zones.
- Compare and analyze driver gaze patterns between static and driving scenarios.
- Evaluate the effectiveness and accuracy of the gaze detection system through rigorous testing and validation processes.
- Explore potential applications for improving the safety and efficiency of autonomous vehicles, driver fatigue detection systems and human-computer interaction interfaces.

## Key Components
### Hardware
- Pupil Invisible Eye tracker device
- Cameras installed within the vehicle for head position tracking

### Software and Libraries
- Python: Programming language used for algorithm development and implementation
- OpenCV: Library for image processing and computer vision tasks
- Tools: Jupyter Notebook and Google Colab
<!-- - TensorFlow: Deep learning framework for advanced feature extraction and classification -->
<!-- - Matplotlib and Plotly: Libraries for data visualization and analysis -->
- Various machine learning and statistical analysis tools for model evaluation and validation

## Technical Details
- Iris region detection and positional tracking algorithms implemented using OpenCV.
- Utilization of ground truth comparisons and manual annotations for model validation and refinement.
- Integration of machine learning algorithms for real-time analysis of driver gaze behavior.
<!-- - Development of a user-friendly interface for data visualization and analysis using Matplotlib and Plotly. -->
- Continuous improvement of model accuracy through data augmentation techniques and algorithmic enhancements.

## Implementation:
- I used the data of 11 participants and extracted the portion of the video from timestamp 3 minutes to 5 minutes for analysis. 
- Each video segment comprised approximately 24,000 frames for both the left and right eyes. 
- The frames needed to be extracted with their exact frame number, so that they could later be matched with the ground truth. Done using the frame_extraction.ipynb
- Based on the World View camera, there were different classes of zones allotted to the frames of the video. Now, the challenge with this was that the world view camera was recording at 25fps, while the eye cameras recorded at almost 200fps.
- I used the world-view of the participants, extracted the 2min part from their videos and got the frame IDs of the frames in there.
- Next, I merged the data of the ground truth annotation based on the world-view camera and assigned the zone class for each of those frames from the world-view.
- Now, the world view camera is recorded in a different frame rate than the left and right eye cameras, so I used the class zones from the world-view camera and assigned the respective zones to the frames of the eye cameras. This was done using linear interpolation. The code is given in the frame_extraction file.

## Conclusion:
- Detailed analysis of iris detection accuracy rates for left and right eyes across 11 participants, with accuracy rates ranging from 20% to 93%.
- Based on these results, 7 out of 11 participants’ data have very high accuracy and this shows how different people have different outlooks while driving.
- A lot of the false detection were majorly during the time of blinking, and lower accuracy implies higher blinking time, which might hinder the safe driving environment, which could be taken care of by the automation of the vehicles.

<!-- ## Usage
To use the Driver Gaze Detection system:
1. Install the required dependencies using the provided `requirements.txt` file.
2. Connect the Pupil Invisible Eye tracker device and ensure proper camera calibration.
3. Run the main Python script to start the gaze detection system.
4. Follow the instructions for data collection and analysis provided in the documentation. -->

## Contributions and Feedback
Contributions to the project are welcome via pull requests. For feedback, questions, or suggestions, please open an issue on the GitHub repository.

<!-- ## License -->
<!-- This project is licensed under the MIT License. See the LICENSE file for details. -->
