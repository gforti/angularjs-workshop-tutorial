#Creating a View

So the idea here is we want to create a page that will render a list of all the phones.  Before we do that we just want to focus on getting the routing to work with a home page.

Start by adding the following code into the app.js file.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step1.png)


We now need to add a phone-list.template.html file and a phone-list.controller.js file under the js folder like so.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step2.png)


Lets start with the controller.  Add the following code to the phone-list.controller.js file.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step3.png)


Once we do that lets update the phone-list.template.html file with the following HTML

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step4.png)


Finally for the angular routing to display the home page, we need to add the ng-view attribute to the div on the index.html page.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step5.png)


Test the site to make sure the phone-list.template.html page is rendering.  Run the index.html page in your browser. The results should look like the following.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step6.png)


Lets continue by creating another view, which will be the detail page.  Add a file called phone-detail.template.html and another file called phone-detail.controller.js under the js folder.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step7.png)


Lets start back at the app.js file to include this route. What matters about the detail page is that we pass the phone id so we can view more information about a single phone. Add the following code to the app.js file.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step8.png)


Now lets move on to the phone-detail.controller.js file and add the following code

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step9.png)

Next update the phone-detail.template.html page with the following HTML

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step10.png)

If you run the index.html page and add in at the end of the url /phones/123 you should get a page that looks like this

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step11.png)

This is happening because we have not added the controller files into the index.html page.  Be sure to do that now.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step12.png)

The page will now render with correctly.  What you saw before or if you viewed the console was showing that the PhoneDetailController was undefined. When you create the JS files for your app be sure to add them to the page.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-view-step13.png)

All the views needed are now complete.

#End of segment. 

__Next:__ [Creating a Service](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/Creating-a-Service.md)
