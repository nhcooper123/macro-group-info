# Geometric morphometrics
Morphometrics is the study of quantitative measurements of morphological traits, e.g. skull length, skull width etc.
*Geometric morphometrics* uses geometric coordinates (x and y for 2D; x, y and z for 3D) instead of measurements to investigate morphological features.
Geometric morphometrics have become a really popular way to investigate morphology (size and shape), and are a particularly useful tool when using museum specimen data.
Many students and postdocs in the group will use these methods in their projects. 
This is not intended to be a comprehensive guide at all, just a place for me to put links to helpful web pages etc. where people have explained things better than I can!

## Workflow of a simple geometric morphometrics analysis
1. Collect data
2. Choose landmarks
3. Digitize
4. Procrustes superimposition (GPA)
5. Principal components analysis (PCA)
6. Error checking (though this also will need some data collection in step 1)
7. Additional analyses

### 1. Collect data
This involves either taking 2D photographs or 3D scans (e.g. surface scans, photogrammetry, microCT scans). 
Your choice of 2D versus 3D will depend on the *question* but also on how much time you have versus how many specimens you wish to use. 
3D scanning is common for biomechanics studies, or studies with few specimens e.g. for taxonomic or paleontological projects. 
If tackling a comparative project it is often better to collect 2D data from more specimens/species.
The group has digital cameras, macro lens, tripod, scale bars etc. and we have access to a microCT and surface scanners, though time on these must be booked 3-6 months in advance.

A few general tips.

* Make sure to regularly back up photographs and scans (DropBox, Google Drive or iCloud are good ideas in case your computer crashes).
* Ensure that you include the specimen ID in the filename (and maybe the species name too), and keep a tidy folder with all your photos or scans in it.
* Remember to copy down *metadata* associated with each specimen as you take the photos or scans, e.g. specimen ID sex, age, locality, species. Recording specimen ID is most important, as you will use this to connect the metadata to your shape data later in the analyses. 
* You will also want to take multiple photos/scans of the same specimen at some point (including setting up the photo/scan and the specimen/equipment again to make it independent) to check that you're able to do this step without introducing too much error (see step 5).

Here are some quick tips for taking photographs.

* Photographs need a scale bar, and should be on a uniform background.
* Small specimens need a macro lens and the camera will need to be quite close to them. 
We have copy stands to help with this.
* Large specimens should be at least 1m from the camera to avoid a distortion called parallax. 
You should attach the camera to a tripod so it is directly above the centre of the specimen. 
Very large specimens may need to be placed on the floor.
* Try to make sure the specimen is as level as possible, you may need to use bean bags or foam. 
Ask a curator if you need help with this as certain things will need to go through pest control procedures before they can be used. 
Also using modeling clay is usually not allowed here.
* Shoot in RAW.
* Remember to take your charger into the collections, and charge over lunch (or take a spare battery/camera) if you're having a heavy data of data collection.
* Remember photographs don't need to be beautiful, but you do need to be able to see all the landmarks clearly, and the scale bar. 

## 2. Choose landmarks
This is the hardest step and also the most important.
Unfortunately it is often the most subjective!
Choice of landmarks (both the coordinate points you will put on the photo/scan, and any outline curves or semi-landmarks) will depend on the *question* you're asking, the species you're studying and the type of analysis you want to do.
My advice is to first read as many studies as possible using the same species as you and see which landmarks they used and which anatomical features are fairly easy to identify.
Landmarks should be present on all the species in your analysis (although you can have absent landmarks if needed), and be repeatable and identifiable. 
You should be able to place landmarks with confidence, and if you try to place landmarks on the same specimen twice, their locations should be as close to identical as possible (this is something to test in the error checking stage).
Landmark should also capture the similarities/differences in your specimens that you hope to analyse later on.

I am not an anatomist, and my expertise is confined to a few groups, so you're likely to have a better idea about this than me once you've done lots of reading. 
However, I'm of course happy to look over your landmark choices (and would suggest that I do so before you start digitizing).  


## 3. Digitize
You'll hear people use the word "digitize" to mean a bunch of different things (especially within museums!). In geometric morphometrics we mean the process of going from photos to having coordinate data we can play around with, i.e. adding landmarks to our photographs.

Digitizing is pretty simple to do in geomorph (see links below), though some students prefer to download the package [ImageJ](https://imagej.nih.gov/ij/download.html) which can be easier. 
You'll be using the mouse to click on the photos at the point you want each landmark to be.

Remember you need to add landmarks in the same order for each specimen, and don't forget to add the scale before you start. 
Save regularly and make sure to backup your files too. 
This can be a time consuming process so it's worth having a quick practice with a small subset of your specimens before starting your final digitization (you may find you need to remove/modify some landmark positions etc.).

## 4. Procrustes superimposition (GPA)
GPA is a way to remove rotation, translation and scaling differences among specimens so they can be compared. 
It's pretty simple to do in geomorph (see links below), and the links below to lectures and a book have great descriptions of it so I won't repeat those here.

## 5. Principal components analysis (PCA)
PCA allows you to take a collection of correlated variables (your landmark coordinates after GPA), and to find the greatest axes of variation in this data. 
This produces principal components scores that are referred to as "shape variables" in geometric morphometrics (note PCA is used in lots of fields). 
You might end up with one PC axis that refers to the shape of the snout, and another for the shape of the mandible for example. 
This is much more useful than plotting raw coordinate positions against each other, and usually reduces the number of variables you need to look at (e.g. a couple of PC axes versus 20 landmarks). 
I won't go into anymore detail here as the links below have great descriptions. 
Make sure you read these carefully, as PCA is simple but often misunderstood.

PCA is pretty simple to do in geomorph (see links below), and geomorph also has some great plotting functions for plotting landmarks at this stage.

## 6. Error checking/sensitivity analyses
This needs to be considered from the *start of a project and throughout*. Essentially we want to ensure that any results you obtain are due to super exciting biology, not to some kind of error or bias. This is probably the most important step in doing good science.

Errors can crop up in all kinds of procedures, from the way you take a photo to the way you run an analysis in R. As you work through the project, think carefully about things that might introduce error. Then think about ways you can test whether there is any error (there's almost always going to be some) and how big it is. To help get you thinking, think about whether someone else following your protocol would get the same result?

A quick aside: there will be additional steps of error checking in your later analyses that we call sensitivity analyses. I often think of these as trying really hard to break your result. If you don't break it then it's more likely to be correct. For example, you might wonder if your significant result is because you have 20 specimens from one species that are driving the pattern. In this case, repeat the analysis removing those species - do you get the same result? You may need to use rarefaction or similar to deal with sample size differences. If you're assuming males and females are the same so you can use non-sexed individuals you should check this is true using specimens with sex data. This is just to point out that error checking doesn't end once you've got your landmarks together, it continues to the end of the project. Note that often you'll pop these kinds of analyses into an appendix if they aren't significant.

## 7. Additional analyses
This is the point where things get (even more) interesting! You now have all your shape data, and it's time to actually investigate the questions you wanted to answer when you started the project! Woo!

Of course this means the analyses you choose will depend on your *question*. There are as many methods as there are questions, so I can't give specific advice here. But the first step is always to go away and read lots of papers asking similar questions. What methods do they use? Are these possible with your data?

## Getting help with geometric morphometrics
1. I highly advise getting hold of this book ([Zelditch et al. 2012](http://store.elsevier.com/Geometric-Morphometrics-for-Biologists/Miriam-Zelditch/isbn-9780123869036/)) and reading the first few chapters, plus any chapters later in the book that are relevant to the analyses you will be doing. 
Don't panic too much about the maths or the equations, just try to get a general understanding of what each method is doing, especially GPA and PCA.
Try and get a copy from the library first, but I also have a copy in my office.

2. David Polly has an excellent [set of lectures](http://www.indiana.edu/~g562/) about all basic topics in geometric morphometrics including PCA, GPA and a basic workflow for an analysis using geomorph.

3. Emma Sherratt has put together an excellent tutorial/vignette for [geomorph](http://www.public.iastate.edu/~dcadams/PDFPubs/Quick%20Guide%20to%20Geomorph%20v2.0.pdf) from inputting landmarks to complex analyses.

4. The [geomorph vignette](https://cran.r-project.org/web/packages/geomorph/geomorph.pdf) may also be helpful for more complex analyses.

5. For error checking, take a look at [Fruciano 2016](http://link.springer.com/article/10.1007/s00427-016-0537-4) a review of the subject in Evolution.

