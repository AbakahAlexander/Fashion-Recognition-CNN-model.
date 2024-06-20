# 🧥 Fashion-Recognition-CNN-model
A multilayer feedforward neural network model is built using Keras.

# 📊 Dataset
The Fashion MNIST dataset is a large collection of Zalando's article images intended as a more challenging drop-in replacement for the original MNIST dataset. It consists of 70,000 grayscale images of 28x28 pixels each, split into 60,000 training and 10,000 testing samples. Each image depicts one of ten fashion categories, such as T-shirts, trousers, and sneakers, labeled from 0 to 9. The dataset is widely used for benchmarking machine learning algorithms in image classification tasks due to its complexity compared to the digit-based MNIST, providing a more realistic scenario for real-world applications.

[Link to dataset](https://github.com/zalandoresearch/fashion-mnist)

# 🛠️ Methodology:
* Import libraries and dataset.
* Preprocess data.
* Build, train, and evaluate CNN model without dropout.
* Build, train, and evaluate CNN model with dropout.
* Make predictions.
* Save model.

# 📝 Summary of CNN model without dropout
It begins with three convolutional layers, each followed by a LeakyReLU activation function and max pooling layers. The first convolutional layer has 32 filters, the second has 64, and the third has 128, all with 3x3 kernels and 'same' padding. After flattening the output from the convolutional layers, the model has a dense layer with 128 units and a LeakyReLU activation. The final layer is a dense output layer with softmax activation, suitable for multi-class classification, where `nclasses` represents the number of output classes.

![Screenshot 2024-06-20 040213](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/8f28efa9-5bcc-420f-9f5e-fe5d7001ed4a)

# 📈 Accuracy
This resulted in training accuracy of 0.9896 and validation accuracy of 0.9210.

![Screenshot 2024-06-20 041931](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/9b1fbf00-a7f8-4dc0-92d3-586828af90cc)

# 📉 Loss
This resulted in a training loss of 0.0272 and validation loss of 0.4804.

![Screenshot 2024-06-20 042146](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/95ac1ad6-c956-4837-bf4b-489bcfadccbd)

# 📝 Summary of CNN model with dropout
This model includes Dropout layers after each MaxPooling layer and before the final Dense layer to reduce overfitting. Dropout rates are 0.25, 0.25, 0.4, and 0.3, adding regularization compared to the earlier model.

![Screenshot 2024-06-20 042355](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/59470d3c-4f2d-482c-9ad6-4e320d996fb6)

# 📈 Accuracy
This resulted in training accuracy of 0.9243 and validation accuracy of 0.9252.

![Screenshot 2024-06-20 042620](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/63a6573d-918d-4cc0-b11b-a95ec82b5a14)

# 📉 Loss
This resulted in a training loss of 0.2005 and validation loss of 0.2055.

# 📝 Classification report

![Screenshot 2024-06-20 042836](https://github.com/AbakahAlexander/Fashion-Recognition-CNN-model./assets/107807886/07c49638-51d1-43ea-97b3-205df7870814)

# 🔚 Conclusion
It was observed that the accuracy and loss values of the second model weren't significantly better than the first. However, the training and validation values in the second model had stronger correlation, indicating better learning in the second model.
