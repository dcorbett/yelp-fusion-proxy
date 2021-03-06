# Yelp Fusion Proxy

This is an example proxy script for working with the 
[Yelp Fusion API](https://www.yelp.com/developers/documentation/v3/get_started) from a browser. _It is meant 
for instructional purposes only, and should not be used in a production environment with additional security measures._


## Usage

First, copy config-sample.php to config.php, and update the parameters with your own app keys.

Then to call an API, pass a parameter **_ep** that contains the desired endpoint within the API, 
beginning with a forward slash:

```$javascript
jQuery.getJSON("./yelp.php?_ep=/businesses/search&term=Taco+Mac");
```

Note that the endpoint will be prepended with *https://api.yelp.com/v3* (no trailing slash).

Any other parameters will be sent to the requested endpoint, so this should allow full access to the API. It is 
currently only meant for making GET requests; any POST/PUT/DELETE requests will fail in unexpected (but spectacular?!) 
ways.

Cheers!
