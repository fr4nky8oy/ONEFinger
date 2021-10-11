 The ONE-Finger is a feature extractor inspired by the simplicity of the iOS and Android finger-based interaction system used with iOS and Android portable handsets and tablets. It also takes inspiration from Björk - Reactable instrument: 
https://www.youtube.com/watch?v=Ni_x_74VKU0&ab_channel=OfficialDeathCubeK 
 
ONE-Finger turns your handset or tablet screen into a gestural-based interactive controller. 
It can extract the following features as continuous values/data: x and y finger position, x and y fingers velocity and overall acceleration. 
 
It is an ideal feature extractor for a regression-type training model, and it could be used for a variety of applications; to control multiple parameters of a virtual-synthesiser at once, as a game controller in Unity or Unreal, as a user-input device to control an interactive art installation, as 3D audio panner for object based audio applications or as lighting remote for live shows such as concerts or theatre's plays. 
 
It uses the open-source TUIO 1.1 protocol: https://www.tuio.org/
This means that it could be expanded/modified to accommodate multi-touch features if required (and also used for Class-type models). Please see http://www.tuio.org/? here if you would like to modify and implement more features to the Max/MSP app.
 
------------------------- Dependancies ---------- Before you start using the One-Finger ----------------------
 
ONE-Finger is built in Max/MSP. It receives Open Sound Control(OSC) messages as continues controls values from the TUIOPad app installed on the handset or tablet device and send them to Wekinator.
 
a.Ensure that the CNMAT Externals by CNMAT are installed in Max/MSP. 
This package contains the necessary OSC objects used within the ONE-Finger app.
https://cnmat.berkeley.edu/downloads
 
b.The TUIOPad app must be installed on the handset or tablet used as the interactive controller. 
This app is free to download directly from the iOS or Android app stores. 

iOS : https://apps.apple.com/us/app/tuiopad/id412446962
Android : https://baixarapk.gratis/en/app/412446962/tuiopad
 
Make sure that the above-mentioned dependencies are installed. 
Without the Max/MSP externals and the TUIOPad app installed the ONE-FINGER won't work.
 
---------------------- Using the One-Finger -----------------------------
 
1.Lunch the TUIOPad app from your handset or tablet. 
 
a.Connect to the host by typing the local IP address. If you don't know how to find your IP address see this:
MAC: https://www.youtube.com/watch?v=IZE548Dp4HA&ab_channel=MattHorner
WINDOWS : https://www.youtube.com/watch?v=PZtbGoTaN3E&ab_channel=How-ToDesktop
b. set the port to 3333
c. set the prefered view (landscape is advised)
d. switch off periodic state, full bandle and additional messages tabs (when the white dots are on the left it means they are off)
e. press starts and interacts with the screen using your finger
f. a shake gesture will get you back to the option page
 
2. Lunch the ONE-Finger Max/MSP app and monitor the incoming messages arriving from the TUIOPad app:
s_id (finger is touching the screen- message received) 
x_Finger position values
y_Finger position values
x_Finger velocity values
y_Finger velocity values
m_Accelleration values
 a. If you do not see any messages arriving in the Max/MSP app, go back to point 1 (instructions on this paragraph). Make sure that you are connected to the correct IP address and you have set port 3333. 
 
3. Launch Wekinator 

a.set the OSC receiving port to 6448
b.within the inputs section set the OSC messages to /wek/inputs and inputs to 5.
c.within the output section set the OSC messages to /wek/outputs, Host to localhost, set the output port to 12000, choose type* All Continuous 
d. click next
e. train and run your model when you are ready*
 
*The ONE-Finger was tested using continuous controllers and the K-n algorithm to build a model capable of controlling up to 13 parameters of audio-reactive wavetable synth:  
https://youtu.be/cWyYZ0Bbz6w 
 
 HAVE FUN!
 
 

