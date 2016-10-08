# simpleAR7
## simpleAR7 Demo - Showing Geolocation hacks added to the JSARToolKit5

Entry for The Stamford Hackathon 16-18 September 2016

<img align="right" height="200" src="https://raw.githubusercontent.com/mkobar/simpleAR7/master/Screenshot_2016-10-08-17-53-33.png">
<img align="right" height="200" src="https://raw.githubusercontent.com/mkobar/simpleAR7/master/sphere.png">

### The Idea
The idea is to allow geolocation-only Augmented Reality (AR) in supported web browsers, without any third party apps (No Apps) required.  So No AppAR.

### How It Works
The current JSARToolKit5 (ported from the python library) already allows AR in web browsers, but with real-time video detection of markers or limited barcodes.  Our hacks use geolocation and geofences to trigger the AR point detection, then allow an image to be displayed at a marker location.

### How It Was Built
We modified the JSARToolKit () with geolocation data tagged to markers and a geofence detection code that could be called instead of the current marker detection event loop.  The demo web site was coded in JavaScript/CSS/HTML5 with our modified JSARToolKit and Three.js (which was used to display the three-dimensional objects in the canvas).
We did find that due to security issues the currently supported browsers (firefox and chrome) can only allow the required getUserMedia method to be allowed if served up with HTTPS.  So we hosted our demos under GitHub pages with HTTPS.

### What's next for NoApp AR
All of the current geolocation features have been added as javascript patches and will need to be ported back to the original ARToolKit in python (as that is the supported base).  Also, since all of the geo and image processing is based in the client web browser, the amount of markers is limited (ARToolKit recommends no more that 1,000 simple markers).  This could be increased with a larger geofence that could trigger marker downloads when entered.

The other major current limitation is that the JSARToolKit currently does not support NFT (Natural Feature Tracking) Markers or full photo images, because it is too computationally expensive on the client side.

### Live Demos
Apple *iPhone* and any *Android* smartphones (or tablets) can run the demo pages (below) with either the Chrome or Firefox browser.

Please note that the geofences are placed from the Stamford Innovation Center (175 Atlantic Street Stamford, CT 06901 lat: 41.052904  lon: -73.539738  to 1544 Bedford Street lat: 41.064597 lon: -73.541436)

https://mkobar.github.io/simpleAR7/index.html

https://mkobar.github.io/simpleAR7/index2.html

##Resources

Stamford Hackathon site: http://www.stamfordhackathon.org/

ARToolKit - http://artoolkit.org

JSARToolKit - https://github.com/artoolkit/jsartoolkit5

Three.js - https://threejs.org and http://ushiroad.com/3j/

X3DOM - http://www.x3dom.org
