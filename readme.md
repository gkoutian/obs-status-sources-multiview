# OBS status sources for multiview

#### Version 1.0

This project is a custom website with different status of the OBS studio Software like Streaming status, package lost, recording time, etc for the use in the multiview screen. Also it has a light and dark version.
 It uses the library
[obs-websocket-js](https://github.com/obs-websocket-community-projects/obs-websocket-js), but beware that its used as a local file and can get outdated with a software update and will be needed to update the file.

## Views

### Global View

Its a simple view that can be used by anyone because it has the cpu and memory used and the local time. Also has an indicator of the virtual camera.

### Audio View

Its a view of the audio levels of the current program.

### Recording View

This view has an indicator of the status of the recording: grey for stop, red for recording and yellow for pause.
The other info you access is the recording duration, and the size of the local file.

### Streaming View
This view has an indicator of the status of the recording: grey for stop, blue for streming and purple for reconnecting.
The other info you access is the streaming duration, the frames dropped and the bitrate of the streaming.

## Screenshots

### Global View - Dark Version

![Screenshot Global Dark version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Global-dark.png)

### Global View - Light Version

![Screenshot Global Light version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Global-light.png)


### Audio View

![Screenshot Audio version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Audio.png)

### Recording View - Dark Version

![Screenshot Recording dark version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Recording%20-%20dark.png)

### Recording View - Light Version

![Screenshot Recording light version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Recording%20-%20light.png)

### Streaming View - Dark Version

![Screenshot Streaming dark version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Streaming%20-%20dark.png)

### Streaming View - Light Version

![Screenshot Streaming light version](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/Streaming%20-%20light.png)


### Multi-View Example
![Screenshot Multiview](https://raw.githubusercontent.com/gkoutian/obs-status-sources-multiview/main/img/multiview.png)


## How to use

Is simple, you only need to add the local html file of the desired view as a browser source.
Follow this steps:

1. In a new scene, or your another desired place, add a new "broser source".
2. Select the checkbox "local file".
3. Browse in your computer for the file of your desired view.

It must appear in the multiview but if you have a lot of sources you will need to deactive some to make place (right clicking in a scene and selecting "Show in multiview").
You can also use a multiview plugin like [durchblick](https://github.com/univrsal/durchblick)

### Config
At the start of the html file you have a script section where you can configure the obs websocket port,  password adn the time of update.

```javascript
const obsPort = 4455; //obs websocket port
const obsPassword = ''; //obs websocket password
const timeUpdate = 1000;  //time in milisecond of the data update
```
