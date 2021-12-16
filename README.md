# Emojify

TODO: -- video --

# Abstract
Emojis are images and icons which allow us to express nonverbal emotions. They have become an integral part of online messaging, chatting, product review, brand expression, and more. However, emoji-driven storytelling has still remained a relatively unexplored portion of data science research, despite the numerous applications. With advancements in computer vision and deep learning, we are increasing our abilities to detect human emotions from images. In this project, I detect and classify human facial expressions in order to map them to corresponding emojis. This then allows facial expressions to be replaced by their corrosponding emojis in real time. 

# Dataset
This project was built based on the [FER-2013 dataset](https://www.kaggle.com/msambare/fer2013?). This dataset consists of 35,888 images, each of which is a 48 x 48 grayscale face. The images are all centered and the faces occupy a roughly equal amount of space. The images are then mapped to 7 distinct classes representing the portrayed emotions:

- angry
- disgust
- feat
- happy
- sad
- surprise
- natural

An important factor to note about this dataset is that its very hard - the average human accuracy is only 65.5%. Part of this is due to the 1-channel nature of the data since the loss of color makes it harder to determine certain emotions (such as the lack of reddening for anger). Additionally, the dataset suffers from a lack of noise which leads to high levels of overfitting. Both these factors and others were difficult obstacles that I had to overcome during my project.

# Related Work
Although there has been a lot of various work and research done on emotion detection, there wasn't much in place for a full pipeline of emotion detection to emoji selection. Although I did find some sources such as [FaceEmoji](https://github.com/angelvillar96/FaceEmoji
)) and [Facial-Emoji-Recognition](https://yagnikbavishi004.medium.com/emojify-using-face-recognition-with-machine-learning-b6b6f8f339c4
)) which I took inspiration from, most of the end design was of my own construction.

I did also look into different models and designs for overall emotion detection on FER-2013. In particular, I took most of my design's inspiration from [this paper](https://arxiv.org/ftp/arxiv/papers/2105/2105.03588.pdf
), which trained a variation of VGGNet with various optimization methods to achieve a 73.28% accuracy on the dataset.


# Methodology
Started with basic CNN model, had trouble with breaching 25%. Experimented a long time with different designs without any success. Finally did more research, found above paper, adopted similar VGG structure. Slightly better, but still huge variations in training. Added much noise into dataset, finally started seeing some success. Tuned hyperparameters (weight decay, momentum, learning rate) to get better results. Biggest issue - training time. For complex issue, needed big network to solve but that meant long training time. Paper ran for 300 epochs, but it would take me almost 3 hours just to run 100. Also had issues with overfitting had to fight (by introducing more noise). To get better results - more noise (less overfitting) + lower lr (had to have a bit too high in order to train faster) + more training time / better compute resources.

huge minimum at 25% which kept getting stuck at
had big problem with overfitting: 
    train-loss: 0.6977
    test-loss: 2.4902
fixed overfitting by introducing lots of noise with data augmentation
fixed minimum by changing network structure and raising learning rate

changed network structure numerous times, eventually got best results with variation of VGG + paper
training very very slow, paper ran for 300 epochs but took me almost 3 hours to run 100


# Experiments / Evaluation
Evaluate test accuracy against paper (VGG) and human accuracy
End accuracy - 54%. Seems kinda bad, but human accuracy only 65%, current ML best is 73.28%.


evaluation - bit of overfitting
improve: more noise, better network + training


# Results

Pretty good, hooked up with real time detection.

# Examples

