# DetectionCamera

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

##	Challenges faced and how they were addressed.
	1. If you access the gallery as soon as touch the capture button, the app may be killed.
	   : Need to handle the exceptions. And also, It would be nice to have the thread and the viewmodel that obsering updated image
	2. Different result with preview and captured images.
	   : After taking picture, I copied it and make detection again. As a result, It have some issues with processing speed, mis calculating scalefactor. So It has to capture preview and overlay view at the same time.
