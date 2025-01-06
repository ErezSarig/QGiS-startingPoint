# Contact me

For any questions, bug reports and any comment or improvements suggestion, please write me at
[Erez.sg@gmail.com](mailto:Erez.sg@gmail.com). 
<br>
<hr>
<br>

# Common startingPoint


This QGiS project is built as a go-to **startingPoint** for new projects. The file opens up with ready made project's settings, styling and easy to use tools and functions. All settings, styles and scripts shared on this project yielded from my own workflows and daily needs while working on versatile types of projects. 

<ins>**Important:**</ins>

**Enabling of macros is needed for tools to work** <br>
**DEM Layer of the area is needed for terrain analysis tools**

## Groups and layers

Project's layers-tree is built to keep focus on the user's **working layers** while structuring styled and improved **background** imagery and also keeping easy access to the **Tools and draft** layers group. 

**Background** is combined from 4 different layers styled using blend modes to create an improved background imagery.

- Ortophoto imagery (deafaulted to google setallite) 
- Google labels, styled to show main features on top of any ortophoto
- OSM Buildings and Water vector tiles, styled to contrast them from other surfaces without hiding or loosing orophoto's details

**Topo** is constructed only from the project's DEM layer styled to show contour lines

- DEM layer is essential for several tools to work so it's strongly advised to replace it only by changing the layer's datasource to your own local DEM file

Also you have **Tables & Data** group to store non-spatial data and **Layers** to store your project's work layers.

## Drafts & tools 

The last group called **Drafts & tools** is made out of [temporary scratch layers](https://docs.qgis.org/3.34/en/docs/user_manual/managing_data_source/create_layers.html#creating-a-new-temporary-scratch-layer) for Points, Lines and Polygons that can be used as drafts. Each layer can also be used for spatial investigations of your project with quick analysing tools.
Scripts and data links for these purposes are allready embedded in each layer's styling rule so you can start easily start just by adding a new feature to that layer. That's the reason they're also reffered to as tools:

### Points layer:

- **Point** - For drafts, just showing your points with no calculations

- **MeasureRadius** - Shows the value of the feature's "Radius" field around your point.

- **ViewShed** - Shows the claculated viewshed of a viewer standing at that point within the calculated radius.

  <sub> **Viewer and target height are defined as layer's variable and can be changed easily, but can't be set separately for each point </sub>

### **Lines** layer:

- **Line** - For drafts, automatic calcuations made for a C-section display

- **Buffer** - Shows the value of the feature's "Buffer" field as a buffer around that line

- **Distance & Avg. slopes **- Show each segment's length and calculated avgerage slope and direction

- **Min Max** - Calculate and shows line's minimum and maximum points

  

- **C-Section mapTip** - Hover with your mouse on each line to display it's calculated C-Section using mapTip 

### Polygons layer:

- **Measures** - Using *Klas Karlsson's* 'Polygons with measurments', this show the measures for all polygon's segments 
- **Intersects others** - Showing the area of intersection of your polygon with another layer and it's calculated size. To choose the layer you want to intersect insert it's name to the feature's "Layer2Intersect" field



- **Intersection group by mapTip** - Shows the aggregated sum of areas intersecting your polygon grouped by categories found on a choosen "GroupByField"



## Ready made settings and scripts

The **startingPoint** file is using project's variables save default scripts and give easy access to them using eval(@ScriptName) on QgsExpressionEngine.

- **@Font** - Easly set and change font settings for all layers,layouts and labels by using this variable when styling of new objects and layers

- **eval_template(@CSS)** - This is a more complex set of ready-made CSS properties (Using the @Font variable  as input). Useful for automatic and unified styling of your html scripts and snippets such as mapTip, Html labels etc

- **eval( @Feat2Html ) ** - Use this script to turn your feature into an Html table.
  
  To control styling of different features use layer's variables such as:
  
  -  **HeaderField** - Insert a field name to use it as a header before the table
  - **HideFields** - Insert field names for fields you don't want to be included in your table, separate field names with a comma
  - **TopFields** - Fields to place on top of the table with their desired order. Other fields will show at the table's bottom with smaller text and in dimgray color
  - **LinkFields** - Fields containing links will use the field's name as a hypertext with field's value as url
  -  **ImageFields** - Will be displayed as images, using field's data as image's url. Images are shown on bottom of the page outside the table



## Project settings

Defualt styling setting are saved for new Polygons, Lines and Points. Newer versions may include styles and colors to support better workflows.

<sub> * Notice that polygons color settings are made with embbeded scripts that can be cleared or deactivated </sub>



