# IdentityClient (In progress)

API protected with IdentityServer (Bearer)

# How to use it ? 

Clone IdentityServer and launch it. <br/>
Send a request POST to IdentityServer with parameters: <br/>
  - url: https://localhost:5001/connect/token
  - headers: Content-Type: application/x-www-form-urlencoded
  - Body: grant_type=client_credentials&scope=api1.read&client_id=oauthClient&client_secret=password

The application returns a token response. Copy it.

Clone IdentityClient and launch it. <br/>
Launch application POSTMAN and send a request GET to WeatherForecastController: <br/>
- url : https://localhost:4001/WeatherForecast <br/>
- headers: Authorization: Bearer {your_token_response}

The application IdentityClient returns you the response.
