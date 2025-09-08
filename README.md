# PACEM

Personalized ECG Monitoring using Adaptive Transformer
Models

1. Problem Statement

   Heart signals (ECG) vary significantly across individuals due to age, lifestyle, genetics,
   and health conditions. Current AI models for ECG analysis are trained on large
   population-level datasets and identify general patterns of normal and abnormal heart
   rhythms. While these models are effective at detecting common cardiac abnormalities,
   they often fail to capture small, personalized variations in a specific person’s ECG.
   For example, subtle changes in heart rate variability or minor irregularities may indicate
   early stages of arrhythmias or other cardiovascular issues. Population-based models
   may ignore these small but clinically significant changes because they consider them
   within the normal range across the population.
   This project proposes a personalized ECG monitoring system using transformer
   models. The system will first learn general patterns from large-scale ECG datasets and
   then adapt itself to each individual using their own ECG recordings. Over time, the
   model continuously updates its understanding of the person’s normal heart rhythm,
   improving the early detection of anomalies, reducing false alarms, and providing a
   tailored monitoring solution suitable for wearable devices or home monitoring systems.

   Key Challenges Addressed:
   · Detecting subtle individual-specific abnormalities that population models miss.
   · Adapting AI models to continuous, personalized ECG data.
   · Balancing model accuracy with real-time monitoring needs in wearable devices.

2. Dataset

- PTB-XL ECG Dataset – 12-lead ECG recordings from over 20,000 patients;
  publicly available on PhysioNet; suitable for pretraining due to large, diverse data.

- MIT-BIH Arrhythmia Database – Annotated 2-lead ECG recordings for
  arrhythmia detection; publicly available; suitable for personalized model testing.
  Importance: These datasets are publicly accessible, include both normal and abnormal
  heart rhythms, and provide annotations for supervised evaluation.

3. Current State-of-the-Art (SOTA)

   · CNN + LSTM Models: Good for detecting arrhythmias but not personalized.
   · Transformer Models: Capture long-range ECG patterns but mostly
   population-based.
   · Personalized Monitoring Approaches: Emerging research uses fine-tuning on
   individual data, showing improved detection of subtle anomalies.

- CNN-Based Models

  · Strengths: Good at extracting local features in ECG signals; widely used for
  arrhythmia detection.
  · Limitations: Unable to capture long-range dependencies; models are
  population-based, not personalized.

- LSTM-Based Models

  · Strengths: Can model temporal dependencies in ECG sequences; suitable for
  sequential pattern recognition.
  · Limitations: Computationally slower than CNNs; less effective for very long ECG
  recordings; still population-level.

- Transformer-Based Models

  · Strengths: Excellent at capturing long-range dependencies; scalable to large
  datasets; flexible for multi-lead ECGs.
  · Limitations: High memory usage; most current implementations are not
  personalized.

- Personalized Fine-Tuning Approaches

  · Strengths: Improves detection of individual-specific abnormalities; leverages
  pre-trained models for faster adaptation.
  · Limitations: Limited research in ECG; requires continuous personal data collection.
  Limitations: Existing methods rarely combine transformer-based models with
  continuous adaptation for individual monitoring
