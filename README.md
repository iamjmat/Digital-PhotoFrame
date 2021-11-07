# Digital-PhotoFrame

## Description
This project is to make use of old unsued smart tablet📱 and use it as a digital photo frame 🖼. 


## Implementation
[Macrodroid](https://play.google.com/store/apps/details?id=com.arlosoft.macrodroid) is installed on the tablet for the automation of the tablet. Macrodroid is a device automation app that can dp various tasks with various inputs. For this purpose, we ue macrodroid webhooks. The webhook triggers the tablet  to unlock and show photos or to exit the app and lock.Macrodoid will be kept in background and it listens to whenever the webhook url is fetched.

The app used for the slideshow is [Fotoo - Digital Photo Frame Photo Slideshow Player](https://play.google.com/store/apps/details?id=com.bo.fotoo). 
I  experimented with quite a few and Fotoo seemed a better option since it has good features like fetching photos from Network share, OneDrive, Google Drive, Google Photos and so on. This would be quite useful as the photo frame could use latest photos even if i dont have physical access to the device. The app is initialised with playing my network share photos as a slideshow whenever started.

In current implementation,adding a simple 'on or 'off  to the webhook url can control the tablet being locked🔒/unlocked🔓 and start/stop the slideshow. 

For on request, the macrodroid unlocks the tablet and starts the Fotoo app. 

For off request, macrdroid exits the slideshow,locks the app and turns the screen off also to save power

For doing it randomly in a day, I used Github workflow which randomly curls the webhook on or off url for triggering it.

Feel free to create issues for any suggestions.
