GOESCloudPredictions is an excursion in applied Machine Learning. It looked to solve one core issue: Improving cloud forecasts and 
interpolating image information between snapshots of the GOES-16 satellite (which occur every 15 minutes)

Files of Interest:
Final Project Report: Technical report on the entirety of the project, its workings, and its findings.
Geostationary Cloud Tracking Spring 2024 - Presentation of the model's findings and decision making rationale
Old: 
    Interim model's report, findings, and other documentation
Data:
    MP4 - Example GIF format of predictions
    PNGs - Processed, masked GOES-16 images to show greyscaled cloud cover. Used directly as input for CNN, ConvLSTM models
Cloud Predictions: 
    Convolution with Separation: Kernel matrix is decomposed into two smaller, one-dimensional vectors 
    through two steps.
    Convolution without Separation: Convlution is performed with full kernel matrix where kernel is 
    simply slided over input images
    Convolutional: Base CNN model application and checkpoints
    Frame Interpolation: Contains framework for CNN-based image interpolation model and checkpoints.
    LSTM Model: Contains the ConvLSTM model which maintained the highest training/testing accuracy. 
Cloud Masking:
    Background subtraction preprocessing code used to visualize GOES images, apply visual bands
    to simulate a cloud cover, contrast clouds from background using background subtraction across
    different times of day, and convert them into PNG format (Data) for CNN/ConvLSTM model input

Contact jonathanjkim5108@gmail.com for any further inquiries, thank you!
    
