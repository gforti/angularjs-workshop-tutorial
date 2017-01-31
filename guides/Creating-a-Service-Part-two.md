#Creating a Service Part two

Going back to the phones.service.js file, lets add a function that will help us find the result of just one phone record. We will need to get the array of phones, loop through them, then match each phone id with the one we are trying to look for.  insert the following code.

start by adding in the reference to the findPhone function.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service2-step1.png)

finish by adding the findPhone function below in phones.service.js

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service2-step2.png)

Now that the service is complete, lets update phone-detail.controller.js using the PhonesService.findPhone function.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service2-step3.png)

All that is left is to now update the view with the model data. Open phone-detail.template.html and replace all of the HTML with the following. since phone is a single phone object, we can just access the properties.

![image](https://github.com/gforti/angularjs-workshop-tutorial/blob/master/guides/img/angular-7-service2-step4.png)

Run and test index.html in your browser.  You should be able to run the complete application by clicking on a phone and viewing the phone details now.

#This segment is complete.
