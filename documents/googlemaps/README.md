# GoogleMaps class

```typescript
import { Platform } from 'ionic-angular';
import {
  GoogleMaps,
  GoogleMap,
  GoogleMapOptions
} from '@ionic-native/google-maps';

export class MapPage {

  map: GoogleMap;

  constructor(private platform: Platform) {
    this.platforms.ready(()=> {
      this.loadMap();
    });
  }

  loadmap() {

    let options: GoogleMapOptions = {
      controls: {
        compass: true,
        myLocation: true,
        myLocationButton: true,
        mapToolbar: true
      }
    };
    this.map = GoogleMaps.create('map_canvas', options);
  }
}
```


## Static method

### create(element, options?)

Generate an instance of [GoogleMap](../googlemap/README.md) class.

<table>
<tr>
  <th>Params</th>
  <th>Type</th>
  <th>Details</th>
</tr>
<tr>
  <td>element</td>
  <td>string | HTMLElement</td>
  <td>Specifies the container of map div</td>
</tr>
<tr>
  <td>options</td>
  <td>GoogleMapOptions</td>
  <td>(optional)Initial option</td>
</tr>
</table>

:arrow_right: returns instance of [GoogleMap](../googlemap/README.md) class
