# Analomy-detection-in-steel-bearings
This Project is done as a part of IBM Applied AI with Deep Learning

To have a simple framework for creating data, I’ve written a test data simulator, which is part of a bigger time series and machine learning toolkit.

This simulator generates data from sampling various physical models, and you can decide on the degree of noise and switch between different states (healthy and broken) of the physical model for anomaly detection and classification tasks.

For now, I’ve implemented the Lorenz Attractor model. This is a very simple, but still very interesting, physical model. Lorenz was one of the pioneers of chaos theory and he was able to show that a very simple model that consists of just three equations and four model parameters can create a chaotic system that is highly sensitive to initial conditions and that also oscillates between multiple semi-stable states where state transitions are very hard to predict.

I’m using Node-RED as the runtime platform for the simulator because it is a very fast way of implementing data-centric applications. Node-RED is open source and runs entirely on Node.js. If you want to learn more on Node-RED, check out this excellent tutorial.

Because the data simulator is completely implemented as a Node-RED flow, we can use Node-RED from the IoT Starter Boilerplate on the IBM Cloud. Of course, the data simulator can run on any Node-RED instance, even on a Raspberry Pi, where it can be used to simulate sensor data on the edge.

Creating the test data simulator

While it was challenging to create the test data simulator, you can get the simulator up and running in four main steps:

    -Deploy the Node-RED IoT Starter boilerplate to the IBM Cloud.
    -Deploy the test data simulator flow.
    -Test the test data simulator.
    -Get the IBM Watson IoT Platform credentials to consume the data using MQTT from any place in the world.
    -Create an IBM Cloud app using the Internet of Things Platform Starter. If you are not logged in to IBM Cloud, log in.
    -Name your application a unique name, and click Create. 
    -In the left menu, click Connections.
    -On the Internet of Things Platform tile, click View credentials.
    -Write down the values of the following properties as you need them later when you work with one of the three technologies (DeepLearning4j, ApacheSystemML, and TensorFlow (TensorSpark)): org apiKey apiToken
    -Click Close.
    -Wait until your application is running, and then click Visit App URL. 
    -Before you can access and open your Node-RED flow editor, you must secure your Node-RED editor. a. Click Next. b. Set a user name a password.
    -Click Go to your Node-RED flow editor. 
    -Log in with the user name and password you’ve just created.
    -Using your mouse, select all the nodes in Flow 1; click the Delete key to empty it. 
    -From the upper-right menu, click Import > Clipboard.
    -Open this simulatorflow.json file in my GitHub repo; copy the JSON object to the clipboard.
    -On the Import nodes window, paste the JSON object to the text field, and click Import. 
    -Click Deploy. The message “Successfully deployed” will display.
    -The debug tab displays the generated messages. Congratulations! Your Test Data Generator is working.
    
i have mentioned a brief view of how to create Data Generator Using Node Red.
refer to (https://developer.ibm.com/tutorials/iot-deep-learning-anomaly-detection-2/) for detailed article 

we will use an ordinary feed-forward network. So we need to do some pre-processing of this time series data

A widely-used method in traditional data science and signal processing is called Discrete Fourier Transformation. This algorithm transforms from the time to the frequency domain, or in other words, it returns the frequency spectrum of the signals.

The most widely used implementation of the transformation is called FFT, which stands for Fast Fourier Transformation, 

