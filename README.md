## Android Orientation Changer

Android devices have a lot of different resolutions. Your responsive design might not work for multiple orientations on each of those devices. With this plugin you can lock the orientation on runtime after you get the device dimensions. 

## Installation

Through the [Command-line Interface](http://cordova.apache.org/docs/en/3.0.0/guide_cli_index.md.html#The%20Command-line%20Interface):
```
cordova plugin add https://github.com/Hless/cordova-plugin-orientationchanger.git
```

To remove:
```
cordova plugin rm com.boyvanderlaak.cordova.plugin.orientationchanger
```

## Usage

After cordova and its plugins are loaded you can execute the following line of code to lock the orientation:
```javascript
window.plugins.orientationchanger.lockOrientation('landscape');
```
You can choose between `'portrait'`, `'landscape'` and `'default'`. 'default' being the orientation as configured in your config.xml. 

If you want to revert back to default behaviour you can use:
```javascript
window.plugins.orientationchanger.resetOrientation(); // Note that is the same as doing .lockOrientation('default')
```

You can get the orientation the plugin is currently enforcing by calling:
```javascript
window.plugins.orientationchanger.getOrientation();
```