# Biodiversity
## Overview of the Analysis
## Table of Contents
- [Overview of the Analysis](#overview-of-the-analysis)
    - [Purpose](#purpose)
    - [About the Dataset](#about-the-dataset)
    - [Tools Used](#tools-used)
    - [Description](#description)
- [Results](#results)
- [Summary](#summary)
- [Link to the Dashboard](#Link-to-the-Dashboard)
- [Contact Information](#contact-information)

### Purpose:
The purpose of this project is to create an interactive dashboard which helps each volunteer visualize their bellybutton bacterial biodiversity data. The volunteers should be able to especially identify the top 10 bacterial species in their belly buttons.

### About the Dataset:
The dataset is contained in the following JSON file:
 - [samples.json](https://github.com/SohaT7/Biodiversity/blob/main/samples.json)

It is read in with the help of the D3.js library and a local server. 

### Tools Used:
 - JavaScript (D3.js and Plotly.js libraries)
 - HTML
 - VS Code

### Description:
The analysis aims to visualize each test subject's data - demogrpahic as well as data related to the bacteria present in their belly button. It will do so by creating charts that show top 10 bacteria cultures found, bacteria cultures per sample, and belly button washing frequency (scrubs per week).

The D3.js library in JavaScript is used to read in data from the external JSON file [samples.json](https://github.com/SohaT7/Biodiversity/blob/main/samples.json). JavaScript and Plotly are then used to generate the following three charts (code can be found in the [charts.js]() file):

 - A horizontal bar chart for the top 10 bacterial species (OTUs) found in an individual's bellybutton 
 - A bubble chart to display bacteria cultures per sample (type and size)
 - A gauge chart to show the weekly washing frequency

## Results
The left side of the page has a dropdown menu, wherefrom the individual can select their (or a particular) ID and have the data linked to that ID visualized. Just below the dropdown menu, the individual's demographic information is shown: ID, ethnicity, gender, age, location, bbtype (bellybutton type), and wfreq (wash frequency).

![Options Dropdown Menu](https://github.com/SohaT7/Biodiversity/blob/main/Images/OptionsDropdown.png)

The data visualization on this dashboard includes a horizontal bar chart, a bubble chart, and a gauge chart. The horizontal bar chart shows the top 10 bacterial species (OTUs) for an individual's ID. The x-axis values are the sample_values (a bacterial population in the sample) and the y-axis values are the otu_ids (ID of a certain bacterial specie). The top 10 bacterial species are displayed in a descending order in the chart (i.e. from the highest sample value to the lowest). 

The gauge chart shows the belly button washing frequency in terms of number of scrubs per week. The values are displayed as a measure from 0 to 10 on the progress bar in the gauge chart.

![Panel, Bar, and Gauge Charts](https://github.com/SohaT7/Biodiversity/blob/main/Images/Charts1.png)

The bubble chart shows the bacteria cultures per sample, i.e. the different bacteria IDs and their respective sizes in the sample that was cultured. The otu_ids (ID for a bacterial specie) are the x-axis values and the sample_values (a bacterial specie's population in the sample) are the y-axis values. The marker size is determined by the sample_values (larger the bacterial specie's population, larger the marker), and the marker color is determined by the otu_ids (a different color for each bacterial specie in the sample).

![Bubble Chart](https://github.com/SohaT7/Biodiversity/blob/main/Images/Charts2.png)

## Summary
The dashboard allows the individual to select their ID from a dropdown menu and visualize the data on their bellybutton bacterial biodiversity. A panel on the left showcases their demographic information. A horizontal bar chart shows the top 10 bacterial species (OTUs) in their bellybutton, a bubble chart displays the bacteria cultures per sample, while a gauge chart shows their weekly washing frequency. This dashboard can be made to also include a button 'View all bacterial species', which can be clicked to show the entire list of bacterial species in the individual's bellybutton as well as a horizontal bar chart for it. Since not all individuals might wan tto view this information, leaving it to be displayed only when the button is clicked, seems to be a good choice. 

### Link to the Dashboard:
https://sohat7.github.io/Biodiversity/

## Contact Information:
Email: st.sohatariq@gmail.com


