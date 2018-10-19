# Video Doorbell, Lab 7

*A lab report by John Q. Student*

### In This Report

1. Upload a video of your version of the camera lab to your lab Github repository
1. As usual, update your class Hub repository to add your [forked IDD-Fa18-Lab7](/FAR-Lab/IDD-Fa18-Lab7) repository.
1. Answer the questions in-line below on your README.md.

## Part A. HelloYou from the Raspberry Pi

**a. Link to a video of your HelloYou sketch running.**

[![Watch the video](https://img.youtube.com/vi/6XdXe3NJdmM/0.jpg)](https://youtu.be/6XdXe3NJdmM) HelloYou.



## Part B. Web Camera

**a. Compare `helloYou/server.js` and `IDD-Fa18-Lab7/pictureServer.js`. What elements had to be added or changed to enable the web camera? (Hint: It might be good to know that there is a UNIX command called `diff` that compares files.)**

I ran the diff on terminal. The main change seems to be the added webcam functionality in the pictureServer.js. 
pictureServer.js:   It also has Webcam obj constructor which specifies the sizes(width, length, etc) of the picture, and jpeg format. 
When the user clicks to take a photo, NodeWebCam class is used to capture the image. The images are stored in the public folder.

![alt text](https://github.com/contactkoh/IDD-Fa18-Lab7/blob/master/pictureServer1.jpg)


**b. Include a video of your working video doorbell**

## Part C. Make it your own

**a. Find, install, and try out a node-based library and try to incorporate into your lab. Document your successes and failures (totally okay!) for your writeup. This will help others in class figure out cool new tools and capabilities.**

**b. Upload a video of your working modified project**



![alt text](https://github.com/contactkoh/IDD-Fa18-Lab5/blob/master/finish3.jpg)


1. A video of your useless box in action.


[![Watch the video](https://img.youtube.com/vi/P1V58qeqeeA/0.jpg)](https://youtu.be/P1V58qeqeeA) Finished Box with Durable Working Bopper! with a nice view of the East River.
