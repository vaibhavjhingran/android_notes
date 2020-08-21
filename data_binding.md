# Data Binding

## Reason:
When using findViewById to find references to views, after every inflation, android has to traveser the view hierarchy to find it for us at runtime.

For large/deep-view hierarchy, this can be expensive and resource draining, slowing down the app.

Data binding, allows us to connect a layout with an activity/fragment at compile time. The compiler generates a helper class, binding class, when the activity is created. Views can be accessed with the generated binding class without any extra overhead. 

## Implementation:

  * Enable data binding (gradle ~> app).
  * Add <layout></layout> root on view.
  * In the activity, create a binding object.
  * Instantiate usually within the onCreate method.
  * Use binding instantiated variable to access UI elements.
  * To refresh all binding created UI data, use invalidateAll().

It's also important to leverage data binding. 

  * Bind data class to a view.
  * Create a data class.
  * In the layout, add a data block
  * In the acitivity, add binding object with data class and views to play around with visuals.

