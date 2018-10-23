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

![alt text](https://github.com/TSQAteam/Automated-API-Testing-Using-Postman-Collections/blob/master/Screens/new_button_collections.png)



**Side Bar**

![alt text](https://github.com/TSQAteam/Automated-API-Testing-Using-Postman-Collections/blob/master/Screens/Side_Bar.png)

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


**Adding URL & Method Selection as POST**


Select Headers Tab and enter the details from your api details provided


Select Body tab and enter the Request details as raw format (You can give which ever format you like form data etc) as given in the api document

Note: If raw is chosen, then JSON(application/json) must be selected.
Now select Tests tab. Choose any of the available test snippets from the right side block. These tests can be used to verify the response received is correct and assure us that all the sent request are passed or not.
For this demo we have chosen ‘Status code: Code is 200’ test which is simple and most used one to verify the response received.


Click the save button.
Now similarly add two or more requests in the same collection. I have added 4 requests in this demo collection as shown in below and saved.


Once we save this collection then we can run this any time with hassle free



**Running the Collection**

To run collections, we can use either
-	Postman app collection runner in the header bar.

-	Sidebar > Collections > Saved Folder > Run


Once we click the run button then Collection Runner window will open as below

In this Collection Runner, select the test environment from the environment dropdown (By default – No Environment), Iterations, Delay, Log Responses & Data on the left and run the collection. You'll see the tests pass as shown in below.







