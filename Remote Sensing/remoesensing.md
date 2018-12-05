---
title : Remote Sensing Lab 4
---

![schaferbien_unsupervised_classification100](https://user-images.githubusercontent.com/42807889/49521664-f62ef480-f873-11e8-97dd-85377a1d112f.jpg)

Unsupervised Classification Answer Sheet
[1] Examine the Laurel image closely. Zoom into the image and pan around.  List 6-10 categories of features that are evident in the image (e.g., roads, etc).

•	Vegetation

•	Roads

•	Structures

•	Bare earth

•	Water

•	shadow

	[2] Using the swipe tool over the original image what features do the four colors represent?

o	Class 2 __vegetation/shadows

o	Class 3 __more dense vegetation

o	Class 4 __bare earth

o	Class 5 __seems like structure (buildings)

[3] How do the classes shown in your unsupervised classification compare to the number/type  of features you expected (as indicated when you examined the image before processing)?

There relatively close to my predictions.  The classification brings out contrast of the different traits the various type of forest and shadow was more evident. The structures popped out more with the classification.

[4] What features were not included (or drawn out) in your unsupervised classification?

Water wasn’t drawn out differently since there were only 5 classes (4 without black frame). Roads were drawn out but you could confuse the roads with bare earth.

[5] What happened to them (and can you explain why they were discarded)?

Some of them could of got grouped with similar pixels and blend in not being separated.  The bare earth and roads had similar characteristics so because of the limit of 5 classes it grouped the similar pixel counts.

[6] What does this stippling represent (compare the unsupervised classification to the original image) and why do you think it occurs given the parameters of the unsupervised classification?

The stippling occurs because of the classification process running it since the process looks for similar pixel counts and groups them together so that they can be separated and be part of a distinct feature on the map. The process looks for the pixels in a set range in the histogram to group and picks out very drastic changes in pixels.

[7] Do you think that increasing the number of classes will reduce or increase the amount of stippling? Why?

There would be definitely more stippling because the process is going to digger deeper into the pixel histogram and pick out ones that have a smaller range of pixel values since there is more classes of classification. For example there could be more stippling on building with having shadows casting as a separate feature while the previous unsuperclassification just showed the two features as one color or class. It separates the pixel range even more giving you more set ranges of different pixel types.

[8] Did the amount of stippling for, say the forested areas, increase or decrease and how does the increase in sample interval explain the change?

The stippling increased in the forest areas; you can tell more pixels were picked up in that set range.  Changing the sample interval changes the range at which ever classified group of values was selected for that classification. The histogram changed in what the range picked up to the different pixel values. There is a bigger sample being collected here classifying more pixels into more groups.

[9] How did increasing the Sample Interval affect the output Unsupervised Classification?  Compared to the original image what features where enhanced (or lost) given the higher sample interval?

One thing that I realized was when I looked at the gray roads the interval classification one seemed to have a fuller polygon shape that didn’t have as many pixels missing then it did in the regular classification. The structures that are impervious labeled gray seemed to have a finer edge compared to the first classification process. Also I found that there is more stippling in the forest areas where certain pixels were picked up and classified.

[10] Compared to the 4 class image what features where enhanced (or brought out/separated) given the higher number of classes?

The features that were enhanced that I saw at bookmark A was that bare earth seem to stand out more for me showing the area around buildings and edges. Roads were pulled out in this 8 class classification, so you could tell that it was grouped with a class of impervious material. The vegetation showed me more stippling with a third layer on top of the vegetation.  Book mark B shows that water/ river systems are drawn out in its own category this time and easily distinguishable compared to the 4 class image. Book mark C shows more of the road infrastructure better and shows the edges of the borders of the different features such as bare earth, roads, buildings and impervious materials. Impervious materials from the previous classification were separated into two different classes, as well as vegetation and shadow.

[11] How did increasing the number of classes change the Unsupervised Classification (i.e., what new features or class breakdowns are evident with more classes)?

With more classes added you can see that impervious material was broken down into a couple new classifications. The vegetation and shadow in the forested areas were broken down once more showing 3 different color stippling. When you look closer since there were more classes bare earth group got broken down more. Water is separated as a new group, even road structure seems to be separated as a new group.



[12]When you examined Bookmarks A, B, and C for the 8 Class Unsupervised Classification to the Laurel_1 image how did the following features change when compared to the 4 Class Unsupervised Classification? (e.g., was there more or less “class” confusion (features were much more confused or much more defined, etc.)

forested areas:  more stippling has 1 extra color, for me it was more confusing since we already had vegetation and shows. The extra class could have been grouped to one of them other classes.

 urban areas (buildings, parking lots): The image got sharper in these areas the edges were more well defined and the extra classes actually cleared up confusion.

 roads: The roads were more well defined the extra class split the impervious class better so that the feature of roads was easier to distinguish.

 water: One of the extra classes separated out water to its own class helping me tell the difference between water and vegetation in the previous classification.

 shadows: To me the shadows got harder to distinguish because of the extra third color, too much was going on and could use grouping to clarify the image better.

[13] Is there any overlap in classes with respect to the features they represent? In other words, is/are there features in the image that are represented by more than one class?
The third color in shadows represents overlap, some of the semi bare earth overlaps with other bare earth. The lines of roads over lap with roads.

[14] Go to Bookmark B and swipe the 8 class Unsupervised Classification over the Laurel_1 image.  What does class 2 (the Ginger Pink) represent?
I want to say the class 2 represents water  more dominantly but there is some stippling within the forested areas more so on the darker shade of the image.

[15] Go to Bookmark D and swipe the 8 class Unsupervised Classification over the Laurel_1 image.  Compared to the information presented in Bookmark B what is the problem with the Unsupervised Classification results with the features shown in the area of Bookmark D?

Only some of the pixels values got sorted right, for example the water was showing up as impervious materials while it should be ginger pink representing water. The classification picked up that feature as a different type of pixel and grouped incorrectly by our way of classification.

[16] How did increasing the Sample Interval, with the higher class number,  affect the output Unsupervised Classification?
Well based on the amount of classes added the output allowed for more areas of study to pop out more. For example water and roads were big ones that were more easily distinguished. Changing the interval of the sample size allowed for the range of pixels being scanned to be grouped more accurately based on the pixel count in the image allowing for more stippling and classification of different characteristics.

[17] Compared to the original image what features where enhanced (or lost) given the higher sample interval?
The edges of buildings and bare earth were enhanced so you could tell where the border ended or began. Roads and water were brought out more in the classification as a separate class. Structures had more defined edges and you can clearly see the man made structures easier. The forested areas in my opinion was lost because of the amount of confusion going on and the stippling that forest  classifications had.

[18] Based on this example would you suggest using a higher sample interval for the unsupervised classification? Why (or why not)?

I would recommend the higher sample interval classification to a point where its reasonable easy to read. The higher the interval sampling the contrasting the pixels will be from each other is easier to break down into groups until repetitive attributes such as what we seen in the forested area stippling. In this case I would recommend the high sample interval and more classes because you were able to see more features that you couldn’t discern from the previous image. I say in this case it would be good to use the bigger sample size but if you past a certain limit the image gets too complicated to group what everything represents.
