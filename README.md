﻿# DetectionCamera

##	Steps to build and run the app.
	1. project copy : git clone https://github.com/jaeeun/DetectionCamera.git
	2. Install SDK : Version 33
		[Adnroid Studio] file > Setting > Appearance & Behavior > System Settings > Android SDK
		Check the box of API level 33 (Android Tiramisu) > Apply
	3. Build Gradle
	4. Build Project

##	Any assumptions made.
	1. If the app open and point the camera at any object, it can identify what kind of object it is.	
	2. While images are being captured, it draw bounding box, shows object type.
	3. After capture, in a few seconds, it will be saved the image with bounding box, object type.
 	4. I fixed the max number of results to 5.

##	Challenges faced and how they were addressed.
	1. If you access the gallery as soon as touch the capture button, New captured image does not add on their own gallery fragment.
 	  : It has to wait for new media file and add the image into the viewpager.
	2. Basic tflite model seems to unstable and the perceived categories of objects are much different from the real.
 	  : It's a little disappointing that I couldn't add a fine tune model.
