#Creating a Service

So we need to focus on creating a service for our application.  We would mainly create multiple services depending on the need of our application.  Services provide a great way for us to structure and handle the business logic of the application.  Because all services in Angular are singletons, we can reuse them throughout the whole application while keeping the state of the service values that might be stored.  We are not going that deep but we will focus on retrieving data and using built-in promises in Angular to help us with the call backs.

Start by creating a constant.js file under the JS folder.  This file is helpful in keeping constant values in our application in such a way that it can be reused throughout the app. 

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step1.png)

In the constant.js file type in the following code.  Notice that the url reference to the data/phones.json file is actually relative to where the index.html page will read the file from, not from the location of the constant.js file itself.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step2.png)

Now we can create the phones.service.js file under the js folder.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step3.png)

Add the following code to the phones.service.js file.  Here we will be using the angular provided service called $http.  It will also us to make AJAX calls with a built-in promise and other built-in features that are useful. We are also injecting the REQUEST constant to know the location of the data to call.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step4.png)


Now that we added these two files be sure to add these files to the index.html page.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step5.png)


Feel free to run the index.html page and check the console to make sure there are no errors.

Now that our service is make a call to get the json data, we need our controller to call and get the data for the view page. Open phone-list-controller.js and add the following code. The service will make the ajax call, and return the data in the form of a promise.  We then set our view model variable phones to that data.  Angular will in turn auto update the view when the value for vm.phones has been updated.  That is the why angular is a VMMV (view to model, model to view) framework.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step6.png)


Last thing needed before we can see anything is to update the phone-list.template.html with the new found data from the controller. Angular has some built-in syntax that allows us to write HTML in a form that uses programming.  So we have an un-ordered list displayed using a loop from the phones array.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service-step7.png)

Once you are done retest index.html and you should now see a page that looks like this.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-complete-1.png)


#End of segment. 

__Next:__ [Creating a Service Part two](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/Creating-a-Service-Part-two.md)
