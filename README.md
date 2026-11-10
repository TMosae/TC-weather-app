#TC Weather App!!

This is a CL weather app built in python. What you do is, you type a city in the terminal, and then it shows you the current temperature and wind speed(no browser, no signup, no API key needed.
I build it following the FreeCodeCamp tutorial: [How to build a command-line weather app with python]

##WHAT DOES IT DO?
- Takes a city name from the terminal
- Turns that city name into coordinates using the Open-Meteo Geocoding API
- Fetches the live weather for those coordinates from Open-Meteo
- Prints the current temperature and wind speed in the terminal
- handles errors gracefully - e.g. if the city isn't found, or you have no internet

##HOW DOES IT WORK?
1. 'get_coordinates(city_name)' - calls 'https://geocoding-api.open-meteo.com/v1/search' to get latitude + longitude
2. 'get_weather(latitude, longitude)' - calls the Open-Meteo forecast API to get the current weather
3. 'main()' - uses 'sys.argv' to read the city you typed, then prints the results

##HOW TO RUN IT?
--you'll need:--
1. python 3 installed
2. The 'Requests' library

--install it with:--
'''bash
pip install requests

--RUN IT--
python3 weather.py vereeniging
          or
python3 weather.py johannesburg 


----WHAT I LEARNED-----
1. How to make http requests in python with Requests
2. how to parse JSON data from an API
3. How to turn a city name into coordinates with a Geocoding API
4. How to use sys.argv to take command line arguments
5. How to handle errors - city not found, no internet cases - without crashing


---CREDITS---
Tutorial from FreeCodeCamp:https://www.freecodecamp.org/news/how-to-build-a-command-line-weather-app-with-python/
