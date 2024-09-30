# Determining the Location using the 'requests' module

```python
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

```python
from datetime import datetime

form1 = datetime.now()

print(form1)
```


# Get system info and configuration using 'platform' module 

```python

import platform

def get_system_info():
    print(f"System: {platform.system()}")                # Operating System
    print(f"Node Name: {platform.node()}")               # Computer Name
    print(f"Release: {platform.release()}")              # OS Version
    print(f"Version: {platform.version()}")              # OS Build Number
    print(f"Machine: {platform.machine()}")              # Machine Type (e.g., x86_64)
    print(f"Processor: {platform.processor()}")          # Processor Type
    print(f"Python Version: {platform.python_version()}") # Python Version
    print(platform.architecture())                       # Architecture
 
get_system_info()
```
