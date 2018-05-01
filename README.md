# emberJS-routerNestedRoute

You can define nested routes by defining a template inside another template by passing a callback to the current route.

To create a nested route, run the below command −

ember generate route nestedroute/fruits

Open the file .hbs file created under app/templates/nestedroute. Here, we have created the file as fruits.hbs with the below code −

<h2>Fruits Page</h2>
<ul>
   <li>Orange</li>
   <li>Apple</li>
   <li>Banana</li>
</ul>

Open the router.js file in emberJSApp/demo-app/app to define URL mappings −

Router.map(function() {
   this.route('nestedroute', function() {
      this.route('fruits');
   });
});

Create the application.hbs file in app/templates/ and add the following code −

{{#link-to 'nestedroute.fruits'}}fruits{{/link-to}}
{{outlet}} 


Only fruits.hbs,router.js and application.hbs files are included in this repository
