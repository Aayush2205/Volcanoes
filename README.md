# Volcanoes
This program redirects us to a web map in which we get to know about the volcanoes and their height according to the data provided and the population that is present all over the world.

## Libraries that are used-
###For this project we have used only 2 libraries- **pandas** and **folium**
**pandas**- as I've used the Jupyter Notebook for this project so pandas is installed by default.
**folium**- folium is a library which converts the python code to javascript/HTML/CSS code which is helpful for interaction in web pages.
            It is needed to be installed using $ pip install folium in Jupyter Notebook.
            
##Project overview

At first we have to insert the volcanoes.txt file using the read_csv function from pandas, as it contains the elevation, name, latitude, longitude and etc.
After inserting the text file we have to create certain variables that will contain the list of the content of the text file like Latitude, Longitude, Elevation and Name.
Using the folium.map we will create a web map with pointing at certain longitute and latitide and the terrain type is *Stamen Terrain*
Now we'll start adding layers for the Volcanoes and the Population using the FeatureGroup function of folium.

###For Volcanoes
At first run a for loop in which we'll use the variable that we created to store the list from the text file and we'll run it through the values of the text file 
The zip() function returns a zip object, which is an iterator of tuples where the first item in each passed iterator is paired together, and then the second item in each passed iterator are paired together etc.
After that I had used the add_child function to add the circle markers for the volcano pinpoint location and it poppthe name and the elevation of the volcano.
And we create a function which decides the color of the marker with respect to the elevation.

###For Population
we'll use add_child function to  add the GeoJSON function of the folium so as to open the world.json file in reading mode as it contains the population of the world.
and for the style_function we'll use a lambda function so as to give a color background with respect to certain population criteria.

for the final step well add both of our feature groups to the map that was created through folium.map
and after adding the feature groups we'll use the LayerControl() function of folium which provide us with layers to control both the feature groups.

To end the program we just use save function of the folium to give the map a name. 
