## Geolocation-API

## This API does the following :
* 1.Generates the distance matrix from the origin and destination address
* 2.Generates the lat,lng for the particular address
* 3.Generates the address from the lat and lng values

* The input is passed through the url and output is of the form of json

## To execute the file Clone the project and follow the steps :

### Type the following in the url and see the results :
    * http://<cluster-name>/api/address?origin={origin-address}&destination={destination-address},
    * http://<cluster-name>/api/location/{location},
    * http://<cluster-name>/api/coordinates?lat={latitude}&long={longitude}
    
`Replace {} with the inputs you want and note to replace the API key inside server.js with your own key`
