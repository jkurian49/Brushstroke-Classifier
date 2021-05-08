# Brushstroke-Classifier

[Brushstroke-Classifier.ipynb](Brushstroke-Classifier.ipynb) implements a neural classifer to determine how brushstrokes were made. During the fabrication of the dataset of brushstrokes, the brush type/material, thickness of paint, and tool path of the CNC machine wielding the brushes were controlled for. [brushstroke_data.csv](brushstroke_data.csv) matches the IDs of the individually-photographed brushstrokes to the labels. 

[Brushstroke-Classifier.ipynb](Brushstroke-Classifier.ipynb) uses a pre-trained VGG-16 model as a feature extractor, with a layer appended at the end to flatten the 3D feature stack and a final dense layer with softmax activation. Due to the limited size of the dataset (288 brushstrokes), separate models are learned for each variable (i.e., 4 models for 4 variables). Lastly, the model predicts labels for the images in [test-images](test-images).
