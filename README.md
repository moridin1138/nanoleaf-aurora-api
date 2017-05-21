# JavaScript Nanoleaf Aurora API for node.js #

A node.js module, forked from @darrent, which provides a wrapper for the Nanoleaf Aurora API.  Modified to include the temporary setting of an effect.

## Examples ##

### Create the client ###

```javascript
var api = new AuroraApi({
    host: '192.168.1.160',
    base: '/api/v1/',
    port: '16021',
    accessToken: 'TOKEN'
  });

```

### Get device information ###

```javascript
api.getInfo()
  .then(function(info) {
    console.log('Device information: ' + info);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get power status ###

```javascript
api.getPowerStatus()
  .then(function(info) {
    console.log('Power status: ' + info);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Turn the device on ###

```javascript
api.turnOn()
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Turn the device off ###

```javascript
api.turnOff()
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the current brightness value ###

```javascript
api.getBrightness()
  .then(function(brightness) {
    console.log('Brightness: ' + brightness);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Set the brightness value ###

```javascript
api.setBrightness(50)
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the current hue value ###

```javascript
api.getHue(50)
  .then(function(hue) {
    console.log('Hue: ' + hue);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Set the hue value ###

```javascript
api.setHue(50)
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the current colour temperature ###

```javascript
api.getColourTemperature()
  .then(function(temperature) {
    console.log('Colour temperature: ' + temperature);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Set the colour temperature ###

```javascript
api.setColourTemperature(100)
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the current colour mode ###

```javascript
api.getColourMode()
  .then(function(colourMode) {
    console.log('Colour mode: ' + colourMode);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the current effect ###

```javascript
api.getEffect()
  .then(function(effect) {
    console.log('Current effect: ' + effect);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Set the current effect ###

```javascript
api.setEffect('Nemo')
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### List all effects ###

```javascript
api.listEffects()
  .then(function(effects) {
    console.log('Effects: ' + effects);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the device orientation ###

```javascript
api.getOrientation()
  .then(function(orientation) {
    console.log('Orientation: ' + orientation);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Get the layout options ###

```javascript
api.getLayoutOptions()
  .then(function(layout) {
    console.log('Layout: ' + layout);
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Identify (flash the panels) ###

```javascript
api.identify()
  .then(function() {
    console.log('Success!');
  })
  .catch(function(err) {
    console.error(err);
  });
```

### Temporarily set effect (will revert when finished) ###
```javascript
api.setTempEffect('Nemo', 10)
    .then(function() {
    console.log('Success!');
})
.catch(function(err) {
    console.error(err);
});
```
