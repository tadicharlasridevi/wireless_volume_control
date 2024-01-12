To start the project we need to train a model to recognize the hand for that we use mediapipe to  which in built have hand recognization model.

import mediapipe as mp
mpHands= mp.solutions.hands
hands= mpHands.Hands
mpDraw=mp.solutions.drawing_utils  #This line used to draw lines on the hand which looks like a skeleton on the hand.

we will process the image using model mediapipe for hand gestures.
Now the hand is recognized using mediapipe #framework in which it have hand recognization model)


To test and work with hands we need open Cam and recognize hand using OpenCV


import CV2
cap=CV2.videoCapture(0)

we take the input using OpenCV   #it helps in opening cam and recording video)

Through opencv we collect the image and convert it into RGB form

Generally image will be in BGR form but its will be easy to wrok with RGB form images.

we calculate the distance btwn thumb tip and index tip

we map this distance with audio of our system using pycaw which is an windows audio API

To work with audio of a system pyCaw API which helps us to control volume of system

From pycaw= pycaw import AudioUtilities,IAduioEndpointVolume

devices=AudioUtilities.GetSpeakers  #(getting to work with speakers)

Volume=cast(interface, pointer(IAudioEndpointVOlume) #(it is the ouput device) #This line helps to adjust the volume of speakers by connecting to the o/p device.

we will add the finded gestures into a list and always calculate the distance btwn them and map it to the volume of system so that the volume changes.

Then we will clsoe the windows.
