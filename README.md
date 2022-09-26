# Deep_Learning_Notebook_Modelling
This is a short how-to about building and using a convolution neural network (CNN) deep learning model through Jupyter notebooks. The model is to be trained with the well known Fashion MNIST dataset to classify clothing images into the designated categories.
<p>
  1. Build, evaluate or tweak a CNN model on Google Colab <br>
  2. Use the model on a Jupyter container of a prebaked docker image.
 
### 1. Build the model on Colab
  <p>
    (a) Assume you have a Google gmail account to start with in order to use Colab and Google Drive. 
  <p>
    (b) Load a model builder notebook into Colab. I have already created a notebook named Build_CNN_Fashion_Colab.ipynb and shared it via this link, https://colab.research.google.com/drive/1A4wf415wuLsrUOi9jgIGw7X9dcCLFZhz?usp=sharing. Just open this link to refer to the notebook.
  <p>
    (c) You are advised to make a copy of the notebook before running through its code cells on Colab. Meanwhile, you may want to upload a sample clothing image to the Google drive. For example, download https://github.com/snpsuen/Deep_Learning_Notebook_Modelling/raw/main/input/fashion_example01.jpg from my Github repo and upload it to your Google drive. Please note that the notebook maps Google Drive root to "/content/drive/My Drive".
  <p>
    (d) Run the notebook by going through each code cell except the last one, until you are satisifed with the prediction or observe an accuracy > 0.9. You may tweak the model by add one or more Conv2d layers like Conv2d(128, (3,3), ...) or increasing the number of epochs or batch size.
  <p>
    (e) Run the last code cell of the notebook to save the model to a folder named "CNN_Fashion_Colab_Model01" at the root of your Google Drive.
  <p>
    (f) Finally, copy out and zip up the model folder, upload the zip file to your Google Drive. The model will be transfered as a zip file to a Jupyter container in Phase 2.
  
### 2. Use the model in a Jupyter container
  <p>
    (a) I have pre-baked a suitable jupyter-tensorflow docker image that comes with all the necessary packages for running the CNN model. It is ready to be pulled as snpsuen/jupyter-tensorflow-opencv:v04 from hub.docker.com.
  <p>
    (b) Run a Jupyter container on snpsuen/jupyter-tensorflow-opencv:v04 in a Linux host.
    ~~~
    docker run -it --name jtnotebook-container -p 8888:8888 snpsuen/jupyter-tensorflow-opencv:v04
    ~~~
  <p>
    (c) Open http://<linux-host>:8888 or a port-forwarding URL like http://localhost:8888, to connect to a Jupyter note book server. Login with the randomly given token number, e.g. http://127.0.0.1:8888/lab?token=36e45f566dda06cc50aae6eabea14c8a612e09f9b17d2277
    
    
