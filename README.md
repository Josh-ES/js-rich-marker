RichMarker – A Google Maps JavaScript API utility library (unofficial)
==============

A library for using arbitrary DOM elements as map markers in the Google Maps JavaScript API v3.
![Analytics](https://maps-ga-beacon.appspot.com/UA-12846745-20/js-rich-marker/readme?pixel)

[Reference documentation](https://googlemaps.github.io/js-rich-marker/reference.html)

Migrated from the [Google Maps JavaScript API utility libraries on Google Code](https://code.google.com/p/google-maps-utility-library-v3/).

## Live Demo

[![RichMarker Screenshot](https://googlemaps.github.io/js-rich-marker/screenshot.jpg)](https://googlemaps.github.io/js-rich-marker/examples/richmarker.html)

[Example page](https://googlemaps.github.io/js-rich-marker/examples/richmarker.html)

## Contributing

Want to contribute? Check out the [contributing guide](CONTRIBUTING.md)!

## License

Copyright 2014 Google Inc. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## NPM Port

This node package is not just a simple copy and paste of the code from
the main git repository, there are some slight changes. The RichMarker
and RichMarkerPosition variables are both exported from the module,
and can be imported using either ES6 syntax:

```import { RichMarker, RichMarkerPosition } from 'js-rich-marker'```

or the standard require:

```var RichMarker = require('js-rich-marker').RichMarker;
var RichMarkerPosition = require('js-rich-marker').RichMarkerPosition;```

depending on your project. A very basic TypeScript declaration file is
included.

## RichMarker

A new RichMarker object can be created as follows:

```import { RichMarker, RichMarkerPosition } from 'js-rich-marker'

const marker = new RichMarker({
    map: google.maps.Map, // the google map object to attach the marker to
    position: google.maps.LatLng, // the position of the marker, using the google maps LatLng format
    draggable: boolean, // whether the marker should be draggable
    content: string | Element, // a string or element representing the HTML pattern you wish to use as a marker
    anchor: RichMarkerPosition, // a number, defining the anchor position of the marker, using the RichMarkerPosition enum
    options: google.maps.MarkerOptions, // see the link below for details
});```

There are other options that can be directly accessed by the constructor, including:

```visible, shadow, anchor```

For a specification on the marker options available to you, visit the
[Google Maps JavaScript API v3 Docs](https://developers.google.com/maps/documentation/javascript/3.exp/reference#MarkerOptions)
