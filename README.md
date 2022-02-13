# World_Weather_Analysis

## **Project Background**

### Project Goals
#### This project focuses on the application of APIs. Some of Google's APIs and Open Weather Map's APIs were used in this project. The goals of this activity are following:
1. Add weather description to retrieved data.
2. Use input statements to filter data for their weather preferences.
3. Using the results from Goal 2, choose four cities to create travel itinerary.
4. Create a travel route between four cities as well as a marker layer.

### Retrieval of Weather Data
#### The raw data were retrieved by ramdomly generating 2,000 sets of coordinates using *NumPy* library. The *CityPy* was used to identify the cities matching these coordinates. With [OpenWeatherMap API](https://openweathermap.org/current), different parameters for each city were gathered by using *for loop* code. The filetered data were turned into a data frame as shown below:

![This is an image](/Weather_Database/deliverable1_output.png)
 <p align="center">
 Random Cities
 </p>
 
### Travel Destinations Map
#### Using the retrieved cities data frame, preferred cities were identified based on user's preferences on minimum and maximum temperatures. In this case, the minimum was set to 70 and the maximum was 80. The results were converted into a new data frame. With [Google Maps and Places API](https://developers.google.com/places/web-service/search), hotels within 5000 meters of each city from the preferred cities data frame were identified and travel destinations map was created.

![This is an image](/Vacation_Search/WeatherPy_vacation_map.png)
<p align="center">
    Vacation Map
</p>

### Travel Itinerary Map
#### To create a travel itinerary map, four cities were chosen (using *loc* method)  from the vacation map. Using [Google Maps Directions API](https://developers.google.com/maps/documentation/directions/overview) , a travel map was created showing markers and waypoints. 

![This is an image](/Vacation_Itinerary/WeatherPy_travel_map.png)
<p align="center">
    Travel Map
</p>

#### The image below shows another version of the travel map with pop-up marker for each city. In the pop-up marker,  hotel name, city, country, and weather condition are included.

![This is an image](/Vacation_Itinerary/WeatherPy_travel_map_markers.png)
<p align="center">
    Travel Map with Markers
</p>