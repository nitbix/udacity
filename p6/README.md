# Data Visualization project

## Summary 
This project focuses on a visualization for the "Prosper Loan Dataset". The
visualization represents how much loan volume has been processed through
prosper, organised by state where the Borrower resided. The main finding that
this visualization is trying to portray is that most of the processed loans are
based in CA, with a few other states trailing behind, and only residual volume
anywhere else.

## Design
This started as a bar chart. The visualization was very cluttered because there
were 50 bars, and a lot of labels at the bottom. After the first suggestion, I
changed it to a pie chart, with the first 5 states listed, and the rest grouped
under "other". After the second feedback, it was clear that something
more had to be done to make the visualization more attractive and clear.
Unfortunately dimple.js does not natively support choropleths, so I had to be
creative. I found a library built on top of d3 that could help build a
choropleth (http://datamaps.github.io/), so I opted for this. The third
suggestion was a very simple one and easy to fix, by adding state labels to the
map.

##Feedback

####1
The bar chart is very cluttered, and even if it can be seen that there is a
dominant state, the confusion in labels makes it hard to read. One of the bars
is missin a label.

####2
I like the fact that you can clearly tell that California has a lot more volume,
but I would also like to know about the smaller states.

####3
I am never sure which state is which. Can you add labels? Also, is there any
supplementary data you can provide? Maybe one state got more loans because on
average people do better economically?

##Resources
 * http://datamaps.github.io/ - I used this as the accessory library to create
   the choropleth
 * http://stackoverflow.com/questions/10599933/convert-long-number-into-abbreviated-string-in-javascript-with-a-special-shortn - I
   copied a function from here to perform the abbreviation of large numbers
   (e.g. 1048576 -> 1m), to make the hover labels more readable. 
