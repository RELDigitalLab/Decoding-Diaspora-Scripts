


Map Corrections and Worldsheets for Map v1.3 Notes and Issues:
This map takes coordinates from the first version of coordinates in the metadata spreadsheet and corrects them. The issues were that some of the locations were incorrect.

It then creates Excel statements to adjust duplicate coordinates so that they do not stack on Google MyMaps. This was done by writing scripts that 1) identify duplicates using conditional statements in Excel, 2) add .01 to each duplicate longitude (or in some cases, a hot fix to the latitude by adding .01). I accomplished this by taking the absolute value of a coordinate component, creating an addition statement to add .01, then multipling that by a coordinate coefficient (coordinate^2/coordinate) to bring the revised coordinate to the proper side of 0 degrees (i.e. -/+) and then a revision of the coordinates. This involved CONCATETATE, ABS, *, /, and SUM statements. 

There are some known sorting issues in that the sequence of some lines are bit off. I recommend reordering either manually while cleaning the data or within a user-friendly client before or after import. 
 
Known issues with using Scalar 
Current Issues:
-Commas in datas cause issues with delimiter
-Multiple pages are created in Scalar with duplicate entries
-Scalar urls are case-sensitive.
