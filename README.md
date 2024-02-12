# React Native Map Clustering

THIS IS JUST A MODIFICATION TO ALLOW PASS A NOT MARKER CLUSTER LIST

This modification allows you to pass a new prop notToCluster whith keys of markers you dont want to cluster.

## Props

| Name                                        | Type                  | Default                                      | Note                                                                                                                                                                                                                            |
| ------------------------------------------- | --------------------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **notToCluster**                            | Array                | []                                      | Pass the marker keys you dont want to cluster                                                                                                                                                              |

## Full Example?

import React from "react";
import MapView from "react-native-map-clustering";
import { Marker } from "react-native-maps";

const INITIAL_REGION = {
  latitude: 52.5,
  longitude: 19.2,
  latitudeDelta: 8.5,
  longitudeDelta: 8.5,
};

const App = () => (
  <MapView
  initialRegion={INITIAL_REGION}
  style={{ flex: 1 }}
  notToCluster=['dontClusterMe']
  >
    <Marker coordinate={{ latitude: 52.4, longitude: 18.7 }} />
    <Marker coordinate={{ latitude: 52.1, longitude: 18.4 }} />
    <Marker coordinate={{ latitude: 52.6, longitude: 18.3 }} />
    <Marker coordinate={{ latitude: 51.6, longitude: 18.0 }} />
    <Marker coordinate={{ latitude: 53.1, longitude: 18.8 }} />
    <Marker coordinate={{ latitude: 52.9, longitude: 19.4 }} />
    <Marker coordinate={{ latitude: 52.2, longitude: 21 }} />
    <Marker coordinate={{ latitude: 52.4, longitude: 21 }} />
    <Marker coordinate={{ latitude: 51.8, longitude: 20 }} />

    <Marker key={"dontClusterMe"} coordinate={{ latitude: 51.8, longitude: 20 }} />
  </MapView>
);

export default App;

### Support

Feel free to create issues and pull requests. I will try to provide as much support as possible over GitHub. In case of questions or problems, contact me at:
[tony@venits.com](tony@venits.com)

### Happy Coding 💖🚀
