# Create dynamic lists with RecyclerView  

* RecyclerView is used to view a large set of data.
* All of the data in the RecyclerView will have the same view and style.
* We can get the benefit of using RecyclerView to improve performance, the app's responsiveness and reducing power consumption, since it doesn't destroy the view of the item when it scrolls off the screen. 
* To build a dynamic list, there are several different classes work together such as:
  * RecyclerView is the ViewGroup that contains the views corresponding to the data. 
  * Each individual element in the list is defined by a view holder object. 
  * The RecyclerView requests those views, and binds the views to their data, by calling methods in the adapter.
  * The layout manager arranges the individual elements in the list. 

* To implement a RecyclerView, first you need to decide what the list or grid is going to look like and extend the ViewHolder class to design how each element in the list is going to look and behave, then define the Adapter that associates the data with the ViewHolder views.

* The items in the RecyclerView are arranged by a LayoutManager class.
* The RecyclerView library provides three layout managers:
  * LinearLayoutManager to arrange the items in a one-dimensional list.
  * GridLayoutManager to arrange all items in a two-dimensional grid, which can be grid vertically or horizontally.
  * StaggeredGridLayoutManager, which is similar to GridLayoutManager, but it does not require that items in a row have the same height (for vertical grids) or items in the same column have the same width (for horizontal grids). 

* The Adapter and ViewHolder classes work together to define how your data is displayed.
  * The ViewHolder is a wrapper around a View that contains the layout for an individual item in the list. 
  * The Adapter creates ViewHolder objects as needed, and also sets the data for those views.

* Three key methods need to be defined for the Adapter:
  * onCreateViewHolder() creates and initializes the ViewHolder and its associated View without filling the contents.
  * onBindViewHolder() fetches the appropriate data and uses the data to fill in the view holder's layout.
  * getItemCount() gets the size of the data set. 

