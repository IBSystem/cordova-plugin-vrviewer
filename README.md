# cordova-plugin-vrviewer

The Cordova plugin for GVR.
See [GVR](https://developers.google.com/vr) for more information.

# Installation

```
$ cordova plugin add https://github.com/almas/cordova-plugin-vrviewer.git
```

# How to use

call the **vrViewer** function directly

## Play VR video ##
```
var options = "{
    'inputFormat': 'FORMAT_DEFAULT',
    'inputType': 'TYPE_STEREO_OVER_UNDER'
    }";

vrViewer.playVideo(url, options);
```

* url: the VR video url, it also can be the fullpath of local video.
* options: JSON string.

### inputFormat: ###
    FORMAT_DASH: 	Indicates that the video uses the MPEG-DASH format.
    FORMAT_HLS:  	Indicates that the video uses the HTTP Live Streaming (HLS) format.
    FORMAT_DEFAULT:  	Indicates that the video is in a standalone, non-streaming format using container formats such as mp4, webm, ogg, aac.
### inputType ###
    TYPE_MONO:  	Each video frame is a monocular equirectangular panorama.
    TYPE_STEREO_OVER_UNDER:  	Each video frame contains two vertically-stacked equirectangular panoramas.

`vrViewer.stopVideo()`


## Play VR panorama image ##
```
var options = "{
    'inputType': 'TYPE_STEREO_OVER_UNDER'
    }";

vrViewer.startPanorama(url, options);
```

* url: the VR image url, it also can be the fullpath of local image.
* options: JSON string.

### inputType ###
    TYPE_MONO:  	Image contains a single equirectangular panorama.
    TYPE_STEREO_OVER_UNDER:  	Image contains a pair of equally-sized equirectangular vertically-stacked panoramas.
