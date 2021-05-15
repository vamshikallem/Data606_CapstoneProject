# Data606_CapstoneProject

# Understanding Physiological and Neurological Fingerprint for Decision Making with Food Choices in Virtual Reality Environment 

INTRODUCTION:
 The emergence of dysfunctional eating behavior and eating disorders starts in adolescence and young adulthood. Epidemiological studies has revealed a strong association between disordered eating behavior (e.g., binge eating), overweight and obesity-related health consequences. This weight gain is observed most during the age of transition to college, where young adults have more independent food and diet-related decisions. In the United States, 30% of individuals seeking weight loss treatment suffer from binge eating disorder (BED), which occurs in over 40% of obese individuals with a body mass index (BMI) > 34. Thus, there is a need to examine food and eating related processes during this developmental period among students attending college and ultimately developing effective treatment for individuals with eating disorders. 
 
PREVIOUS WORK:
 This Project is an advancement of pre-existing projects on Validation of Virtual Reality Buffet Environment and Neurophysiological Variations in Food Decision Making within Virtual and Real Environments from the departments of Psychology and Information Systems at UMBC. 
Validation of a Virtual Reality Buffet environment to assess food selection processes among emerging adults: 
Primary aim of the above study was to assess convergent validity by examining the correlations between the nutritional content of participants food selections in the VR buffet and their RW food buffet selection (in Kcals, grams, fat, carbohydrates, protein) one-week apart. The second aim was to assess user experience in the VR environment. Specifically, examined participants’ perceptions of the VR buffet in terms of: (a) how natural was their overall experience in the VR buffet; (b) how much their final selection in the VR buffet represented a lunch that they would select and eat/drink on an average day; and (c) how much their final selection represented the lunch that they would select and eat/drink if the same food selection were available. 
   
Findings demonstrated the validity and acceptability of a highly immersive and realistic VR buffet for assessing food selection that is generalizable to RW food settings. 
Neurophysiological Variations in Food Decision Making within Virtual and Real Environments: 
This research presents a pilot study to achieve a long-term goal by designing and developing experimental environments, protocols and methods to examine the multifactorial neurophysiological correlates of food decision-making behavior, with potential implications for the development of effective treatments for individuals with dysfunctional eating. The experimental protocol was designed in a virtual reality (VR) and real-life (RL) buffet setting. The main aim was to identify what are the neurophysiological correlates of food decision-making behaviors within the VR and the RL buffet setting? How consistent are individuals’ food decision-making processes in the VR setting and the RL buffet setting? 
Findings revealed that the left inferior frontal gyrus demonstrated significant differential activation when subjects chose high compared to low density food in both settings. These findings suggest that VR simulations may provide similar neural responses to real world environments, particularly in control regions of the brain. 

AIM:
The objective of this project is to explore the physiological signals collected from wearable Sensors and VR headsets in order to understand and predict how they could characterize and explain the cognitive processes involved in the food-related decision making in a Virtual Reality Buffet. Formulate machine learning model Time Series analysis to discriminate event periods using the Neurophysiological features, e.g. resting vs activation, food selection and non-food selection, high-density vs low-density food. Secondary objective is to quantify the complementary and temporal dynamics of physiological signals to inform future experiments and data collection.

DATA:

Collection:
To assess the food decision-making processes in both environments, behavioral assessments and quantitative measurements were adopted, including questionnaires and various sensing modalities such as electrocardiography (ECG), galvanic skin response (GSR), eye movement and body motion. Neurophysiological measures were captured in both VR and RL phases of the study. In the VR setting, participants’ physiological signals, including heart rate (ECG), GSR and position were measured using Shimmer wearable sensors. In both the VR and RL setting, Microsoft band was also used to capture skin temperature, heart rate (PPG), GSR, accelerometer and gyroscope data.  Furthermore, the nutrition density of the food which participants chose in both environments was calculated and categorized into two groups (high and low-density). Then, data processing techniques were developed to identify the neurophysiological variations with different food choices (high/low density) in both environments. There are 15 Participants involved in VR and RW data collection process, which are collected one week apart. 
Explanation and EDA:
There are certain tasks involved to prior and post the data collection process for better understanding of participants state of mind.
1.	Hunger Emotion Rating - to know how hungry the participant is.
2.	Baseline Task - to obtain the baseline of heart rate.
3.	Go / no-Go Task - to practice and instruct the participants about VR setting and Data collection.
4.	Speech Emotion Task - Surprise participants and ask to talk about their strength and weakness, which can help understand their physical and mental state. 
5.	VR and RW food selection task.
6.	Review Questionnaire.

Comprising all of these together we have a TIMESTAMP DATA, recording the start and end times of above events, which helps to data instances from respective interval to analyze particular task.

Shimmer's Data (Physiological Data):
To analyze the physiological behavior, they have used Shimmer's sensors and Microsoft band to detect the motion using Accelerometer, GSR (Galvanic Skin Response) to sense skin gland activity, ECG (Electrocardiography) to know the heart rate and Gyroscope to sense movement.

I have worked on two different types of Physiological data collected using shimmer device. 
1. GSR Data (Galvanic Skin Response) measures the skin conductance of sweat gland activity
2. ECG Data (Eclectro Cardio Graph) helps to measure the heart rate variability 

Our goal here is to understand Stress Indicating Factors (GSR&ECG) and discriminate each event period using the features extracted from GSR & ECG:

Below is the Image representing three different event periods namely VR Baseline, Speech Emotion and Food Selection on a sample GSR signal.
![](Images/Image%20representing%20event%20periods.PNG)


GSR or Electrodermal Activity:
GSR is used to measure sweat gland activity related to emotional arousal, it refers to variation of electric conductance of the skin in response to skin secretion. 

Two major components of GSR signal are:

Skin Conductance Response (SCR): Also called the Phasic component, it refers to the number of sweat glands that are activated. SCRs are faster in their appearance and takes longer to decline to baseline, which means that another SCR occurs shortly one after another resulting in an overall increase in GSR activity. This cumulative effect leads to the underestimation of SCR amplitude.

The Rapid rise and asymptomatic exponential decay are the main characteristics of this signal and the overlap issue is the main problem in the decomposition of these signals.

a. SCR occurs in response to a stimulus which is an event.

b. NS-SCR- non-specific SCR occurs without any specific reason.

Skin Conductance Level (SCL): Also called the Tonic component, is a slowly changing and continuous signal. Slow drifts in baseline and spontaneous fluctuations are the characters of this signal.

Below is the image discriminating raw GSR signal and its Phasic and Tonic components.
![](Images/Phasic%20and%20Tonic%20Components%20on%20GSR%20signal.PNG)
