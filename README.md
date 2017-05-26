# webMethods CloudStreams Provider for Google Maps
This project provides a sample webMethods CloudStreams Provider Project for Google Maps. The following APIs are available:
* **Directions:** The Google Maps Directions API is a service that calculates directions between locations. https://developers.google.com/maps/documentation/directions
* **Distance matrix**: The Google Maps Distance Matrix API is a service that provides travel distance and time for a matrix of origins and destinations, based on the recommended route between start and end points. https://developers.google.com/maps/documentation/distance-matrix
* **Elevation**: The Google Maps Elevation API provides elevation data for all locations on the surface of the earth, including depth locations on the ocean floor (which return negative values). https://developers.google.com/maps/documentation/elevation
* **Geocode**: The Google Maps Geocoding API is a service that provides geocoding and reverse geocoding of addresses. https://developers.google.com/maps/documentation/geocoding
* **Gelocation**: The Google Maps Geolocation API returns a location and accuracy radius based on information about cell towers and WiFi nodes that the mobile client can detect. https://developers.google.com/maps/documentation/geolocation
* **Timezone**:The Google Maps Time Zone API provides time offset data for locations on the surface of the earth. https://developers.google.com/maps/documentation/timezone

## Requirements

The project was developed and tested on the following installation:
1. Integration Server 9.12
2. CloudStreams Server 9.12
3. Software AG Designer 9.12 with Service Development and CloudStreams Development

## Quick start

To install the project on your local development environment follow these steps.

### Prepare CloudStreams Servers

1. In Software AG Designer open ```Window > Preferences```
2. Navigate to ```Software AG > CloudStreams Servers```
3. Add your local Integration Server. If there is already an entry make sure username and password are correct by clicking the Test button.

### Import CloudStreams Provider Project

1. In Software AG Designer switch to the ```CloudStreams Development``` perspective.
2. Select File > Import and choose ```Software AG > CloudStreams Provider Project```. Click Next.
3. Select the root of this repository as the Root Directory
4. Select the ```Google Maps``` project
5. Check ```Copy project into workspace```
6. Click Finish.
7. Expand the newly imported project.
8. Right-click ```com.softwareag.googleMaps``` and select Deploy.

### Import Integration Server packages
The CloudStreams Provider Project does not contain neccessary doctypes.

1. Copy GoogleMaps.zip and GoogleMapsTests.zip to ```<install_dir>/IntegrationServer/instances/<instance>/replicate/inbound```
2. Open Integration Server Administration in your browser
3. Install both packages with ```Install Inbound Releases``` in Package Management

### Add Google API Key and activate connections

To access Google APIs an API key is neccessary. Generate your API key here: https://console.developers.google.com/apis/credentials. Make sure all Google Maps APIs are enabled in your library by clicking and enabling each of them (https://console.developers.google.com/apis/library).

1. Open Integration Server Administration in your browser
2. Navigate to ```Solutions > CloudStreams > Providers > GoogleMaps```
3. Select ```Google Maps``` from the Connector List

You will find two (disabled) connections: GoogleMapsTest:apiConnection and GoogleMapsTest:mapsConnection. You need to modify both connections:
1. Click the Edit button of the connection
2. Enter your Google API key in APIKey-field and save the changes.
3. Enable the connection.

______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.
_____________
Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.
