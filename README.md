# Video Doorbell, Lab 7

*A lab report by John Q. Student*

### In This Report

1. Upload a video of your version of the camera lab to your lab Github repository
1. As usual, update your class Hub repository to add your [forked IDD-Fa18-Lab7](/FAR-Lab/IDD-Fa18-Lab7) repository.
1. Answer the questions in-line below on your README.md.

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**

[![Watch the video](https://img.youtube.com/vi/3CKa2gV6IuQ/0.jpg)](https://youtu.be/3CKa2gV6IuQ) Button working


[![Watch the video](https://img.youtube.com/vi/6XdXe3NJdmM/0.jpg)](https://youtu.be/6XdXe3NJdmM) HelloYou.


## Part B. Web Camera

**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)**

I ran the diff on terminal. The main change seems to be the added webcam functionality in the pictureServer.js. 
pictureServer.js:   It also has Webcam obj constructor which specifies the sizes(width, length, etc) of the picture, and jpeg format. 
When the user clicks to take a photo, NodeWebCam class is used to capture the image. The images are stored in the public folder.
When the parser is reading the arduino button, the button read-in sends dark and light via emit to web page which changes the background color of the web site.
socket.io has takePicture method which takes the picture and gets rid of special characters but merges the date info to make a jpeg picture and save them in the public folder. 

To enable button on Arduino to take picture, pictureServer.js parser would listen to the serial from Arduino which gets passed to client.js on client side via server-msg socket which would be received in client.js. THis was already happening on button click which changes the background color, so I simply added the call to takePicture() in client.js inside the socket sever-msg's switch statement which mimicks taking photo (light --> black).

**b. Include a video of your working video doorbell**

[![Watch the video](https://img.youtube.com/vi/bRsL-9n1XgA/0.jpg)](https://youtu.be/bRsL-9n1XgA) video doorbell working


## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**

I tried to add a thumbnail image function to the takePicture method.
I followed the instruction online. Installed the gm package and added the var declaration and method to resize the image. 
I set the image path to the public folder.
I was able to run the server and take picture.
However, when I checked the public folder where the resized image png file must be in, I was not able to find the resized file. 
I googled for other ways to do it but without the fundamental background in node.js and scripting, I was unsuccessful.. 

![alt text](https://github.com/contactkoh/IDD-Fa18-Lab7/blob/master/gm1.jpg)

![alt text](https://github.com/contactkoh/IDD-Fa18-Lab7/blob/master/gm2.jpg)

![alt text](https://github.com/contactkoh/IDD-Fa18-Lab7/blob/master/gm3.jpg)


**b. Upload a video of your working modified project**

Unsuccessful attempt screenshot after many trials...

![alt text](https://github.com/contactkoh/IDD-Fa18-Lab7/blob/master/gm1.jpg)

[![Watch the video](https://img.youtube.com/vi/bRsL-9n1XgA/0.jpg)](https://youtu.be/bRsL-9n1XgA) video doorbell working

