![image241](http://report.h2783491.stratoserver.net/files/image241.png)

Contents:

- [A.	Introduction:](#a-introduction)
- [B.	Administration](#b-administration)
  - [I.	Sync users to Portal V4](#i-sync-users-to-portal-v4)
  - [II.	Configuration](#ii-configuration)
  - [III.	Add Probe](#iii-add-probe)
- [C.	How to aggregate Data:](#c-how-to-aggregate-data)
  - [I.	Bucket aggregations for X axis](#i-bucket-aggregations-for-x-axis)
  - [II.	We use metric aggregations for Y axis](#ii-we-use-metric-aggregations-for-y-axis)
- [D.	Visualizing Data:](#d-visualizing-data)
  - [I.	Scatter Chart](#i-scatter-chart)
  - [II.	CDF Chart](#ii-cdf-chart)
  - [III.	Pie Chart](#iii-pie-chart)
  - [IV.	Bar Chart](#iv-bar-chart)
  - [V.	Stacked Bar Chart](#v-stacked-bar-chart)
  - [VI.	Aggregated Bar Chart](#vi-aggregated-bar-chart)
  - [VII.	Coordinate Map](#vii-coordinate-map)
  - [VIII.	Set TimeFilter for Visualization](#viii-set-timefilter-for-visualization)
  - [IX.	Clone Visualize](#ix-clone-visualize)
- [E.	Dashboard](#e-dashboard)
- [F.	User can only see its own/shared/public visualizations or dashboards:](#f-user-can-only-see-its-ownsharedpublic-visualizations-or-dashboards)
- [G.	Group of users:](#g-group-of-users)
- [H.	Redirect to Alarm Page](#h-redirect-to-alarm-page)
- [I.	Discover](#i-discover)
- [J.	Document Revision:](#j-document-revision)


<div id='a-introduction'/>
# A.	Introduction: 

- This document is brief introduce about how to create visualizations of the data in INTERLEV Portal V4. You can then build dashboards that display related visualizations.
- Helps to manage Probes, Users, Group of Users and related Permissions.
- And you can also schedule report daily, weekly and monthly as needed.

# B.	Administration:

## I.	 Sync users to Portal V4:

To sync users from Portal V3 to V4, user click on Sync users to Portal V4 button then input Password (min. 6 characters) as 
 
>![image1](http://report.h2783491.stratoserver.net/files/image1.png)

Then click on Sync button, list of users will be synchronized from Portal V3 into Portal V4.

## II.	 Configuration:

### 1.	Set up popularity for Dimension
On left menu, click on Configuration menu item, Management page will be shown as:

 >![image2](http://report.h2783491.stratoserver.net/files/image2.png)

Step 1: On Management page, click on Fields, list of dimensions will be shown as: 

 > ![image3](http://report.h2783491.stratoserver.net/files/image3.png?style=centerme)

Step 2: Click on popularity column, the Fields table will be ordered by popularity.
	 
> ![image4](http://report.h2783491.stratoserver.net/files/image4.png)
Click on Edit icon of controls as:
  
> ![image5](http://report.h2783491.stratoserver.net/files/image5.png)
Update Field page will be shown as:
 
> ![image6](http://report.h2783491.stratoserver.net/files/image6.png)
-	Click on “+” icon to increase Popularity.
-	Click on “-” icon to decrease Populariy.
-	Click on “Update Field” button to apply the changes and back to previous page.
-	Click on “Cancel” button to back to previous page without changes.


### 2.	Dimension is ordering by popularity on New Visualization page
Click on Visualize menu item, Visualize page will be shown as:

 > ![image7](http://report.h2783491.stratoserver.net/files/image7.png)

Click on Add icon, then click on Scatter plot as:

 >![image8](http://report.h2783491.stratoserver.net/files/image8.png) 

Click on Dimension box, list of Dimensions is ordering by popularity as:
 > ![image9](http://report.h2783491.stratoserver.net/files/image9.png)

Input data then click on Create A Visualization, New Visualization page will be shown.

Click on Select a field, list of Dimensions is ordering by popularity as:

 >![image10](http://report.h2783491.stratoserver.net/files/image10.png) 

### 3.	Dimension is ordering by popularity on Edit Visualization page
Click on Visualize menu item, Visualize page will be shown. Then click on a plot to open as:
	 
 >![image11](http://report.h2783491.stratoserver.net/files/image11.png)


Click on Select a field, list of Dimensions is ordering by popularity as:

 > ![image12](http://report.h2783491.stratoserver.net/files/image12.png)

### 4.	Change Password:

Click on Account, change password page will be shown as:

>  ![image13](http://report.h2783491.stratoserver.net/files/image13.png)

Input Password and Repeat password, if they are not matched, warning message will be shown as:

 > ![image14](http://report.h2783491.stratoserver.net/files/image14.png)

Input Password and Repeat password, if they are matched, information message will be shown as:
> ![image15](http://report.h2783491.stratoserver.net/files/image15.png)
 
User should logout then log in again to continue working.
## III.	 Add Probe:

Admin login then click on Permisisons
 
> ![image16](http://report.h2783491.stratoserver.net/files/image16.png)

To add new Probe, click on Add Probe button
 > ![image17](http://report.h2783491.stratoserver.net/files/image17.png)

Then input Name, Password, Password confirmation as:
> ![image18](http://report.h2783491.stratoserver.net/files/image18.png)
 

If Password and Password confirmation are not matched, warning will be shown as:

> ![image19](http://report.h2783491.stratoserver.net/files/image19.png)
 

Click on Submit, new Probe is created successfully as:

 >![image20](http://report.h2783491.stratoserver.net/files/image20.png) 

User can add related User and related Group as:
 
 >![image21](http://report.h2783491.stratoserver.net/files/image21.png)
New Probe and related Users/Groups is saved successfully.

# C.	How to aggregate Data:

Have two types of aggregations: bucket and metric aggregations.

>  ![image22](http://report.h2783491.stratoserver.net/files/image22.png)

## I.	Bucket aggregations for X axis:

A bucket aggregation groups all documents into several buckets, each containing a subset of the indexed documents. The decision which bucket to sort a specific document into can be based on the value of a specific field, a custom filter or other parameters. Currently, V4 portal supports 8 bucket aggregations, as:
 
 >![image23](http://report.h2783491.stratoserver.net/files/image23.png)

Example : You can construct a Date Histogram on the timeStamp field of all events with the interval milliseconds. In this case, there will be a bucket for each milliseconds and each bucket will hold all events that have been sent in that milliseconds.

> ![image24](http://report.h2783491.stratoserver.net/files/image24.png)
 

	Below will be description for each bucket aggregations:
### a.	Date Histogram:
The date histogram aggregation requires a field of type date and an interval. It will then put all the documents into one bucket, whose value of the specified date field lies within the same interval.

Besides common interval values like minutes, hourly, daily, etc. there is the special value auto. When you select this interval, the actual time interval will be determined by V4 portal depending on how large you want to draw this graph, so that a good amount of buckets will be created (not too many to pollute the graph, nor too few so the graph would become irrelevant).

Here is each type of interval. You can select one or use Custom option to custom as other one.
 
> ![image25](http://report.h2783491.stratoserver.net/files/image25.png)

### b.	Histogram:
A histogram is pretty much like a date histogram, except that you can use it on every number field. Same as with date histogram, you specify a number field and an interval (which in this case is any number). The aggregation then builds a bucket for each interval and puts in all documents, whose value falls inside this interval.

### c.	Range
The range aggregation is like a manual histogram aggregation. You also need to specify a field of type number, but you have to specify each interval manually. This is useful if you either want differently sized intervals or intervals that overlap.

### d.	Terms:
A terms aggregation creates buckets by the values of a field. This is much like a classical SQL GROUP BY. You specify a field (which can be of any type) and it will create a bucket for each of the values that exist in that field, and put all documents in that field that have the value.

### e.	Filters:
A filter aggregation is a completely flexible (but therefore maybe slower than the others) aggregation. You just specify a filter for each bucket and all documents, that match the filter will be in that bucket. 

### f.	Significant Terms:
The significant terms aggregation can be used to find "uncommonly common" terms in a set of documents . Given a subset of documents, this aggregation finds all the terms which appear in this subset more often than could be expected from term occurrences in the whole document set. It then builds a bucket for each of the significant terms which contains all documents of the subset in which this term appears. The size parameter controls how many buckets are constructed, i. e. how many significant terms are calculated.
The subset on which to operate the significant terms aggregation can be constructed by a filter or you can use another bucket aggregation first on all documents and then choose significant terms as a sub-aggregation which is computed for the documents in each bucket.

### g.	Geohash:
Elasticsearch can store coordinates in a special type geo_point field. That way the geohash aggregation can create buckets for values close to each other. You have to specify a field of type geo_point and a precision. The smaller the precision, the larger area the buckets will cover.

## II.	We use metric aggregations for Y axis:

After you have run a bucket aggregation on your data, you will have several buckets with documents in them. You now specify one metric aggregation to calculate a single value for each bucket. The metric aggregation will be run on every bucket and result in one value per bucket.

In the visualizations the bucket aggregation usually will be used to determine the "first dimension" of the chart (e.g. for a pie chart, each bucket is one pie slice; for a bar chart each bucket will get it’s own bar). The value calculated by the metric aggregation will then be displayed as the "second dimension" (e.g. for a pie chart, the percentage it has in the whole pie; for a bar chart the actual high of the bar on the y-axis).

We have each type of metric as:
 
> ![image26](http://report.h2783491.stratoserver.net/files/image26.png)

Example: After you set up bucket aggregation on your data as 
 
> ![image27](http://report.h2783491.stratoserver.net/files/image27.png)

You now want to choose mkbps (Throughput) to specify one metric aggregation to calculate a single value for each bucket. The metric aggregation will be run on every bucket and result in one value per bucket as:
 
> ![image28](http://report.h2783491.stratoserver.net/files/image28.png)

You can click on Add Metrics to add more metric aggregation as:
> ![image29](http://report.h2783491.stratoserver.net/files/image29.png)		 

After applying changes, plots will be shown as:
 
> ![image30](http://report.h2783491.stratoserver.net/files/image30.png)

You can set up multi metrics as you want, just need to more metrics as Min/Max/Top Hit…..

Enter a string in the Custom Label field to change the display label.

You can click the Advanced link to display more customization options:

Below is description of each one:

### Metric Aggregations:

#### a.	Count:
This is not really an aggregation. It just returns the number of documents that are in each bucket as a value for that bucket. Sounds pretty simple, but is often enough for many kinds of analysis.

#### b.	Average/Sum
For the average and sum aggregations you need to specify a numeric field. The result for each bucket will be the sum of all values in that field or the average of all values in that field respectively.

#### c.	Max/Min
Like the average and sum aggregation, this aggregation needs a numeric field to run on. It will return the minimum value or maximum value that can be found in any document in the bucket for that field.

#### d.	Unique count
The unique count will require a field and count how many different / unique values exist in documents for that bucket.

#### e.	Percentiles:
A percentiles aggregation is a bit different, since it won’t result in one value for each bucket, but in multiple values per bucket. These can be shown as e.g. different colored lines in a line graph.

#### f.	Percentile Rank
The percentile ranks aggregation returns the percentile rankings for the values in the numeric field you specify. Select a numeric field from the drop-down, then specify one or more percentile rank values in the Values fields. Click the X to remove a values field. Click +Add to add a values field.

#### g.	Top Hit
A top_hits metric aggregator keeps track of the most relevant document being aggregated. This aggregator is intended to be used as a sub aggregator, so that the top matching documents can be aggregated per bucket.

The top_hits aggregator can effectively be used to group result sets by certain fields via a bucket aggregator. One or more bucket aggregators determines by which properties a result set get sliced into.


### Parent Pipeline Aggregations:

For each of the parent pipeline aggregations you have to define the metric for which the aggregation is calculated. That could be one of your existing metrics or a new one. You can also nest this aggregations (for example to produce 3rd derivative)

#### a.	Derivative
The derivative aggregation calculates the derivative of specific metrics.
#### b.	Cumulative Sum
The cumulative sum aggregation calculates the cumulative sum of a specified metric in a parent histogram
#### c.	Moving Average
The moving average aggregation will slide a window across the data and emit the average value of that window
#### d.	Serial Diff
The serial differencing is a technique where values in a time series are subtracted from itself at different time lags or period

### Sibling Pipeline Aggregations:

Just like with parent pipeline aggregations you need to provide a metric for which to calculate the sibling aggregation. On top of that you also need to provide a bucket aggregation which will define the buckets on which the sibling aggregation will run

#### a.	Average Bucket
The avg bucket calculates the (mean) average value of a specified metric in a sibling aggregation
#### b.	Sum Bucket
The sum bucket calculates the sum of values of a specified metric in a sibling aggregation
#### c.	Min Bucket
The min bucket calculates the minimum value of a specified metric in a sibling aggregation
#### d.	Max Bucket
The max bucket calculates the maximum value of a specified metric in a sibling aggregation


# D.	Visualizing Data:

To start visualizing your data, click Visualize in the side navigation.
The Visualize tools enable you to view your data in several ways. To get started, click the add button next to Search section.

 > ![image31](http://report.h2783491.stratoserver.net/files/image31.png)

There are a number of visualization types to choose from. Let’s go through now.

## I.	  Scatter Chart:

Click on Scatter chart.

>  ![image32](http://report.h2783491.stratoserver.net/files/image32.png)

Input data as:
1.	Series
2.	Dimension
3.	Time Range

> ![image33](http://report.h2783491.stratoserver.net/files/image33.png) 

Click on Create A Visualization, new Visualization will be created as:

>![image34](http://report.h2783491.stratoserver.net/files/image34.png) 

To add second Series, click on Add Series then input  Series and select Dimension as image:
 
>![image35](http://report.h2783491.stratoserver.net/files/image35.png)

Plot will be changed as:

>![image36](http://report.h2783491.stratoserver.net/files/image36.png) 

To add Y2 axis, click on Metrics & Axes as image:

>![image37](http://report.h2783491.stratoserver.net/files/image37.png) 

Then expend second dimension section
 
>![image38](http://report.h2783491.stratoserver.net/files/image38.png)

Click on Value Axis then select New Axis as image

>![image39](http://report.h2783491.stratoserver.net/files/image39.png) 

Right Axis will be created as image:

 >![image40](http://report.h2783491.stratoserver.net/files/image40.png)


Click to Save button to save the plot successfully.

## II.	  CDF Chart:

Click on CDF Plot as:

> ![image41](http://report.h2783491.stratoserver.net/files/image41.png)


Input data as:
1.	Series
2.	Dimension
3.	Time Range

 >![image42](http://report.h2783491.stratoserver.net/files/image42.png)

Then click on Create A Visualization, New Visualization page will be shown as:

 >![image43](http://report.h2783491.stratoserver.net/files/image43.png)


To add second Series, click on Add Series then input  Series and select Dimension as image:
>![image44](http://report.h2783491.stratoserver.net/files/image44.png)
 
Then click on Add, new filter and new plot will be applied as:

>![image45](http://report.h2783491.stratoserver.net/files/image45.png)
 

Click on X to remove series.

> ![image46](http://report.h2783491.stratoserver.net/files/image46.png)

To change Label of line here:
 >![image47](http://report.h2783491.stratoserver.net/files/image47.png)

Move Lable section to bottom: click on Panel Setting then set Legend Position is bottom as:
 >![image48](http://report.h2783491.stratoserver.net/files/image48.png)

Click to Save button to save the plot successfully.


## III.	 Pie Chart:

Click on Pie Range as:

 >![image49](http://report.h2783491.stratoserver.net/files/image49.png)


Input data as:
1.	Series
2.	Dimension
3.	Ranges
In sample below:
From 0 to 1 means 0 <= duration(s) < 1
From 1 to 2 means 1 <= duration(s) < 2
From 2 to 3 means 2 <= duration(s) < 3
From 4 to 5 means 4 <= duration(s) < 5
From 6        means 6 <= duration(s) 
4.	Time Range

> ![image50](http://report.h2783491.stratoserver.net/files/image50.png)

Then click on Create A Visualization, New Visualization page will be shown with series as:

> ![image51](http://report.h2783491.stratoserver.net/files/image51.png)

Click on Narrow up icon,

> ![image52](http://report.h2783491.stratoserver.net/files/image52.png)


 To view the statistical data as:

> ![image53](http://report.h2783491.stratoserver.net/files/image53.png)

Click on Add a Series, Add Series popup will be shown as:

> ![image54](http://report.h2783491.stratoserver.net/files/image54.png)



Input Series then click on Add as:

 >![image55](http://report.h2783491.stratoserver.net/files/image55.png)

The added Series will be applied as:

> ![image56](http://report.h2783491.stratoserver.net/files/image56.png)

Click on Save button to save the Pie Plot.



## IV.	 Bar Chart:

Click on Vertical Bar as:

 
>![image57](http://report.h2783491.stratoserver.net/files/image57.png)

Input data as:
1.	Series
2.	Dimension
3.	Time Range

 

Click on Create A Visualization, new Visualization will be created as:

> ![image58](http://report.h2783491.stratoserver.net/files/image58.png)

To add second Series, click on Add Series then input  Series and select Dimension as image:
 
>![image59](http://report.h2783491.stratoserver.net/files/image59.png)

Plot will be changed as:

> ![image60](http://report.h2783491.stratoserver.net/files/image60.png)

To add Y2 axis, click on Metrics & Axes as image:

> ![image61](http://report.h2783491.stratoserver.net/files/image61.png)

Then expend second dimension section
 
>![image62](http://report.h2783491.stratoserver.net/files/image62.png)

Click on Value Axis then select New Axis as image

> ![image63](http://report.h2783491.stratoserver.net/files/image63.png)

Right Axis will be created as image:

 >![image64](http://report.h2783491.stratoserver.net/files/image64.png)


Click to Save button to save the plot successfully.
.

## V.	  Stacked Bar Chart:

On left menu, click on Visualize menu item, Visualize page will be shown:

Click on Add icon, then click on Success Rate as:

 
 >![image65](http://report.h2783491.stratoserver.net/files/image65.png)

Input data as:

 > ![image66](http://report.h2783491.stratoserver.net/files/image66.png)

Then click on Create A Visualization, New Visualization page will be shown with series as:

>  ![image67](http://report.h2783491.stratoserver.net/files/image67.png)

Click on Narrow up icon,

 > ![image68](http://report.h2783491.stratoserver.net/files/image68.png)


 To view the statistical data as:

 > ![image69](http://report.h2783491.stratoserver.net/files/image69.png)

Click on Add a Series, Add Series popup will be shown.

Input Series then click on Add as: 

>![image70](http://report.h2783491.stratoserver.net/files/image70.png)

The added Series will be applied as:

 >![image71](http://report.h2783491.stratoserver.net/files/image71.png)

Add one more series as:

 >![image72](http://report.h2783491.stratoserver.net/files/image72.png)

Click on Save button to save the Plot successfully.


## VI.	  Aggregated Bar Chart:

Click on Vertical Bar as:

 >![image57](http://report.h2783491.stratoserver.net/files/image57.png)


Input data as:
a.	Series
b.	Second Series
c.	Dimension
d.	Time Range

>  ![image73](http://report.h2783491.stratoserver.net/files/image73.png)


Then click on Create A Visualization
1.	To calculate Moving Average, we need to configure Y-Axis as image below. You can also give the axis a custom label as needed.
 

 >![image74](http://report.h2783491.stratoserver.net/files/image74.png)




2.	To show daily data long the x-axis, select the X-Axis buckets type, select Date Histogram from the aggregation list, choose timeStamp  and choose Daily from the field list. You can also give the axis a custom label as needed.

 >![image75](http://report.h2783491.stratoserver.net/files/image75.png)

3.	Click Apply changes     ![image76](http://report.h2783491.stratoserver.net/files/image76.png) to view the results.
 ![image77](http://report.h2783491.stratoserver.net/files/image77.png)

Click to Save button to save the plot successfully.



## VII.	 Coordinate Map:

1.	Click New.
2.	Select Coordinate map.
 
> ![image78](http://report.h2783491.stratoserver.net/files/image78.png)

3.	Set the time window for the events we’re exploring:
4.	Click the time picker in the V4 portal toolbar.
5.	Click Relative.
6.	Set the start time and the end time as:

>  ![image79](http://report.h2783491.stratoserver.net/files/image79.png)

7.	Once you’ve got the time range set up, click the Go button and close the time picker by clicking the small up arrow in the bottom right corner.

To map the geo coordinates from the log files select Geo Coordinates as the bucket and click Apply changes  ![image76](http://report.h2783491.stratoserver.net/files/image76.png) . Your chart should now look like this:

 > ![image80](http://report.h2783491.stratoserver.net/files/image80.png)

You can navigate the map by clicking and dragging, zoom with the   ![image81](http://report.h2783491.stratoserver.net/files/image81.png)buttons, or hit the Fit Data Bounds ![image82](http://report.h2783491.stratoserver.net/files/image82.png)  button to zoom to the lowest level that includes all the points. You can also include or exclude a rectangular area by clicking the Latitude/Longitude Filter  ![image83](http://report.h2783491.stratoserver.net/files/image83.png) button and drawing a bounding box on the map. Applied filters are displayed below the query bar. Hovering over a filter displays controls to toggle, pin, invert, or delete the filter.
 
 >![image84](http://report.h2783491.stratoserver.net/files/image84.png)

Save this map with the name Map Example.

## VIII.	 Set TimeFilter for Visualization
  
On left menu, click on Visualize menu item, Visualize page will be shown 

Step 1: Click on Add icon, then click on Scatter plot
>![image85](http://report.h2783491.stratoserver.net/files/image85.png)

Step 2: Input data as:

Series: LSPO_CZ_1/3G_internet/PING/32B_znalec/32/80.250.24.26
Dimension: msec
TimeRange: Last 7 days

> ![image86](http://report.h2783491.stratoserver.net/files/image86.png)

Then click on Create A Visualization, New Visualization page will be shown. Selected Time Range will apply for Visualize TimeFilter and Global TimeFilter as:

> ![image87](http://report.h2783491.stratoserver.net/files/image87.png)

Step 3: Hover over Visualize TimeFilter, list of functions will be shown as:

 >![image88](http://report.h2783491.stratoserver.net/files/image88.png)

•	Enable Filter: 
> o	Checked: Enable Filter
>>•	Plot will be shown based on Visualize Filter.

> o	Uncheck: Disable the filter without removing it. Diagonal stripes indicate that a filter is disabled.
> ![image89](http://report.h2783491.stratoserver.net/files/image89.png)

>>•	Plot will be shown based on Global Filter.

•	Pin the filter: Pinned filters persist when we switch contexts. For example, we can pin a filter in Visualize and it remains in place when we switch to Discover as:

In Visualize: 
 > ![image90](http://report.h2783491.stratoserver.net/files/image90.png)

In Discover as:
 > ![image91](http://report.h2783491.stratoserver.net/files/image91.png)

•	Invert Filter: Switch from a positive filter to a negative filter and vice-versa.
 
>![image92](http://report.h2783491.stratoserver.net/files/image92.png)

•	 Remove Filter: Remove the filter.
 >![image93](http://report.h2783491.stratoserver.net/files/image93.png)

Step 4: Change Global TimeFilter to “Last 24 hours”, this will be applied to Visualize TimeFilter as:

> ![image94](http://report.h2783491.stratoserver.net/files/image94.png)

And plot will be changed as:
 
>![image95](http://report.h2783491.stratoserver.net/files/image95.png)

Click on Save button to save the changes successfully.


## IX.	 Clone Visualize

Click on Visualize menu item, Visualize page will be shown as:

> ![image7](http://report.h2783491.stratoserver.net/files/image7.png)

Check to select Visualization above as

> ![image96](http://report.h2783491.stratoserver.net/files/image96.png)

Then click on Copy icon as:

> ![image97](http://report.h2783491.stratoserver.net/files/image97.png)
 
Confirmation popup will be shown as:

> ![image98](http://report.h2783491.stratoserver.net/files/image98.png)

Click on Clone button, new Visualization will be copied successfully as:

> ![image99](http://report.h2783491.stratoserver.net/files/image99.png)


# E.	Dashboard:

To build a Dashboard:
## 1.	Go to V4 Portal then click on Dashboard on Left Menu:
 
>![image100](http://report.h2783491.stratoserver.net/files/image100.png)

Dashboard page will be shown. Then click on Add button to add new one as:

> ![image101](http://report.h2783491.stratoserver.net/files/image101.png)

Click on Add to add visualization as:

> ![image102](http://report.h2783491.stratoserver.net/files/image102.png)

Then select a Plot with TimeFilter and a Plot without TimeFilter as:

> ![image103](http://report.h2783491.stratoserver.net/files/image103.png)

Visualization which has TimeFilter, it will be shown at Top Right of Plot as:

 
>![image104](http://report.h2783491.stratoserver.net/files/image104.png)

Change Global TimeFilter from “Last 24 hours” to “Last 7 days”,
it will apply to Plot without TimeFilter as:

> ![image105](http://report.h2783491.stratoserver.net/files/image105.png)

Click on Save button to save dashboard successfully.

## 2.	Find And Replace:

Go to Dashboard page, Find And Replace function will be available as:

 >![image106](http://report.h2783491.stratoserver.net/files/image106.png)

For easy view, we use a Dashboard with design as below:

>![image107](http://report.h2783491.stratoserver.net/files/image107.png)
 

Series of each Plot as below:
	Series for Plot 1:
> ![image108](http://report.h2783491.stratoserver.net/files/image108.png)

	Series for Plot 2:
> ![image109](http://report.h2783491.stratoserver.net/files/image109.png)

	Series for Plot 3:
> ![image110](http://report.h2783491.stratoserver.net/files/image110.png)

	Series for Plot 4:

> ![image111](http://report.h2783491.stratoserver.net/files/image111.png)

Summary for series of Plots list:
>![image112](http://report.h2783491.stratoserver.net/files/image112.png)	 

a.	On Dashboard, click on Find And Replace button:

> ![image113](http://report.h2783491.stratoserver.net/files/image113.png)	

b.	Input Find series and Replace with as:

>![image114](http://report.h2783491.stratoserver.net/files/image114.png)	
 

c.	Click on “Replace” button, first plot which contains find series will be changed. In this case Plot 1 will be affected as below:

 >![image115](http://report.h2783491.stratoserver.net/files/image115.png)	

Dashboard will be changed as:

 >![image116](http://report.h2783491.stratoserver.net/files/image116.png)	

d.	Click on Find And Replace button then input as:
> ![image117](http://report.h2783491.stratoserver.net/files/image117.png)	

e.	Click on “Replace all“ button, all plots which contains find series on current Dashboard will be changed. In this case Plot 1, 2 will be affected as below:

> ![image118](http://report.h2783491.stratoserver.net/files/image118.png)	

Dashboard will be changed as:

> ![image119](http://report.h2783491.stratoserver.net/files/image119.png)	


## 3.	Lazy loading for the plots on a dashboard:
On left menu, click on Dashboard menu item, Dashboard page will be shown as:

 > ![image120](http://report.h2783491.stratoserver.net/files/image120.png)


Click on name of Dashboard to open. Top 6 plots will be loaded as:

>![image121](http://report.h2783491.stratoserver.net/files/image121.png)

Others will be shown when scrolling as:

>![image122](http://report.h2783491.stratoserver.net/files/image122.png)

## 4.	Export and Schedule Dashboard:

### a.	Export Selected Report:
On left menu, click on Dashboard menu item, Dashboard page will be shown.
Then click on Report button (pdf icon) as:
>![image123](http://report.h2783491.stratoserver.net/files/image123.png)	 

-	A Dialog will be shown with setting defaults as:
PDF checkbox is checked as default.
Dashboard checkbox is checked as default.
Time Zone is loaded with current client time zone.
> ![image124](http://report.h2783491.stratoserver.net/files/image124.png)

-	User can do more optional settings as:
o	Check on Excel checkbox to include Excel file.
o	Check on Chart Per Page to change Dashboard Type
o	Input Email then click on Add button to receive email.
Note: user can add multiple emails when repeat this step.

Or User can click on Delete icon to remove email.
o	Change Time Zone to another one.
 >![image125](http://report.h2783491.stratoserver.net/files/image125.png)

o	User can click on Cancel button to close popup.

-	Then click on OK button, message when generating:
> ![image126](http://report.h2783491.stratoserver.net/files/image126.png)

Message after competed:
 
>![image127](http://report.h2783491.stratoserver.net/files/image127.png)

-	Click on Download PDF:
>![image128](http://report.h2783491.stratoserver.net/files/image128.png)
 
-	With Type as Dashboard, PDF will be as Dashboard as:
> ![image129](http://report.h2783491.stratoserver.net/files/image129.png)

-	Click on Download Excel to download as:
> ![image130](http://report.h2783491.stratoserver.net/files/image130.png)

-	After generating, report will be listed on Report list of Dashboard. Click on Show Report List icon to view Report List of Dashboard as:
> ![image131](http://report.h2783491.stratoserver.net/files/image131.png)

Report list of Dashboard will be shown as:
> ![image132](http://report.h2783491.stratoserver.net/files/image132.png)

> User can click on Download XLSX to download excel file.

> User can click on Download PDF to download pdf file.


-	Check mail: a report will be sent to inputted list of users as:
> ![image133](http://report.h2783491.stratoserver.net/files/image133.png)

Open attachment:

> ![image134](http://report.h2783491.stratoserver.net/files/image134.png)

With Dashboard Type as Dashboard, Attached PDF will be as Dashboard as:

>![image135](http://report.h2783491.stratoserver.net/files/image135.png)

 
Attachment Excel file as:
> ![image130](http://report.h2783491.stratoserver.net/files/image130.png)

Data in Excel file will be matched with output from Discover page with the same series and Time Range as:
> ![image137](http://report.h2783491.stratoserver.net/files/image137.png)


### b.	Schedule Report:

-	Click on Show Schedule List as:
 >![image138](http://report.h2783491.stratoserver.net/files/image138.png)

Screen will be shown as:
> ![image139](http://report.h2783491.stratoserver.net/files/image139.png)

-	Validated message when click on Add Task but missing Title  & Email as:
> ![image140](http://report.h2783491.stratoserver.net/files/image140.png)

Validated message when missing Email as:
>  ![image141](http://report.h2783491.stratoserver.net/files/image141.png)

-	Set up Daily, Weekly and Monthly as:

Title: title of task

Type: Daily/Weekly/Monthly

•	Daily setting example:
>  ![image142](http://report.h2783491.stratoserver.net/files/image142.png)

Run daily at #Time with #Time in [0, 23]. Example above, Task will run daily at 7 Europe/Berlin.

•	Weekly setting example:
>  ![image143](http://report.h2783491.stratoserver.net/files/image143.png)

Run weekly at #Time with #Time in [0, 23] and Days of the Week. Example above, Task will run weekly at 7 Europe/Berlin on Saturday.

•	Monthly setting example:
 > ![image144](http://report.h2783491.stratoserver.net/files/image144.png)

Run monthly at #Time with #Time in [0, 23] and Days in month. Example above, Task will run monthly in 20th at 7 Europe/Berlin.

•	Start and End Time

•	Layout: 
  >> Dashboard: show layout as Dashboard format.

  >> Chart Per Page: show each visualization on one page.

•	Active:
>>Checked : active

>>Unchecked: inactive

•	Emails: can add multiple emails as:
 > ![image145](http://report.h2783491.stratoserver.net/files/image145.png)

-	List of Tasks will be shown as:
>  ![image146](http://report.h2783491.stratoserver.net/files/image146.png)

-	Click on Report List icon to view list of reports for each schedule as:
 > ![image147](http://report.h2783491.stratoserver.net/files/image147.png)

> ![image148](http://report.h2783491.stratoserver.net/files/image148.png)
 
Click on Download PDF link to download PDF report.
-	At scheduled time, report will be sent as:
>  ![image149](http://report.h2783491.stratoserver.net/files/image149.png)

List of emails as:
 > ![image150](http://report.h2783491.stratoserver.net/files/image150.png)

-	Deactivate a Task as:
>  ![image151](http://report.h2783491.stratoserver.net/files/image151.png)

-	Delete a Task as:
 > ![image152](http://report.h2783491.stratoserver.net/files/image152.png)

Task is deleted as:
>  ![image153](http://report.h2783491.stratoserver.net/files/image153.png)

-	Email for daily report:
 > ![image154](http://report.h2783491.stratoserver.net/files/image154.png)

-	Email for weekly report:
 > ![image155](http://report.h2783491.stratoserver.net/files/image155.png)

-	Email for monthly report:
>  ![image156](http://report.h2783491.stratoserver.net/files/image156.png)

-	Attachment for ChartPerPage Type:
 
> [ChartPerPage_Type](http://report.h2783491.stratoserver.net/files/ChartPerPage_Type.pdf)

-	Attachment for Dashboard Type:

> [Dashboard_Type](http://report.h2783491.stratoserver.net/files/Dashboard_Type.pdf) 




# F.	User can only see its own/shared/public visualizations or dashboards:
## 1.	Create private Visualization as default:
 
Step 1: On left menu, click on Visualize menu item, Visualize page will be shown

Step 2: Click on Add icon, then click on CDF plot as:

 > ![image157](http://report.h2783491.stratoserver.net/files/image157.png)

Step 3: Input data then Save, New Visualization will be created as:

 > ![image158](http://report.h2783491.stratoserver.net/files/image158.png)

Step 4: Click on gear icon on Actions column, Action popup will be shown as:

 > ![image159](http://report.h2783491.stratoserver.net/files/image159.png)

The created Visualization is private as default.

## 2.	Set public Visualization:

Step 1: create a New Visualization as:

 > ![image160](http://report.h2783491.stratoserver.net/files/image160.png)

Step 2: Click on gear icon on Actions column then check on “Is Public” as:

 
> ![image161](http://report.h2783491.stratoserver.net/files/image161.png)

Then click on OK button, selected Visualization set to Public Visualization.

## 3.	Share a Visualization for Users:

Step 1: create a New Visualization as:

 >![image162](http://report.h2783491.stratoserver.net/files/image162.png)
 
Step 2: Click on gear icon on Actions column then input/select AccountName into Sharing to Users.
Then click on Add, AccountName will be added successfully as:
 
>![image163](http://report.h2783491.stratoserver.net/files/image163.png)
 
Click on OK button, selected Visualization will be shared to added Account.

## 4.	Share a Visualization for Groups:

Step 1: create a New Visualization as:

>  ![image164](http://report.h2783491.stratoserver.net/files/image164.png)

Step 2: Click on gear icon on Actions column then input/select GroupName into Sharing to Groups.
Then click on Add, GroupName will be added successfully as:

 > ![image165](http://report.h2783491.stratoserver.net/files/image165.png)

With Group1 contains two users as:
 > ![image166](http://report.h2783491.stratoserver.net/files/image166.png)

Click on OK button, selected Visualization will be shared to added Group.


## 5.	Create private Dashboard as default:

Step 1: Click on Dashboard menu item, Dashboard page will be shown. Then click on Add button to add new one 

Step 2: Click on Add to add visualization

Click on the Plot above to add into Dashboard.

Then click on Save, New Dashboard will be created as:

>  ![image167](http://report.h2783491.stratoserver.net/files/image167.png)

Step 3: Click on gear icon on Actions column, Action popup will be shown as:

>  ![image168](http://report.h2783491.stratoserver.net/files/image168.png)

The created Dashboard is private as default.

## 6.	Set public Dashboard:

Step 1: create a New Dashboard as:

>  ![image169](http://report.h2783491.stratoserver.net/files/image169.png)

Step 2: Click on gear icon on Actions column then check on “Is Public” as:

 
> ![image170](http://report.h2783491.stratoserver.net/files/image170.png)

Then click on OK button, selected Dashboard set to Public Dashboard.

## 7.	Share a Dashboard for Users:

Step 1: create a New Dashboard as:

 > ![image171](http://report.h2783491.stratoserver.net/files/image171.png)

Step 2: Click on gear icon on Actions column then input AccountName into Sharing to Users.
Then click on Add, AccountName will be added successfully as:
>![image172](http://report.h2783491.stratoserver.net/files/image172.png)
 
Click on OK button, selected Dashboard will be shared to added Account.


## 8.	Share a Dashboard for Groups:

Step 1: create a New Dashboard as:

> ![image173](http://report.h2783491.stratoserver.net/files/image173.png)

Step 2: Click on gear icon on Actions column then input GroupName into Sharing to Groups.
Then click on Add, GroupName will be added successfully as:
>![image174](http://report.h2783491.stratoserver.net/files/image174.png)
 
With Group1 contains two users as:
 
>![image166](http://report.h2783491.stratoserver.net/files/image166.png)

Click on OK button, selected Dashboard will be shared to added Account.

## 9.	User can see its own and Share/Public Visualizations/Dashboards:

Step 1: Launch Portal V4  http://h2783491.stratoserver.net:8080

Step 2: Log in Portal with account as:
	
> User: kapilantest

> Pass: 123456

Step 3: On left menu, click on Visualize menu item, Visualize page will be shown as:

 >![image175](http://report.h2783491.stratoserver.net/files/image175.png)

User can see its own Visualizations and Share/Public Visualizations

Step 4: On left menu, click on Dashboard menu item, Dashboard page will be shown as:
>![image176](http://report.h2783491.stratoserver.net/files/image176.png)
 
User can see its own Dashboards and Share/Public Dashboards.

# G.	Group of users:
## 1.	Add Users to Groups:

Step 1: Log in Portal V4 with account as:

	> Username: kapilan
	> Password: 123456
	
Step 2: Then click on Permissions

> ![image177](http://report.h2783491.stratoserver.net/files/image177.png)

Step 3: Click on Users, select User and click on Edit icon as

> ![image178](http://report.h2783491.stratoserver.net/files/image178.png)

Step 4: Click on Add Group button
•	Select existing Group from dropdown
•	Or input New Group Name
Then Submit

> ![image179](http://report.h2783491.stratoserver.net/files/image179.png)

Selected User is added to Group1 as:

 
>![image180](http://report.h2783491.stratoserver.net/files/image180.png)




	Add Users to Groups as below:
|Users |Groups   | 
|-----------|:-----------:|
| kapilan | Group2 |
| hoang	| Group1|
| hoangnguyen	| Group1, Group2|


## 2.	Add Groups/Users to Probes:


Step 1: Click on Permissions menu item 

> ![image181](http://report.h2783491.stratoserver.net/files/image181.png)

Step 2:Then click on Probe Access button, Edit Probe page will be shown.
	

Step 3: Click on Edit icon of a probe, Edit Probe page will be shown:

	 
>![image182](http://report.h2783491.stratoserver.net/files/image182.png)



Step 4: Click on Add User and Add Group then Submit as

>![image183](http://report.h2783491.stratoserver.net/files/image183.png)

User and Group will be added successfully and show on Probes list as:

 
>![image184](http://report.h2783491.stratoserver.net/files/image184.png)

Step 5: Check Probe Permission:

Set up Users/Groups for probes as below:
| Probe| Users	| Groups|
|-----------|:-----------:|-----------:|
| Dell15-WLTTE| hoangnguyen| | 
| Hybrid_access_N_4| hoangnguyen|Group2(hoangnguyen, kapilan) |	
| LAN-PC| hoangnguyen| |	
| LSPO_CZ_2| | Group1(hoang, hoangnguyen)| 
| LSPO_NL_HHH_1| |Group2(hoangnguyen, kapilan) |	
| TMA3| hoang| |		 
| TMA4| hoang	 | |		
	
	 	
	 	
		 
	

Login into Portal V4, on Discover page or Add/Edit Visualization page, probe access for each User as below:

a.	For kapilan account:

Click on Discover menu item, click on Get Series, list of available Probes:

>![image185](http://report.h2783491.stratoserver.net/files/image185.png) 

b.	For hoang account:

Click on Discover menu item, click on Get Series, list of available Probes:
 
>![image186](http://report.h2783491.stratoserver.net/files/image186.png)

c.	For hoangnguyen account:

Click on Discover menu item, click on Get Series, list of available Probes:
>![image187](http://report.h2783491.stratoserver.net/files/image187.png)
 

	Summary permission is as below:
| Users| Probe| 
|-----------|:-----------:|
|hoang| LSPO_CZ_2,	TMA3,	TMA4| 
|hoangnguyen| Dell15-WLTTE, 	Hybrid_access_N_4,	LAN-PC,	LSPO_CZ_2,	LSPO_NL_HHH_1| 	
|kapilan	| Hybrid_access_N_4,	LSPO_NL_HHH_1| 	
	


## 3.	Delete Group from User:


Step 1: Click on Permissions menu item 

 > ![image177](http://report.h2783491.stratoserver.net/files/image177.png)

Step 2: Then click on Users button, Edit Users page will be shown.
	

Step 3: Click on Edit icon of an User, Edit Users page will be shown:

	 
>![image188](http://report.h2783491.stratoserver.net/files/image188.png)



Step 4: Click on Delete icon then Submit as

> ![image189](http://report.h2783491.stratoserver.net/files/image189.png)

Confirmation will be shown:

>  ![image190](http://report.h2783491.stratoserver.net/files/image190.png)

After confirmation, Group will be removed successfully as:

> ![image191](http://report.h2783491.stratoserver.net/files/image191.png)

Click on Submit to apply the changes as:

> ![image192](http://report.h2783491.stratoserver.net/files/image192.png)

## 4.	Delete User/Group from Probe:


Step 1: Click on Permissions menu item 

 > ![image177](http://report.h2783491.stratoserver.net/files/image177.png)

Step 2:  Then click on Probe Access button, Edit Probe page will be shown.
	

Step 3: Click on Edit icon of a probe, Edit Probe page will be shown:

	 
> ![image193](http://report.h2783491.stratoserver.net/files/image193.png)



Step 4: Click on Delete icon to delete Group then Submit as

>  ![image194](http://report.h2783491.stratoserver.net/files/image194.png)

Confirmation will be shown:

 > ![image195](http://report.h2783491.stratoserver.net/files/image195.png)

After confirmation, Group will be removed successfully as:

 > ![image196](http://report.h2783491.stratoserver.net/files/image196.png)

Click on Submit to apply the changes as:

 
> ![image197](http://report.h2783491.stratoserver.net/files/image197.png)

Step 5: Check Probe Permission:

After remove Group from User and Probe, permission for probes as below:

| Probe| Users	| Groups|
|-----------|:-----------:|-----------:|
| Dell15-WLTTE| hoangnguyen| | 
| Hybrid_access_N_4| hoangnguyen||	
| LAN-PC| hoangnguyen| |	
| LSPO_CZ_2| | Group1(hoang, hoangnguyen)| 
| LSPO_NL_HHH_1| |Group2(kapilan) |	
| TMA3| hoang| |		 
| TMA4| hoang	 | |
 

Login into Portal V4, on Discover page or Add/Edit Visualization page, probe access for each User as below:

a.	For kapilan account:

Click on Discover menu item, click on Get Series, list of available Probes:

> ![image198](http://report.h2783491.stratoserver.net/files/image198.png)

b.	For hoang account:

Click on Discover menu item, click on Get Series, list of available Probes:
> ![image186](http://report.h2783491.stratoserver.net/files/image186.png)

c.	For hoangnguyen account:

Click on Discover menu item, click on Get Series, list of available Probes:

> ![image199](http://report.h2783491.stratoserver.net/files/image199.png)

	Summary permission is as below:
| Users| Probe| 
|-----------|:-----------:|
|hoang| LSPO_CZ_2,	TMA3,	TMA4| 
|hoangnguyen| Dell15-WLTTE, 	Hybrid_access_N_4,	LAN-PC,	LSPO_CZ_2,	~~LSPO_NL_HHH_1~~| 	
|kapilan	| ~~Hybrid_access_N_4~~,	LSPO_NL_HHH_1| 	
	

# H.	Redirect to Alarm Page


On left menu, click on Alarm menu item as
		
>![image200](http://report.h2783491.stratoserver.net/files/image200.png)		 

		Alarm page will be shown as:

>![image201](http://report.h2783491.stratoserver.net/files/image201.png)	 

All functions will be worked as this user log in http://alarmv4.h2746383.stratoserver.net

# I.	Discover:

We can interactively explore our data from the Discover page. We have access to every document in every index that matches the selected index pattern. We can submit search queries, filter the search results, and view document data. We can also see the number of documents that match the search query and get field value statistics. If a time field is configured for the selected index pattern, the distribution of documents over time is displayed in a histogram at the top of the page.
>  ![image223](http://report.h2783491.stratoserver.net/files/image223.png)

## 1.	Setting the Time Filter:
The time filter restricts the search results to a specific time period. 

By default the time filter is set to the last 15 minutes. You can use the Time Picker to change the time filter or select a specific time interval or time range in the histogram.

To set a time filter with the Time Picker, click Time Picker images in the V4 Portal toolbar.
We have 3 types of setting:

-	Quick time filter:
  >![image224](http://report.h2783491.stratoserver.net/files/image224.png)

-	Relative time filter:
 
> ![image225](http://report.h2783491.stratoserver.net/files/image225.png)

-	Absolute time filter”
 
> ![image226](http://report.h2783491.stratoserver.net/files/image226.png)

Click the caret in the bottom right corner to close the Time Picker.
>  ![image227](http://report.h2783491.stratoserver.net/files/image227.png)

To move forward/backward in time, click the arrows to the left or right of the Time Picker:
>  ![image228](http://report.h2783491.stratoserver.net/files/image228.png)

## 2.	Searching Data:

a.	Search Criteria:
To search data, enter search criteria in the Query bar and press Enter or click Search
Example: We have 1162 events in Time Period as image below.
 
> ![image229](http://report.h2783491.stratoserver.net/files/image229.png)

We can use some of Search Criteria as following: 
-	Free text search:
Input free text into Query Bar as “juergen” then click on Search icon, output will be 100 events for inputted key search.
 
> ![image230](http://report.h2783491.stratoserver.net/files/image230.png)

b.	Saving and Opening Searches:
To save the current search:
Click Save in the V4 Portal toolbar.
Enter a name for the search and click Save.
> ![image231](http://report.h2783491.stratoserver.net/files/image231.png)

To load a saved search into Discover:
Click Open in the V4 Portal toolbar.
Select the search you want to open.
> ![image232](http://report.h2783491.stratoserver.net/files/image232.png)

3.	Filtering By Data:
We can filter the search results to display only those documents that contain a particular value in a field. We can also create negative filters that exclude documents that contain the specified field value.
-	To add a filter from the Documents table:
>o	Expand a document in the Documents table by clicking the Expand button  ![image233](http://report.h2783491.stratoserver.net/files/image233.png)  to the left of the document’s table entry.
>o	To add a positive filter, click the Positive Filter button ![image234](http://report.h2783491.stratoserver.net/files/image234.jpeg)  to the right of the field name. This includes only those documents that contain that value in the field.
>o	To add a negative filter, click the Negative Filter button ![image235](http://report.h2783491.stratoserver.net/files/image235.jpeg)  to the right of the field name. This excludes documents that contain that value in the field.
>o	To filter on whether or not documents contain the field, click the Exists button  ![image236](http://report.h2783491.stratoserver.net/files/image236.jpeg) to the right of the field name. This includes only those documents that contain the field.

> ![image237](http://report.h2783491.stratoserver.net/files/image237.png)


-	Managing Filters:
To modify a filter, hover over it and click one of the action buttons.
>![image238](http://report.h2783491.stratoserver.net/files/image238.png)
 
>o	Enable Filter: Disable the filter without removing it. Click again to reenable the filter. Diagonal stripes indicate that a filter is disabled.

> ![image239](http://report.h2783491.stratoserver.net/files/image239.png)

>o	Pin the filter: Pinned filters persist when we switch contexts in V4 Portal. For example, we can pin a filter in Discover and it remains in place when we switch to Visualize. Note that a filter is based on a particular index field—if the indices being searched don’t contain the field in a pinned filter, it has no effect.

>  ![image240](http://report.h2783491.stratoserver.net/files/image240.png)

>o	 Invert Filter: Switch from a positive filter to a negative filter and vice-versa.

>o	 Remove Filter: Remove the filter.

# J. Document Revision: 

This table records the status and version history of this document:
| Version | Date | Author |  Status (draft, peer review etc) | Version History |
|-----------|:-----------:|:-----------:|:-----------:|-----------:|
| 1.0 | 05/07/2018 | Lien	|  draft  |  | 
| 1.1 | 05/10/1018 | Kapilan|  review  |  | 
| 1.2 | 05/21/2018 | Lien	|  Update  | - Add scatter plot with 100 samples
|  |  | |   |-	Filters| 	
| 1.3 | 11/16/2018 | Lien	|  Update|  -	Search series & Find And Replace -	Redirect to Alarm Page-	Order the dimension based on the popularity-	How to add a Custom Pie Visualization-	Manage User and Probe Access Permissions-	Multiple Series for Scatter Plot-	Save Last Modified of Visualize-	How to add a Custom CDF and Vertical Bar Visualization-	Lazy loading for the plots on a dashboard-	Set Visualize TimeFilter and Global TimeFilter-	Use just Global TimeFilter in Dashboard-	Add feature that a user can only edit its own visualisations or dashboards-	Implement group of user as for V3-	Clone Visualize-	How to add a SuccessRate Visualization-	Report| 
| 1.4 | 1/2/2019 | Lien	|  Update| -	Send Dashboard via email-	Schedule Report | 
| 1.5 | 1/21/2019 | Lien	|  Update|-	How to add Y2 axis for: D.I – Scatter Chart. D.IV- Bar Chart  | 	
| 1.5 | 2/17/2019 | Lien	|  Update| B.II. Configuration -> 4. Change password | 
| 1.5 | 2/19/2019 | Lien	|  Update|B.III. Add Probe  | 
| 1.5 | 4/20/2019 | Lien	|  Update|  D. II. CDF Chart: page 28-32-	E. Dashboard: page 68-83| 			
| 1.5 | 5/03/2019 | Lien	|  Update|  F. User can only see its own/shared/public visualizations or dashboards|
