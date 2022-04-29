# Chest cancer classifier
>It was a project about chest cancer detection using machine learning and deep leaning (CNN) .
we classify and diagnose if the patient have cancer or not using AI model .
We give them the information about the type of cancer and the way of treatment.
we tried to collect all data we need to make the model classify the images easily.
so i had to fetch data from many resources to start the project .
I researched a lot to collect all the data from many resources and cleaned it for the CNN \
**MOHAMED HANY**
</br>
<h4>Our goal in this project is to build a robust classifier that can predict the type of the tumor</h4>
<h1>Dataset</h1>
<img src="https://user-images.githubusercontent.com/46766351/165880858-6e2708b1-2e03-415b-945c-266b1a967055.png"></img>
Data contain 3 chest cancer types :
<ul>
  <li>Adenocarcinoma</li>
  <li>Large cell carcinoma</li>
  <li>Squamous cell carcinoma</li>
</ul>
<p>database is available on <a href="https://www.kaggle.com/code/vincentsiow/chest-ct-scan-using-resnet101v2/data">Kaggle</a></p>
<p>API command</p>

```
kaggle datasets download -d mohamedhanyyy/chest-ctscan-images
```

<h1>Model</h1>

<p>for this classification task we will use the Xception model developed by François Chollet</p>

>This idea behind the Inception module is to make this
process easier and more efficient by explicitly factoring it
into a series of operations that would independently look at
cross-channel correlations and at spatial correlations.
We propose a convolutional neural network architecture
based entirely on depthwise separable convolution layers.
In effect, we make the following hypothesis: that the mapping of cross-channels correlations and spatial correlations
in the feature maps of convolutional neural networks can be
entirely decoupled. Because this hypothesis is a stronger version of the hypothesis underlying the Inception architecture,
we name our proposed architecture Xception, which stands
for “Extreme Inception”.

<p>learn more : <a href="https://arxiv.org/pdf/1610.02357v3.pdf">Paper</a></p>

<p>the architecture of the Xception model is given as</p>
<img src="https://production-media.paperswithcode.com/models/xception.png"></img>

<h1>Evaluation of the model</h1>

| epochs      | batch size | accuracy on training | accuracy on test  |
| :----:        |    :----:   |    :----:   |         :----:  |
| 12   | 32        | 0.9918      |0.8539|

<h1>use the model</h1>

<ol>
  <li>
    <p>
      clone the repository
    </p>
  
  ```
    git clone https://github.com/mohamed-yassine-benkhadda/chest_cancer.git
  ```
  </li>
  <li>
    <p>
      load the model in a python file
    </p>
  
  ```
    from tensorflow import keras
    model = keras.models.load_model('model.h5')
  ```
  </li>
  <li>
    <p>
      enjoy the model
    </p>
  
  ```
    result = model.predict(X)
  ```
  </li>
</ol>
