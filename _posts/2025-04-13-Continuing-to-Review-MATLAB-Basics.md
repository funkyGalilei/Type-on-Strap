---
title: "Continuing to Review MATLAB Basics"
categories: 
- Engineering Projects
- MATLAB
tags:
- Simulink
- MATLAB
- programming
- software
---
I wanted to recap the courses and learning paths I've taken through Mathworks. I've talked about them before, but in the meantime I've completed 3 more courses I believe and have learned a bit more. I give my quick thoughts about each below:
## Basic MATLAB Skills
Pretty self explanatory, but it was a good review and gave me base to work from.
## MATLAB Proficiency
This was most useful for exploring different data types, and seeing how they fit together. Some data types like the date time format I've had to work with, and seeing all of them graphed visually with labels on an infographic made things very clear
## MATLAB Programming Skills
I spoke on this course in an earlier post, and was useful for some random tidbits of info I didn't know, like the refactor button in the GUI.
## MATLAB for Simulink Users
I had done this one previously, and was good background for the way Simulink interacts with the MATLAB workspace
## MATLAB Software Development
This one was very interesting, but I'm not sure if I'll be able to implement it soon. One of the most interesting takeaways, was the existence of MATLAB projects, which are a way to write and store function files for work on a team. I haven't maintained files like that, mainly because my projects haven't grown to be that big working with another engineer. In addition, I have used git with MATLAB files that imitated this, but didn't know that unit tests were a thing.
Again, this is more knowledge that would be useful in more technically involved and complex projects, which is something I will do in the future.
## MATLAB Visualization and Graphics
This is something I consider myself an expert in, and thought as much entering the course. However, taking it was still beneficial. I remember being frustrated with axes, and not knowing whether or not to index into a Line variable property, or to index into the axes properties. Now I'm able to know which property is attached to what (I also forget about gca sometimes and just pass all the arguments in at once which isn't that readable).
I also enjoyed working with `surf()` functions a bit more, and didn't really work with them that much before. I also learned about `meshgrid()` and interpolating between values to create a smooth mesh. This will come into handy when visualizing Z values over matrices, I just haven't worked with those alrge types of data sets yet.
## Efficient and Robust MATLAB Programming
One of the interesting things about MATLAB is the process of "vectorizing" a calculation. Usually when I think of arrays, I think of the needing of a for loop, or 2 for loops if the thing I want to act on is a matrix. But with MATLAB, you can vectorize this process with *element wise* operators, like ".*", which would multiply each element in the array by the following thing.
I knew about this before, as its a basic MATLAB concept, but I didn't know that this computation is actually *faster* than looping. So now I'll try and think differently in the MATLAB language, and make my code more readable as well.
## Conclusion
All in all, I am really glad I continued to learn and take Mathworks courses, and hope to learn more about Simscape and the everything I can do with that. I know that muscle memory and writing functions out is the best way to improve. Forcing myself to have great coding practices will pay off in the long run even if its annoying to learn initially. My license is not infinite so I hope to learn all I can right now!
