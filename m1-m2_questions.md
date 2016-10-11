## Milestone 1

Individual Comments:

Input: It sounds like you are saying that the user enters info in json format. That can't be right but that seems the way it is worded.

* The user doesn’t enter any information about the plot, the user only searches for movies. The user can add their own comments and ratings to the movies and post them back to the database.

Also, it seems like you are entering information about the plot from OMDB and from the user. Are you merging these? Are you submitting the results to the IMDB or keeping track of this information separately? What does searching by ID mean? Is the user expected to know IDs?

* The user doesn’t enter any information about the plot, the user only searches for movies. The user can add their own comments and ratings to the movies and post them back to the database.
* The user doesn’t enter any information about the plot. All the movies and its data will be pulled from the Online Movie Database.
* We are not submitting the results to the IMDB and will be keeping track of this information separately. 
* The user will not be searching by ID but only by movie titles, year, plot.

Processing: It looks like you can remove movies. What happens to info that has been added to a movie that would be useful to another user if that user later wants to add the movie? (For instance, number of favorites) Or are you just removing information that you could later get back if needed from the OMDB API? I am glad that you will have a facility to remove users. I assume this means the user wants to remove him- or herself. If the same user comes back and rejoins, it would be better to have no record of their prior association.

* User cannot add or remove information from the movies. User also cannot remove movies.
* We are only removing the information that we can get back from the OMDB API which excludes ratings and comments. 

Output: You mention following in output but not in processing. You should mention it in processing. You should also consider following regarding favoriting and possibly other functionality. For instance, should the favoriting by someone with many followers count more than the favoriting of someone with no followers?

* It’s possible some sort of weighting functionality could be useful (i.e “popular” users such as movie critics could have their opinions hold more weight) but that’s not something we’ve discussed or considered implementing so far.

General Questions: What happens if a filmmaker uploads a film to Pocketfilms but does not enter information for that film into the IMDB? Does that ever happen? In other words, is it possible to have films for which there is no IMDB entry? Similarly, what if there is confusion about the presence of films in the list as to whether Pocketfilms has the right to show that film? For instance, let's say I search for a particular Disney movie that Pocketfilms does not have and Disney would not allow to be shown by others. Might I be confused into thinking I should be able to view it through Pocketfilms because it is in my list?

* To clarify, the movie database we will be using is IMDb through the OMDb API, but this application will hopefully be usable with other databases with little modification, as long as it is formatted similarly. The app is not aimed to store actual movies or allow you to view those movies, though links may be provided in some cases. 

## Milestone 2

You have listed team names but not roles. Is this also something you plan to do?

* Roles are updated in our most recent version of Development book (milestone 3).

Your business rules seem more like requirements. An example of a rule might be to say that there is no limit on the number of users a user may follow. Or a movie can not be added to both “Watched” and “To Watch” by the same user.

Business Rules (revised):

* There is no limit to the number of users a user can follow
* There is no limit to the number of movies a user can add to any list
* Users can mark a movie watched from the “to watch” list and it will be moved to the “Watched list”.
* There will be no movie in both the to watch list and the watched list
* User can make his own lists but the default lists will be “To watch” and “Watched”

What do you mean when you say "if NodeJS has no interest"?

* We did not have the exact technologies fleshed out then and structure of our program, we’re moreso just listing things that we think will be useful, but it will come down to what we need to implement the functionality that we want. 

Some aspects of your design patterns are unclear to me. You don't mention enough detail for MVC. For the observer pattern, I wonder if you mean that the observed rather than observer would get notified. The description of the façade pattern does not say anything specific about who or what is using the subsystems.

* We updated this in the Milestone 3 development book we submitted.

I thought you were going to use the IMDB. Is that no longer the case? The project should use some publicly available source of data.

* We will be using OMDB as a proxy to get the data since we cannot use data from pocketfilms.



