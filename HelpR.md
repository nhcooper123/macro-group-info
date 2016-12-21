# Help my R is broken!

No one really ever *learns* or *knows* R, we just get better at knowing where to look for help! And at feeling like we will find a solution eventually!

For newer R users, it's sometimes hard to know where to start when trying to solve an R problem. 
I suggest students try to solve problems on their own before asking me, but I recognise it is not always obvious how to do this. 
Here are some pointers for how I solve R problems. 
Not every step will always be needed (and some are obvious, sorry!), and over time you'll probably develop other techniques that work better for you.

Remember to keep trying and know that it does get easier as you gain experience.
And if you feel like you've tried really hard to fix a problem, do ask for help!

## General help tips
1. Google is your friend.
2. Google is sometimes your annoying friend. 
Sometimes Google is less helpful, for example when what you're searching for is a common word. 
In these cases you can try the following.
..* add "CRAN" to the search term
..* use [rseek](https://www.rseek.org) which will only search R relevant sites
..* go directly to [stackoverflow](https://www.stackoverflow.com). Many Google searches will take you here anyway.
3. R mailing lists. 
There is an R-help mailing list, but I'd avoid this like the plague. You may see answers from the list in your Google searches that will help, but the list itself is often not too beginner friendly. 
This is weird given that the rest of the R community is really helpful! 
The mailing lists for [special interest groups](https://www.r-project.org/mail.html) (e.g. R-sig-phylo) are much better, and often host interesting discussions about the topic as well as R.
4. Twitter. 
I find Twitter super useful when I have R questions, but it does depend on who follows you, and whether the right person sees your tweet. 
Your question also needs to fit into 140 characters! Use **#rstats** to tag the tweet. Some useful accounts to follow for R tips are: @GSwithR, @rstudiotips, @RLangTip, @Rbloggers, @rstudio, and @rOpenSci.
5. R books. There are lots of these on the market now, and the ones that are worth buying/checking out of the library will depend on your interests. Ask someone who works in your field for some advice. And if you're in my group I probably have most of what you'd want in my office...

## More specific suggestions for different situations

### I have no idea where to start!
If you've no idea what _analyses_ you need to do then stop now. 
Go back and read papers asking similar questions and see what they did.
Talk to your supervisor and/or colleagues to get some ideas. 
Never do an analysis just because you _can_, do it because it helps answer the question you're trying to answer.

### Sorry I meant I have no idea where to start trying to do this in R!

1. Google is your friend. 
Try googling "How do I do X in R?".
2. CRAN has some great [Task Views](https://cran.r-project.org/web/views/) that list all the packages for a certain topic. Have a look and see if the topic you're interested in is there. 
You can also check out the full [list of R packages](https://cran.r-project.org/web/packages/available_packages_by_name.html).
3. Vignettes. 
Often you will come across these on Google searches, but you can also find them by typing `help(package = "packagename")`
into the R console (replacing `packagename` with the name of the package you're interested in. 
This will bring up a list of all the functions in the package and near the top a link to user guides and vignettes. 


### I know the function I need to use but can't work out how to use it!

1. Google is your friend. 
Vignettes


## I've tried using the function and it keeps giving errors!

1. Google the error message. 

Vignettes
Check for common errors
Restart R Studio