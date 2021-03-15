# NLP-Surname-Classification

**Keywords**: Natural Language Processing(NLP), text mining, classification, Multilayer Perceptron(MLP), Convolutional Neural Network(CNN), Recurrent Neural Network(RNN)

The reader may refer to PPT & PDF for complete content, and refer to the same code with results shown on Colab in the following links:
1. Preprocessing: https://bit.ly/3hGWYhs
2. MLP: https://bit.ly/3nTLxpf
3. CNN: https://bit.ly/3rwRCKr
4. RNN: https://bit.ly/3ptfcG8

Figure 1: Rao, D. & McMahan, B. (2019). Natural Language Processing with PyTroch. California, CA: O’Reilly Media.

The code mainly comes from the book Rao, D. & McMahan, B. (2019). Natural Language Processing with PyTroch. California, CA: O'Reilly Media. Based on that, I tuned the model and visualize the outcomes. This article was actually my final project of the course PyTorch and Machine Learning in NCCU.

## (2) Outline
(1) Data Introduction & Data Preprocessing
(2) Neural Networks Tuning Tips
(3) Model Introduction & Baseline Model
(4) MLP
(5) CNN
(6) RNN
(7) Conclusion
(8) Reference



(1) Data Introduction & Data Preprocessing

1. Data Introduction
The surname dataset, a collection of 10,000 surnames from 18 different nationalities collected by the authors from different name sources on the Internet. We split the data into 70% training data, 15% validation data, and 15% test data.

2. Data Preprocessing
First of all, splitting the surname dataset into 70% training data, 15% validation data and 15% test data.
Next, we vectorize the surnames using one-hot encoding. We utilize two variants — “collapsed one-hot vector” and “one-hot matrix.” We use “collapsed one-hot vector” in MLP to save running time, and use “one-hot matrix” in CNN & RNN. In short, “collapsed one-hot vector” doesn’t retain the sequential information and only gives the Boolean values of a character appears or not , whereas “one-hot matrix” records the sequential information.

(2) Neural Networks Tuning Tips
Inspect ML17 for the NN tuning tips.
ML17: Tuning Deep Networks
Activators, optimizers, epochs, mini-batch size, BN, dropout and weight decay
medium.com

(3) Model Introduction & Baseline Model

1. Model Introduction
• Neuron: A minimum unit of neural network.
• Perceptron: A single-layer neural network.
• FNN(feedforward neural network): MLP(multilayer perceptron, also called “fully-connected” network), CNN(convolutional neural network).
• RNN(recurrent neural network): RNN, LSTM(long short-term memory), GRU(gated recurrent unit).

2. Baseline Model
We use the exactly the same models of MLP & CNN retrieved from the book as the baseline models of MLP & CNN respectively. As for RNN, we do the same thing but slight adjust the drop probability from 50% to 0% since 0% yield better performance.

(4) MLP
1. Baseline MLP Model



Figure 2 & 3 & 4: Details of baseline MLP model.
2. Best MLP Model


Figure 5 & 6: Details of the best MLP model.
3. MLP Summary

Figure 7: Summary of MLP models.


(5) CNN
1. Baseline CNN Model



Figure 8 & 9 & 10: Details of baseline CNN model.
2. Best CNN Model



Figure 11 & 12 & 13: Details of the best CNN model.
3. CNN Summary

Figure 14: Summary of CNN models.


(6) RNN
1. Baseline RNN Model



Figure 15 & 16 & 17: Details of baseline RNN model.
2. Best RNN Model



Figure 18 & 19 & 20: Details of the best RNN model.


3. RNN Summary

Figure 21: Summary of RNN models.


(7) Conclusion


Figure 22 & 23: “MLP vs. CNN” & “CNN vs. RNN.”


Figure 24 & 25: “Ensemble Learning” & “Prospect.”


(8) Reference
1. Géron, A. (2019). Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow (2nd ed.). California, CA: O’Reilly Media.
2. Rao, D. & McMahan, B. (2019). Natural Language Processing with PyTroch. California, CA: O’Reilly Media.
3. Sarkar, D. (2019). Text Analytics with Python (2nd ed.). Karnataka, India: Apress.
4. Ganegedara, T. (2018). Natural Language Processing with TensorFlow. Birmingham, UK: Packt Publishing.
5. Subramanian, V. (2018). Deep Learning with PyTorch. Birmingham, UK: Packt Publishing.
6. Patterson, J. & Gibson, A. (2017). Deep Learning: A Practitioner’s Approach. California, CA: O’Reilly Media.
7. 斎藤康毅 (2016). ゼロから作るDeep Learning ―Pythonで学ぶディープラーニングの理論と実. Japan, JP: O’Reilly Japan.
8. Kuo, M. (2021). ML16: Hands-on Text Preprocessing. Retrieved from https://bit.ly/3tsS6Bz

