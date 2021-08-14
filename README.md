# Opening hours of restaurants in the Gothenburg area
A python project that uses the Google Places API to collect all the opening hours of restaurants in the Gothenburg area, then stores it in a .csv file.

## TO-DO

- Add possibility to show next 20 results with nextPageToken query
- Store results in a .csv file
- Create a list of different search terms to use
- Function for iterating through restaurants and find opening hours

## 1. Getting the data

### 1.1 Creating a Google Places API key 
First I had to create an API key to be able to get the data I wanted in a simple way.\
By creating a project on the Google Cloud Platform and then Enabling the Places API I was able to create an API-key.\
To be able to then use the API-key to send requests I had to enable billing on the Google Cloud Platform.

### 1.2 How to structure the GET-requests
<a href=https://developers.google.com/maps/documentation/places/web-service/search-find-place#fields>How to search and find with the API</a>\
I used this resource from the Places documentation to find out how to structure the GET-requests.\
The entities/rows we want are the Restaurants in Gothenburg.\
The attributes/fields we want he data to have are; opening hours, rating and total amount of ratings.

