# Pie Charts in R Studio, R version 4.5.1

## Pie Chart (base)

>Category1 <- c(“Name1”, “Name2”)

*#Category1 = Functional groups*

*#Name1 = Name of each functional group*

>Category2 <- c(1,2)

*#Category2 = Count of proteins in each functional group*

>DataName <- data.frame(Category1, Category2)

>mycolors <- c("red", "orange", "dodgerblue4", "blue", "deepskyblue", "green4", "green2", "mediumorchid4", "mediumorchid2",
"maroon2", "goldenrod", "paleturquoise4", "paleturquoise2", "seashell2", "seashell4")

>png("Filename.png", width = 800, height = 800)

*#Width and height values are in pixels*

>pie(DataName$Category2, labels = NULL, cex = #, main = “Title”, col = mycolors)

*#cex changes the label font size*

*#base pie command keeps order of Category1*

*#Removes label names, replaces them with numbers that can be removed in Illustrator*

>legend(“right”, legend = Category1, fill = mycolors, cex = #)

*#Add legend. Can use bottomright, bottom, bottomleft, left, or combos with top.*

*#Legend overwrites part of pie chart. Generate pie chart w/ and w/o legend and crop if needed.*

>dev.off()

*#Clears previous figure.*

*#Files save to working directory.*
