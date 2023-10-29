# Figure_Reader:
If data from a figure is unavailable, take a screenshot and use this Figure_Reader tool to click and identify data points. 

## Summary:
In 2020, me and a team of researchers embarked on a ***meta-analysis*** to determine the standard ranges for concentrations of brain metabolites measured with in vivo 1H Magnetic Resonance Spectroscopy. If you're not familiar with neuroimaging methods... the key point is that we were conducting a meta-analysis, reading hundreds of papers and extracting out resulting values. We realized that it was common (quite surprisingly) that there were papers that included figures, but did *not* list their summary statistics. 

When we came across such papers, we simply contacted the authors. However, we rarely got responses back with these emails. Other times, we did receive a reply, but their message was that they no longer had the data. 

We didn't want to simply skip over these papers... some of these papers included data from metabolites that are rarely targeted or in populations not typically investigated.

Our first strategy to handle this was to take a screenshot, add gridlines, and eyeball the values. We realized this was time consuming and fairly innacurate. 

Finally, I had the realization that if I took the same screenshots, I could map the pixel values to the figure axes. If I simply set the left and right and/or bottom and top axis points, I could then I could figure out the figure axis corresponding 2-d image point within the figure.

So, I wrote some quick code in Python to see if it worked. I never intended this to be a full-blown application... But I realized that I would need something reasonable if I was going to send to my other team members ***and*** I wanted this to be done well for the publication. 

Now I've created applications using TKinter and Kivy in the past. In retrospect, maybe it would have been nice to use one of these libraries here as well... but as I sat down to code this, I was really curious about Matplotlib's Widgets (which I had only tried for simple tasks). I also knew I could have something working almost immediately with Matplotlib, so I jumped in.

## Keywords:
meta-analysis, missing data, axis mapping, pixel mapping, Python, Matplotlib, Matplotlib Widgets

## Uses:
If you're conducting a meta-analysis and can't get your hands on raw data or summary statistics from a figure, use this tool to identify values.

## Citation:
If you find this tool useful, please cite:

> Gudmundson, A. T., Koo, A., Virovka, A., Amirault, A. L., Soo, M., Cho, J. H., ... & Stark, C. E. (2023). Meta-analysis and open-source database for in vivo brain Magnetic Resonance spectroscopy in health and disease. Analytical biochemistry, 676, 115227.

## Instructions:
1. ***Installation:***
2. Download the python (Read_Figure.py) file.
3. ***Running the Application:***
4. Open a terminal/command prompt
5. Type "python PATH_TO_FILE/Read_Figure.py PATH_TO_IMAGE/IMAGE_NAME.png"
6. ***Groups:***
7. Set the Left and Right and/or Bottom and Top Figure axes from the figure.
8. Select the Radio Button for each of the Left, Right, Bottom, and Top you selected above.
9. Once selected, click as close as you can to the axis tick mark.
10. Select the 'Click' Radio Button option.
11. Click the 'Update' Button.
12. Text Above the Figure should display the axes.
13. ***Groups:***
14. Type in the number of groups and hit the Enter or Return key.
15. You can now select which group you're going to work on.
16. ***Values:***
17. With the 'Click' option still selected, click the points you wish to identify.
18. Each user-click will output the coordinates in the terminal window.
19. ***Close:***
20. A .csv file with the Image Filename is automatically created upon closing. 
21. The Timestamp, Group Information, and coordinates are stored.

## Dependencies:
- Python3
- Numpy
- Pandas
- Matplotlib
