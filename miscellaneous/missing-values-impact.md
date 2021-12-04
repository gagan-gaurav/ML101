# Missing values Impact

Missing values can sometimes tell you how strongly the presence or absence of one variable affects the presence of another.

&#x20;To visualize the correlation between different columns based on the missing values, use missingno.dendogram.&#x20;

The dendrogram uses a hierarchical clustering algorithm to bin variables against one another by their nullity correlation. Cluster leaves which linked together at a distance of zero fully predict one another's presence.

![Code for missingo](<../.gitbook/assets/image (28).png>)

![](<../.gitbook/assets/image (29).png>)
