# Driver-Gaze-Analysis
This is my Under Graduate Project under the mentorship of Dr. Pranamesh Chakraborty. The aim of the project is to analyze driver gaze in different static and dynamic scenarios using the Pupil Invisible Eye Tracker. The eye and head parameters are observed and their data is studied to provide the different aspects of driver behaviour that are important for the improvement of transportation engineering and automated vehicles. 

# Eye parameters
1. While driving, a comprehensive set of features are extracted from eye data, including pupil and iris information, eye movement types and gaze estimation.
2. The coordinates of the pupil centre are detected to know the position of the eyes with respect to their direction of gaze, provided by the eye tracker.
3. The detection of various eye parameters such as pupil, iris and eyelid is done using small DNNs with maximum connections and tensor normalization. Techniques like landmark validation and batch balancing are used to ensure accuracy and robustness in feature detection.