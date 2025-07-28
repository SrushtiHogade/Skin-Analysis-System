# Skin-Analysis-System
This is a web application that recommends skincare and makeup products based on the user's skin features extracted from a selfie. The system uses Computer Vision techniques and deep learning models to detect:

Skin Tone

Skin Type

Acne Concern Level

Based on these, relevant products are recommended using cosine similarity, prioritizing the ones that match the user's skin profile.

## Working:
1. Image Input
The user is prompted to click a selfie via webcam.

Real-time face detection ensures:

Only one face is visible

Good lighting

Face occupies most of the frame

After capturing, the user is redirected to the next step.

2. form – Skin Info Confirmation
Extracted skin details are prefilled in a form.

The user can modify these values or add more concerns.

Submitting redirects to the recommendations page.

3. recs – Product Recommendations
Top relevant products are shown in card layout.

## Model Architechture:
*Skin Tone Detection*
Skin pixels are extracted using thresholding and color-space filtering (HSV, YCrCb).

A KNN model classifies the mean skin color into tones based on the Fitzpatrick scale.

*Skin Type & Acne Detection*
A CNN model predicts skin type: Dry, Oily, or Normal.

Another CNN classifies acne severity: Low, Moderate, or Severe.

Both models use EfficientNetB0 via transfer learning for better accuracy.

*Product Recommendation*
Each product in the dataset is tagged with suitable skin types, tones, and concerns.

The user’s data is compared against products using cosine similarity.

The top matching products are recommended in different categories.

## Output
Accurate and personalized product suggestions

Clean UI with real-time webcam capture and easy navigation

Backend that processes and classifies facial features automatically

<sub>This project is inspired by publicly available research papers, open-source repositories, and concepts from the fields of computer vision and deep learning. It builds upon these foundational ideas to develop a personalized skincare and makeup recommendation system.</sub>







