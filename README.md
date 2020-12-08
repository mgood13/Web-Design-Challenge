# Web-Design-Challenge

This project is a website used to visualize the Python API project from an earlier homework.
It contains a number of linked pages that display the analyses from that project. Each analysis
is for comparing Latitude with a number of different parameters (Temperature, Cloudiness, 
Humidity, and Wind Speed). On each page there is an analysis for the full world followed by plots
for each hemisphere specifically along with analysis and fun facts along the way.
There is a page for comparison of all full world plots side by side, Raw Data for the dataset,
and Resources for the project. This is summarized below.


<ul>
    <li>The <i> <b class = 'highlight'>Weather Analysis</b> </i> page brings the user back to the homepage.</li>
    <li>The <i> <b class = 'highlight'>Plots</b> </i> dropdown contains links to each specific plot generated during this analysis. Each analysis was performed first for the whole earth
    and then each hemisphere separately to observe any more granular trends in the data.</li>
    <li>The <i> <b class = 'highlight'>Comparison</b> </i> tab contains all of the plots together side by side.</li>
    <li>The <i> <b class = 'highlight'>Resources</b> </i> tab contains information about the resources that went into generating this dataset.</li>
    <li>The <i> <b class = 'highlight'>Data</b> </i> tab allows visualization of the raw data used to generate the plots.</li>
    <li>The <i> <b class = 'highlight'>Github</b> </i> symbol is a link to the code used to create the webpage.</li>

</ul>

<p>
The following code was used to generate the html table. First the file is read in from the 
weather_check.csv. Then it is processed, and finally written as html code to a file "table.html".
We took this code and placed it into our own data.html file which became the Raw Data tab above.

```
weather_df = pd.read_csv('../WeatherPy/weather_check.csv')
html_df = weather_df
weather_df.head()

outputhtml = html_df.to_html()
type(outputhtml)

text_file = open("table.html", "w")
text_file.write(outputhtml)
text_file.close()
```



</p>
