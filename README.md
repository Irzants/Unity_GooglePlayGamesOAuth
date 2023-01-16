# Unity_GooglePlayGamesOAuth
Maybe this step is usefull for you

 source: https://developers.google.com/games/services/console/enabling
 
 MAYBE, WATCH THIS TUTORIAL CAN HELP YOU : https://www.youtube.com/watch?v=e4SHxOaePqY&ab_channel=Flarvain
 
 - Step by step setting Google Play Games Services Login -
 
	1.	Create keystore khusus untuk debug
	2.	Get the fingerprint keystore
	3.	Create new OAuth credential on Google Cloud (using fingerprint keystore)
	4.	Download JSON credential, use it on project
	
-Adding SHA fingerprint
1.	Go to Google PLay Console, and select app
2.	Seelct Grow -> Play Games Services -> setup & management -> Configuration, click on Add credential
3.	If login from Android apk, select Android else Game Server for type
4.	Under Authorization section
	- Click on Create OAuth Client button
	- Open Create OAuth Client id
	- Enter your package name
	- Fill in the SHA fingerprint (for creatin one, check FAQ)
	- Save
	- Back to authorization section and select the created OAuth client
5. Click on Save

~ Input NEW SHA1 into credentials ~
	1.	Go to Google Developer Console
	2.	Click All aplication > your application
	3.	Go to Release Management > App signing
	4.	Notice theere is an "Upload Certificate" and an "App Signing Certificate"
	5.	Copythe SHA1 from the APP SIGNING CERTIFICATE. 
		After all that keystore rigmorale, they fail to mention this part in documentation
	6.	Click All App on the TOP LEFT, then click Game Services > Game Details
	7.	Look for API Console Project
	This game is linked to the API console project called 'YOUR APP NAME SHOULD BE HERE'
	8.	Click on your app name at this location
	9. Now you are in the API's & services. click on Credentials
	10. Delete whatever you have under OAuth 2.0 client IDs
	11.	Now, click on Create Credentials > OAuth Client ID
	12.	COPY THE SHA1 FROM THE APP SIGNING CERTIFICATE HERE AND BE SURE YOUR PACKAGE NAME IS CORRECT
