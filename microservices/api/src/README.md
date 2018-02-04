## Geolocation-API

## This API does the following :
* Generates the distance matrix from the origin and destination address
* Generates the lat,lng for the particular address
* Generates the address from the lat and lng values

* The input is passed through the url and output is of the form of json

## Resources used:
* Google Maps Geocoding API- It is a service that provides geocoding and reverse geocoding of addresses.
* Google Maps Distance Matrix API- It is a service that provides travel distance and time for a matrix of origins and destinations, based on the recommended route between start and end points.
* Reverse Geocoding - Reverse geocoding is the process of converting geographic coordinates into a human-readable address.


#### Using the HTTP GET method, we retrieve the data given in the form and the above mentioned APIs then return a JSON object, the output in terms of the distance between Source and Destination is computed using Distance Matrix API.

## To execute the file Clone the project and after deploying follow these steps :

### Type the following in the url and see the results :
     http://<cluster-name>/api/address?origin={origin-address}&destination={destination-address},
     http://<cluster-name>/api/location/{location},
     http://<cluster-name>/api/coordinates?lat={latitude}&long={longitude}
    
`Replace {} with the inputs you want and note to replace the API key inside server.js with your own key`

![Api](https://github.com/Ash-D23/Geocoding-T49/blob/master/readme-assets/api.png)
