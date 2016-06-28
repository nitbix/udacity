# Data Visualization project

## Summary 
This project focuses on a visualization for the "Prosper Loan Dataset". The
visualization represents how much loan volume has been processed through
Prosper, organised by state where the Borrower resided. The main finding that
this visualization is trying to portray is that most of the processed loans are
based in CA, with a few other states trailing behind, and only residual volume
anywhere else.

## Design
This started as a bar chart. I imagined that the vertical distance between
California and the closest second would be useful information, and a bar chart
makes it very obvious. However, the visualization was very cluttered because
there were 50 bars, and a lot of labels at the bottom.

After the first suggestion, I changed it to a pie chart, with the first 5 states
listed, and the rest grouped under "other". This clearly conveyed the idea that
most of the states didn't contribute much to the amount borroed on Prosper.

After the second round of feedback, it was clear that something more had to be
done to make the visualization more attractive and clear. Unfortunately
dimple.js does not natively support choropleths, so I had to be creative. I
found a library built on top of d3 that could help build a choropleth
(http://datamaps.github.io/), so I opted for this. I decided to encode the total
amount borrowed with the colour, because position was already used by the shape
of the graph, and using size would have made it messy (perhaps changing the size
of each state according to the loan amount could have work, but that would have
made for a very unfamiliar map).

The third suggestion was a very simple one and easy to fix, by adding state
labels to the map, and some additional information in the hover box.

Suggestion 4 was from the Udacity reviewer, and I find that it reconciles the
doubts I was having about conveying by how much California dominates the Prosper
Loans borrowing. I added the original bar chart under the choropleth, and added
a small paragraph to describe the visualization. To be honest, I didn't think I
would be allowed to use two graphs, otherwise I think I would have already added
the bar chart at the bottom.

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

####4
The choropleth map is very good at communicating your finding, but there are a
few things that can be done so that the finding is more clearly communicated:

 * The title says loan volume which gives the impression of total number of loans.
In finance, volume often refers to a dollar amount but a viewer might not know
this. I would write some unit abbreviation in parenthesis whenever you use the
term 'volume', so that it's clear you mean a dollar amount, something like
'(USD)'.
 * The title of the visualization is a little too small. I would increase the size
of the font and give it a descriptive title fit for the finding. For this
dataset you could have a title like 'Prosper Loan's Largest Marketplace in
California' or something like it.
 * Include some introductory text before the graphic (experiment with the
placement, one side might be best) that explains the data and what you are
trying to show (similar to the readme but more concise).
 * In the tooltip be consistent and use the same term for volume that you use in
the title or introductory text. So instead of 'Total Borrowing' use 'Volume'
although you can still write 'Total Borrowing' in parenthesis if you like.
 * See if you can make the text for 'Total Borrowing' / 'Volume' in the tooltip
bold (I would leave state name without bold text since you can already see which
state you are hovering over). This will help to emphasize that this number is
the volume that you are referring to.

##Resources
 * http://datamaps.github.io/ - I used this as the accessory library to create
   the choropleth
 * http://stackoverflow.com/questions/10599933/convert-long-number-into-abbreviated-string-in-javascript-with-a-special-shortn - I
   copied a function from here to perform the abbreviation of large numbers
   (e.g. 1048576 -> 1m), to make the hover labels more readable. 
