# Help my R is broken!

No one really ever *learns* or *knows* R, we just get better at knowing where to look for help! And at feeling like we will find a solution eventually!

For newer R users, it's sometimes hard to know where to start when trying to solve an R problem. 
I suggest students try to solve problems on their own before asking me, but I recognise it is not always obvious how to do this. 
Here are some pointers for how I solve R problems. 
Not every step will always be needed (and some are obvious, sorry!), and over time you'll probably develop other techniques that work better for you.

Remember to keep trying and know that it does get easier as you gain experience.
And if you feel like you've tried really hard to fix a problem, do ask for help! 
There are some tips on doing this at the end.

## General help tips
1. Google is your friend.
2. Google is sometimes your annoying friend. Sometimes Google is less helpful, for example when what you're searching for is a common word. In these cases you can try adding "CRAN" to the search term, or use [rseek](https://www.rseek.org) which will only search R relevant sites. It may also help to go directly to [stackoverflow](https://www.stackoverflow.com). Many Google searches will take you here anyway.
3. R mailing lists. There is an R-help mailing list, but I'd avoid this like the plague. You may see answers from the list in your Google searches that will help, but the list itself is often not too beginner friendly. This is weird given that the rest of the R community is really helpful! The mailing lists for [special interest groups](https://www.r-project.org/mail.html) (e.g. R-sig-phylo) are much better, and often host interesting discussions about the topic as well as R.
4. Twitter. I find Twitter super useful when I have R questions, but it does depend on who follows you, and whether the right person sees your tweet. Your question also needs to fit into 140 characters! Use **#rstats** to tag the tweet. Some useful accounts to follow for R tips are: @GSwithR, @rstudiotips, @RLangTip, @Rbloggers, @rstudio, and @rOpenSci.
5. R books. There are lots of these on the market now, and the ones that are worth buying/checking out of the library will depend on your interests. Ask someone who works in your field for some advice. And if you're in my group I probably have most of what you'd want in my office...

## More specific suggestions for different situations

### I have no idea where to start!
If you've no idea what _analyses_ you need to do then stop now. 
Go back and read papers asking similar questions and see what they did.
Talk to your supervisor and/or colleagues to get some ideas. 
Never do an analysis just because you **can**, do it because it helps answer the question you're trying to answer.

### Sorry I meant I have no idea where to start trying to do this in R!

1. Google is your friend. 
Try googling "How do I do X in R?".
2. CRAN has some great [Task Views](https://cran.r-project.org/web/views/) that list all the packages for a certain topic. Have a look and see if the topic you're interested in is there. 
You can also check out the full [list of R packages](https://cran.r-project.org/web/packages/available_packages_by_name.html).
3. Vignettes. 
Often you will come across these on Google searches, but you can also find them by typing `help(package = "packagename")`
into the R console (replacing `packagename` with the name of the package you're interested in. 
This will bring up a list of all the functions in the package and near the top a link to user guides and vignettes. 
You may be able to find what you need there, if you've chose the right package.
4. Twitter. 
This is an occasion that Twitter can really help as it's easy to ask "What package/function do I need to do X in R?".
5. Papers that use the method. 
Many papers these days come with supplemental code, or will at least cite the package they used in the paper. 
If they didn't use R, see if there is an R equivalent (using Google).


### I know the function I need to use but can't work out how to use it!

1. Google is your friend. 
2. R help.
This will probably have already come up via Google, but if not you can type `?functionname` into R (replacing `functionname` with the name of the function you're interested in) and the helpfile will load. 
Some helpfiles are great, some are awful. 
The best place to start is at the bottom with the **Examples**. 
See if you can run these, then see if you can modify them to get them to work with your data. 
I usually do this first, but this is because over the years I've got better at reading R helpfiles. 
You will probably have more luck with Google in the first instance.
3. Vignettes. 
Vignettes are longer helpfiles/user guides that package developers sometimes create. 
These are generally easier to follow than the helpfiles themselves.
Often you will come across these on Google searches, but you can also find them by typing `help(package = "packagename")`
into the R console (replacing `packagename` with the name of the package you're interested in. 
This will bring up a list of all the functions in the package and near the top a link to user guides and vignettes. 
You should be able to find what you need there.

### I've tried using the function and it keeps giving errors!

First check the standard stuff:

1. Do you have any typos? Missing brackets or commas? Mistakes with capital letters rather than lowercase? Number 1 instead of lowercase l (or vice versa)?
2. Are you using R Studio? If so try restarting R Studio, it sometimes crashes for no reason.
3. Have you got all the right packages installed *and* loaded (using `library(packagename)`)
4. Are you using the right working directory? Is your data where you think it should be?
5. Try re-running your code from the beginning of the script, *line by line*. Sometimes I've made a mistake reading in the data at the top of a script but because I've run the whole thing I miss the error and cause all sorts of downstream problems! Don't forget to start with `rm(list = ls())` so you're working with a clean R. Check that each stage has worked as expected.

Now check the more specific stuff:

1. Google the error message! 
You will need to remove any parts of this that are *specific to your data*. For example, the name of the dataset or variables. 
This sometimes takes a bit of playing around with. 
But if you got an error, it's almost guaranteed that someone else got the same error at some point!
2. Check the helpfile.
Type `?functionname` into R (replacing `functionname` with the name of the function you're interested in) and the helpfile will load. 
Some helpfiles are great, some are awful. 
The best place to start is at the bottom with the **Examples**. 
See if you can run these, then see if you can see how they differ from your code - this might give you a clue to the error.
3. Vignettes. 
Vignettes are longer helpfiles/user guides that package developers sometimes create. 
These are generally easier to follow than the helpfiles themselves.
Often you will come across these on Google searches, but you can also find them by typing `help(package = "packagename")`
into the R console (replacing `packagename` with the name of the package you're interested in. 
This will bring up a list of all the functions in the package and near the top a link to user guides and vignettes. 

## Asking for help

If you've exhausted all these possibilities it's time to ask for help! But asking for help the right way can help you get an answer much faster.

1. Always provide your **code** and your **data**. It doesn't have to be all of your code, just enough to read in the data and get to the error message or the stage you've got stuck. Likewise you don't need to send all of your data (and if your dataset is huge it's probably best not to!), just enough to replicate the problem. Some people feel awkward about this but without these we're probably not going to be able to solve the problem.
2. Make sure the question is clear. 
If you're asking about an error message this is easier, just make sure to include the error message.
If you're asking how to do something it can be harder. 
The best way in this case is to give a dummy example of *what you want the output to look like*. 
Take a look at some stackoverflow questions to get an idea of the best ways to do this. 
For example, using A, B, C etc. rather than long species names.
