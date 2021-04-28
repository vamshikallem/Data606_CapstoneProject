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
The objective of this project is to explore the physiological and neurological signals collected from wearable Sensors and VR headsets in order to understand and predict how they could characterize and explain the cognitive processes involved in the food-related decision making in a Virtual Reality Buffet. Formulate machine learning model like VAR(Vector Auto Regressive Models) and LSTM's to carryout Multivariate Time Series analysis to discriminate event periods using the Neurophysiological features, e.g. resting vs activation, food selection and non-food selection, high-density vs low-density food. Secondary objective is to quantify the complementary and temporal dynamics of physiological signals and neurological signals to inform future experiments and data collection.

DATA:

Collection:
To assess the food decision-making processes in both environments, behavioral assessments and quantitative measurements were adopted, including questionnaires and various sensing modalities such as prefrontal cortex functional near-infrared spectroscopy (fNIRS), electrocardiography (ECG), galvanic skin response (GSR), eye movement and body motion. Neurophysiological measures were captured in both VR and RL phases of the study. Neurological signals from the prefrontal cortex of the brain during food selection were captured using an OCTAMON 8-channel fNIRS device. In the VR setting, participants’ physiological signals, including heart rate (ECG), GSR and position were measured using Shimmer wearable sensors. In both the VR and RL setting, Microsoft band was also used to capture skin temperature, heart rate (PPG), GSR, accelerometer and gyroscope data.  Furthermore, the nutrition density of the food which participants chose in both environments was calculated and categorized into two groups (high and low-density). Then, data processing techniques were developed to identify the neurophysiological variations with different food choices (high/low density) in both environments. There are 15 Participants involved in VR and RW data collection process, which are collected one week apart. 
Explanation and EDA:
There are certain tasks involved to prior and post the data collection process for better understanding of participants state of mind.
1.	Hunger Emotion Rating - to know how hungry the participant is.
2.	Baseline Task - to obtain the baseline of heart rate.
3.	Go / no-Go Task - to practice and instruct the participants about VR setting and Data collection.
4.	Speech Emotion Task - Surprise participants and ask to talk about their strength and weakness, which can help understand their physical and mental state. 
5.	VR and RW food selection task.
6.	Review Questionnaire.

Comprising all of these together we have a TIMESTAMP DATA, recording the start and end times of above events, which helps to data instances from respective interval to analyze particular task.

fNIRS Data (prefrontal cortex functional near-infrared spectroscopy):

To assess the Neurological behavior during food selection in both VR and RW buffet environment, fNIRS sensors are used with two different receivers, 8 different light sources with two different wavelengths measuring the oxygenated, deoxygenated hemoglobin content in the prefrontal cortex of brain.

Most challenging part of this project is preprocessing fNIRS data to obtain a high-quality signal by removing artefacts like,
1. Channel Exclusion - reason of this noise in signal is improper coupling of opt odes to head, instrument and surrounding noise.
2.  Motion artefacts - this is the noise generated by head movements or the body movements.
3. Physiological artefacts - these are generated by Cerebral signals or Skin Hemodynamics.

 
 
We are yet to implement these preprocessing methodologies on this fNIRS data, exploring those tools and software's available. After spending most my time in research for the optimal methods to apply to obtain a best quality signal we have decided to use Wavelet Filtering to avoid Motion artefacts and SQI (Signal Quality Indexing) to eliminate Channel exclusion and Physiological artefacts.

Shimmer's Data (Physiological Data):
To analyze the physiological behavior, they have used Shimmer's sensors and Microsoft band to detect the motion using Accelerometer, GSR (Galvanic Skin Response) to sense skin gland activity, ECG (Electrocardiography) to know the heart rate and Gyroscope to sense movement.

 

Methodology:
1. Understand Data Collection procedures and Data Formatting.
2. Data preprocessing to extract High Quality Signals.
3. Feature Extraction to create Metadata required to formulate ML models.
4. Automate pre-processing for whole data.
5. Feature based modeling to discriminate events.
