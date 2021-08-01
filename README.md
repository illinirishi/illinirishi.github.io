CS 416 Data Visualization- Essay describing the Narrative Visualization
By Rishikesh R. Pagnis; rpagnis2 Summer 2021

Essay describing the Narrative Visualization

The following essay describes the salient points as required in the graded assignment. This essay is available as a README.md file (https://github.com/illinirishi/illinirishi.github.io/blob/main/README.md) on GitHub also. 
You can view the visualization by clicking here (https://illinirishi.github.io/) : Final Project for CS 416 - Compare Fuel Economy measured in Miles per Gallon(MPG)in the City vs on the Highway using a scatter plot. Do number of Cylinders matter? How about Electric Cars with no cylinders?
About the Visualization
The chosen narrative visualization is an Interactive Slideshow. It consists of 3 slides(as Scenes) where the reader has the ability to look at the full dataset as well as highlight data based on a categorical(Engine Cylinders)variable.
The visualization is based on a dataset from a course assignment for scatter plots... https://flunky.github.io/cars2017.csv. The attributes in this dataset are Make(Make of Vehicle), Fuel(Type of Fuel),EngineCylinders(Number of Cylinders in an Engine), AverageHighwayMPG, AverageCityMPG of 146 vehicles from the year 2017.
The narrative visualization is built with scenes, annotations, parameters, and triggers as per the requirements of the project.
Scenes:

There are three scenes in the narrative visualization. The scenes follow a template for visual consistency and follow an order to best convey the message. 
The project title is static and placed above the visualization for the narrative visualization.
The visualization area which displays the data and is consistent with height 510px, width 980px, and background color "grey" for the duration of the narrative visualization.
The plot axes and legend are consistent, and the axes are linear and extend as per the range of the data. The scatter marks are circular and consistent in size and color for the entire narrative visualization.
The visualization scenes are designed for a uniform look and feel and be visually consistent to keep the viewer from getting distracted while moving from one scene to another.
The order of the scenes is driven by the thought of driving the user from an overview of the overall data and highlight the overall trend of the data in scene 1, then to explore that trend in scene 2 based on the categorical variable Number of Cylinders(EngineCylinders) and visualiza how the number of cylinders can affect fuel economy, and finally in scene 3 the user is driven to a suggested conclusion which in this case is to consider the impact of low fuel economy on his next vehicle purchase and preferable buy an electric vehicle. 
Annotations

To highlight the trend in the data, we use Annotations and guide the user to analyze the data further, and ask the user to draw a conclusion from the data. The annotations use a consistent font size, color and a bolded style so that they are not missed by the user. The description and location of the color-coded legend is also provided as an annotation so that the user is not lost. As per the requirement the annotation appear as part of the scene and do not have to wait for a mouseover event.
In Scene 1, the annotation text is positioned inside the visualization area and is meant to highlight the primary findings of the visualization. "As number of cylinders increases, fuel economy decreases for all vehicle types except Electric Vehicles.". The legend is also explained here..."The Legend for number of Engine Cylinders is on the right." When the user clicks the button to move forward to Scene 2 or Scene 3 of the top left of the visualization area the annotation for Scene 1 is cleared.
In Scene 2, the annotation text is positioned inside the visualization area and is meant to highlight the possibility of user being engaged with the data. The user is invited to mouseover the data to see the trends for the different number of Engine Cylinders independently("Mouseover the data to see the individual trends for different vehicles based on the number of Engine Cylinders."). When the user clicks the button to move or navigate back to Scene 1 or forward to Scene 3 the annotation for Scene 2 is cleared.
In Scene 3, the annotation text is positioned inside the visualization area and is meant to ask the user to reflect on what has been discovered in this narrative visualization and to consider this information when making his next vehicle purchase("If you notice the fuel economy for Electric Vehicles with no cylinders is the maximum."). When the user clicks the button to navigate back to Scene 1 or to Scene 2 the annotation for Scene 3 is cleared.

Parameters

Parameters are used to engage the user in the narrative visualization and further explore the data. The parameters used are the state variables in this narrative visualization. The parameter used in this visualization is the categorical variable "EngineCylinders". At first glance EngineCylinders looks like a quantitative variable, but it offers clear seperations of the fule economy variables AverageCityMPG and AverageHighwayMPG and so becomes a good categorical variable option to drive home the point of the Narative Visualisation. The user can visualize the data based on the number of Engine Cylinders at a time (Number of Engine Cylinders being 2,3,4,6,8,10,12,0) by mousing over any data point belonging to the specific number of engine cylinders as per the color in the legend. This allows the user to gain more information about fule economy based on the AverageCityMPG and AverageHighwayMPG, the overall trend that based on number of engine cylinders.
The current state of the visualisation as set up in each scene is controlled by the parameter "EngineCylinders". When mousing over a data point belonging to a particular number of EngineCylinders, the current state changes and the data points belonging to the other number of EngineCylinders are set to opacity = 0.01. When mousing off the data point the current state changes again and opacity for all data points for all vehicle types returns to 1.

Triggers

Triggers are utilized in two ways for this visualization.
The buttons along the top left of the visualization use triggers that enable a user to change scenes. The buttons are labelled such that their functions are made to be obvious: "Scene 1", "Scene 2", "Scene-3" and "About the Visualization".
The user event of clicking on any one of the Scene1, Scene2, Scene3 buttons changes the current Scene of the visualization by changing the visualization scene. A mouseover highlight is used such that the button that represents the current scene of the visualization is displayed with an increased brightness of the label text. When the user mouses over the other buttons, they become temporarily highlighted which indicates to the user that they may be clicked. Upon clicking a button this triggers a change to that specific scene being shown to the user.
Triggers are also utilized with the data points.
The user event of "mouse over" a data point changes the current state of the chart by applying an opacity of 0.01 to all data not part of the vehicle type that is currently moused over. The user event of "mouse off" changes the current state of the chart by returning the opacity of all data points back to 1. This capability for the user event associated with data mouse over is communicated with an annotation.

References used:

D3 Scatter plot example used as reference: https://devdocs.io/d3~3/
Tutorial for building a stepper page used as reference: http://vallandingham.me/stepper_steps.html
Building Legends in d3.js https://www.d3-graph-gallery.com/graph/custom_legend.html

Other References:
How to Slideshow Gallery: https://www.w3schools.com/howto/howto_js_slideshow_gallery.asp
HTML Styles - CSS: https://www.w3schools.com/html/html_css.asp
Hosted Library: https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js
