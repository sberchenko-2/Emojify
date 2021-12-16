# Emojify

-- video --

# Abstract


# Problem Statement
Emojis or avatars are ways to indicate nonverbal cues. These cues have become an essential part of online chatting, product review, brand emotion, and many more. It also lead to increasing data science research dedicated to emoji-driven storytelling.

With advancements in computer vision and deep learning, it is now possible to detect human emotions from images. In this deep learning project, we will classify human facial expressions to filter and map corresponding emojis or avatars.

# Dataset
The FER2013 dataset ( facial expression recognition) consists of 48*48 pixel grayscale face images. The images are centered and occupy an equal amount of space. This dataset consist of facial emotions of following categories:

0:angry
1:disgust
2:feat
3:happy
4:sad
5:surprise
6:natural

[Facial Expression Recognition Dataset](https://www.kaggle.com/msambare/fer2013?)

HUMAN ACCURACY: 65% - 68%

# Related Work
https://yagnikbavishi004.medium.com/emojify-using-face-recognition-with-machine-learning-b6b6f8f339c4
https://github.com/angelvillar96/FaceEmoji
https://arxiv.org/ftp/arxiv/papers/2105/2105.03588.pdf

# Methodology
CNN

# Experiments / Evaluation
So much pain to get working 
huge minimum at 25% which kept getting stuck at
had big problem with overfitting: 
    train-loss: 0.6977
    test-loss: 2.4902
fixed overfitting by introducing lots of noise with data augmentation
fixed minimum by changing network structure and raising learning rate

changed network structure numerous times, eventually got best results with variation of VGG + paper
evaluation - bit of overfitting


# Results

improve: more noise, better network + training

# Examples

