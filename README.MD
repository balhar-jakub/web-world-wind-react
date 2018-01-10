This is an initial version of an component showing the integration of the Web World Wind into the ES5 and React ecosystem. 
It is possible to integrate the map by including this component and receive the instance of the Web World Wind created inside
this component.

After the installation of the component it is integrated into the application via: `import Map from 'web-world-wind-react'`

In order to receive the Web World Wind instance use the component in following way:
```javascript
import React, { Component } from 'react';
import Map from 'web-world-wind-react';

class App extends Component {
    mapCreated(webWorldWind) {
        console.log('Web World Wind was initialized');
    }
    
    render(){
        <div className="App">
            <Map 
                onMapCreated={this.mapCreated.bind(this)}
            />
        </div>
    }
}
```

In order to customize the way the Map will look like. There are two elements to customize:

```html
<div id="map">
    <canvas id="wwd-results"></canvas>
</div>
```