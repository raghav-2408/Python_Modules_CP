# Determining the Location using the 'requests' module

```
import requests

def get_location():
    # Use an IP Geolocation API like ipinfo.io
    response = requests.get('https://ipinfo.io')
    data = response.json()
    
    # Extract country information from the response
    country = data.get('country')
    
    # Print the country
    print(f"The country you are currently in is: {country}")

get_location()
```


# Get the current date along with the time using 'datetime' module

```
from datetime import datetime

form1 = datetime.now()

print(form1)
```
