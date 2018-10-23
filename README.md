# Automated-API-Testing-Using-Postman-Collections

**Introduction:**

Postman Collections are groups of requests that can be run together as a series of requests we can organize into folders.
Running a collection is useful when you want to automate API testing. When you run a collection, you send all requests in your collection one after another.

**Installation:**

Install standalone windows application from here: https://www.getpostman.com/postman

**Creating Collections:**

Collections can be created from the:
- Launch screen
- New button
- Sidebar

**Launch Screen:**

![alt text](https://github.com/TSQAteam/Automated-API-Testing-Using-Postman-Collections/blob/master/Screens/LS.png)

**New Button**

**Side Bar**

Now open the CREATE A NEW COLLECTION modal either from Launch screen > Create New tab > Collection or New button > Collection or Sidebar > Collections > New collection
In the CREATE A NEW COLLECTION modal:
-	Enter a name and optional description.
-	Select an authorization type. (You can enter here for the collection or you can override this by specifying in the individual request. Here in this document, we specified in individual requests)
-	Enter a pre-request script to execute before the collection runs. (You can enter here for the collection or you can override this by specifying in the individual request. Here in this document, we specified in individual requests)
-	Add a test to execute after the collection runs. (You can enter here for the collection or you can override this by specifying in the individual request. Here in this document, we specified in individual requests)
-	Add variables to the collection and its requests if need.
-	Click the Create button
Eg:

**Add requests to collection**
We can create and save request(s) to a collection from the:
-	Request builder
-	New button
-	Launch screen

**Build view**
In the Workspaces build view, enter a new request in the builder.
Click the Save button.
In the SAVE REQUEST modal, enter a request name and select a collection or folder to save the request.
Click the Save button.

**New button**
In the header toolbar, click the New button.
Click "Request".
In the SAVE REQUEST modal, enter a request name and select a collection or folder to save the request.
Click the Save button.

**Launch screen**
The Create New tab appears by default when you launch Postman.
Open Postman.
In the Create New tab, click "Request".
In the SAVE REQUEST modal, enter a title and description.
Select a collection and save the request in an existing collection or create a new collection.
Click the Save button


After you save the request, you can add the URL, method, headers, and body to the request in the builder.
Eg.
We are using the below two api requests details for this demo:
Base URL : http://13.236.67.139:85/api/ 
Request Name: CreateNewLog
Url	/json/reply/CreateNewLog
Method	Post
Header	Content-Type:"application/json"
Request	{"LocationID":1}
Response	{"GrabbaSerialIndex": 1}

Request Name: UpdateLog
Url	/json/reply/UpdateLog
Method	Post
Header	Content-Type:"application/json"
Request	{"Log":
{
"GrabbaSerial": "ShoppingItem",
"GrabbaSerialIndex": 1,
"IMEI":"itemI456",
"SIMidentifier":"identifier156",
"DateTime":"2018-04-06 00:05:20",
"LocationID":1
}
}
Response	{ "UpdateStatus":True, "ErrorMessage":"" }






