#### 007 James Bond + XLR Radios

A framework for a real-time visualization using 3 XLR radios to triangulate the location of a fourth. This framework consists of 3 elements: a computer tethered to 1 XLR radio, a remote server collecting+relaying the lat/lon positions of, and a client-side webpage displaying the location data in real-time on a map.

A python script using the XLR API sends frames to radio 1, both for getting its distance to radio 4 (TRANSMIT REQUEST), as well as getting distance measurements from each remote radio to the fourth (REMOTE AP COMMAND). Using these distance measurements along with the hard-coded lat/long of the three radios, we are able to locate the forth radio in space and convert its X/Y location to lat/long. The script them makes repeated HTTP POST requests, with the lat/long in the body,  to the remote server.

The server visualizes the data on a map using Mapbox and D3.js. 
