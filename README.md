# RobloxApiClient


This library is based on the RobloxApiClient object, which simulates a user session.

Here are the methods of RobloxApiClient:

friends(id1,id2)

Returns a bool indicating if the users with the given IDs are friends.

name(id):

Returns the name of the user with the given ID.

assetComments(id):

Gets a JSON object containing comments on the given asset.

catalogSearch(geartype = -1, genre = -1, subcategory = -1, category = -1, currency = -1, sort = -1, freq = -1, keyword = None, creatorID = None, minim = 0, maxim = None, notforsale = True, pagenumber = -1, resultsperpage = -1)

Searches the catalog for items with the given parameters. The Gear, Genre, Category, Subcategory, Currency, Sort, and Time objects contain potential values.

getFriends(id):

Gets a list of the user's friends.

friendCrawl(id, maxfr = 100)

Gets a list of users related to the given users by indexing their friends, then their friends' friends, and so on until the limit specifief by maxfr has been reached.

getCurrentStatus():

Returns the currently logged in user's status.

getUserPresence(id):

Gets the presence of the user with the given ID. For more see here.

createAccount(username, password, birthday, gender = 2):

Creates an account with the given parameters. birthday is a datetime object. Gender is 1 for female and 2 for male. Returns a HTTP object containing the new user's id.

getItemInfo(id):

Returns a JSON object full of info about the item.

buyItem(id):

Buys the item with the given ID.

logIn(username,password,returnurl = ""):

Logs in with the given credentials. returnurl is pointless unless you're concerned with looking legit.

getCurrency():

Returns the current user's balance. May be useful for MGUI :)

setXsrfToken():

Sets the XSRF token. Used internally. The token can be obtained in the form of the RobloxApiClient's token property.

sendMessage(subject,body,recipientid):

Sends a message.

forumPost(forumid,subject,body,disablereplies = False):

Creates a forum post on the forum with the given ID.

replyToForumPost(postid, text, disablereplies = False):

Replies to a forum post with the given ID.

getRobloSecurityCookie():

Returns the ROBLOSECURITY cookie, allowing you to replace your own cookie and log into that session.

commentOnAsset(assetid,text):

Comments on the given asset.

joinGroup(groupid):

Joins the given group.

reportAbuse(self,userid,category,comment):

Reports a user. Category is a number; hacking is 5.

getRap(self,assetid,returnv = None):

Gets the RAP of an item. returnv is used internally.

getUserRAP(self,userid):

Gets the RAP of the given user. Will use up a LOT of bandwidth in a short time.

getSellers(assetid):

If the given asset is limited, returns a JSON table containing information about its sellers.

getSalesData(assetid):

If the given asset is limited, returns a JSON table containing generalized information about its sellers. Includes a graph that maps price to Unix timestamp.

snipeLimited(self,assetid,desiredprice):

A built-in function that buys a limited if it's equal to or below the given price.

logOut():

Logs you out.

favItem(item): 

Favorites the given item. Credit to Vibe.

updateStatus(message):

updates your status to the given message. Also made by Vibe.
