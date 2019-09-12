# Barkio Barking Detection Challenge
Welcome to Barkio Barking Detection Challenge! We are TappyTaps, a developer company of mobile apps. We are now launching a new dog monitoring app called [Barkio|https://barkio.com] and we are running (hopefully) an interesting challenge for you. 

## What is Barkio
Barkio is a new app launching soon for mobile and desktop, which will help the pet owners with monitoring their dogs. The app comes in handy when the dog owners are at work or when traveling as they can easily stay in touch with their dog and interact with it remotely. Besides video and audio monitoring, the app tells the dog owner whether the dog is quiet (resting) or whether some noise was detected. As of now, the app can detect the noise, but it cannot recognize whether the noise was barking or something else.
  
## The purpose of this challenge
We want to help the dog owners when they’re not at home (e.g., traveling, working) to check on their dog. The dog owner can check all activities in the Activity log, and replay all captured noises. Unfortunately, the app cannot detect whether the noise was the dog barking or not, so the dog owner needs to listen to the noises to detect it. We want to help the pet owners and tell them if the noise was their dog barking. A solution to this is an algorithm to detect barking. We already developed prototype of this internally, but we believe you may have other ideas how to solve this specific sound detection, so we’ve come up with a challenge! 

## The goal
* create a program which identifies barking intervals in the MP3 file and the length of each interval
* **NOTE**: Feel free to use the MP3 [file we've provided](Barkio-Barking-Detection-Challange-1.mp3) to test the algorithm or test it on any barking sounds of your choice. The evaluation of the algorithm will be performed on a different MP3 file.

## Rules of the challenge
* Clon this repository
* Write a program in a language of your choice that analyzes audio and the output creates a JSON with the results
* The detection program itself must be running without the internet network (any installation/configuration will, of course, have access to the internet network)
* The application must be running in a Unix environment. On Windows, you can use for example Docker or Windows Subsystem for Linux.
* Prepare the install.sh file in your cloned repository to run the installation/configuration of the app and also a file INSTALL, where will be written how the environment should be prepared (e.g., Node JS 10.0, Python, etc.).
* In your cloned repository, prepare a run.sh file which accepts 1 parameter - the path to MP3. This script will run an analysis of the file and will write the result of the analysis in JSON format to the standard output 
* Your solution will be publicly available on GitHub and anyone can use it in the future without any restrictions (not just TappyTaps).

## Evaluation of the algorithm
* The MP3 file contains X intervals of dog's barking; for each correct detection of the barking part, the participant gets 1 point  
* For each false detection, the participant loses 1 point 
* For each correctly detected length of the barking interval, the participant gets 1 point 
* Tolerance of when the barking interval starts is +- 1 second, tolerance of the interval length identification is +- 2 seconds 
* The total rating will be given by a percentage (number of points / X * 2) * 100 
* The order of the winners will be determined by the number of points. If two or more participants reach the same number of points, the order of the winners will be determined by the speed of the processing (how long it takes the program to detect the barking).

## Example
The tested MP3 file contains 10 intervals of the dog's barking. The tested algorithm identifies 9 starting points of the barking intervals. It also correctly identifies a length of 7 of those 9 intervals. The algorithm wrongly identifies 1 non-barking interval as barking.
* Maximum points possible: 20
* Points for barking recognition: 9
* Points for correct interval length: 7
* Penalty points for wrong identification: -1
* **The overall score is (9 + 7 -1) / 20 * 100 = 75%**

## Prices
* **$500 USD** for the best algorithm which gets at least 60% in the evaluation process
* **$300 USD** for the second-best algorithm which gets at least 60% in the evaluation process
* **$100 USD** for the third-best algorithm which gets at least 60% in the evaluation process

## Bonus for precise algorithm
* **extra $300 USD** for the best algorithm of all that gets at least 90% in the evaluation process

Thank you for participating! We're looking forward to your projects. 
