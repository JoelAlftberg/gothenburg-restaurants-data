# Opening hours of restaurants in the Gothenburg area
A python project that uses the Google Places API to collect all the opening hours of restaurants in the Gothenburg area, then stores it in a .csv file.

## TO-DO

- Add possibility to show next 20 results with nextPageToken query
- Store results in a .csv file
- Create a list of different search terms to use
- Function for iterating through restaurants and find opening hours
- Visualize the data
- Clean formatted address to just include the street 

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

### 1.3 Formatting the data
Basically no cleaning was needed, I could just input the data from the json we got from the queries into a dictionary and then into a Pandas dataform.
A minor problem is that by using the Text Search query, we don't query the opening hours. It seems that you need to do a specific query against\
the restaurant and ask for the opening hours. This means we need to loop through the dictionary we created from the json\
and create a separate function to populate the dict with another column where we append the opening hours.

