# hotelery Web-Service
## Introductory
To interact with the hotelery Smart Housekeeping API you must provide the 'Authorization'-HTTP-Header with the following value 'Api-Key yourSpecialSecret' with each request.
If the Authorization-Header is missing, or your key isn't valid in any way you'll receive a 401-HTTP-reponse.
In one of the next API versions you'll be able to switch to OAuth as well.

## REQUEST THRESHOLD
In general, you can interact (send requests) as often as you want to our Web-Service.
For updates of resources we suggest that you send your data only when it updates on your side (trigger). No need to (re-) send unchanged data.
When it comes to pulling data from our service it is up to you how "real time" your data should be. We're suggesting to have poll intervals no longer than 15 minutes.

## ENVIRONMENTS
Development: https://ws-prev.hotelery.de  
Production: https://ws.hotelery.de

## DEV NOTES
For security reasons we do not throw / return explicit validation errors. You'll just receive a 500 response.

The preview / development API Server will sleep after 30 minutes of inactivity, but it'll wake up on any HTTP request send to it. The live / production environment will be reachable 24/7.

All rights reserved. 

hotelery is a product by [we.io GmbH](https://we-io.de "we.io GmbH")