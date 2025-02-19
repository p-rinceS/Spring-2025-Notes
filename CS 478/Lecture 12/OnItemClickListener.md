

declares method `public void onItemClick()`

On item click you can specialize for the item that's being clicked.

Takes four parameters
1) parent
2) view
3) position of the item in the list
4) Id of the item that was clicked



[[Adapter]] specifies the format of the element and the content of the list view


You can distinguish different items in the list and do anything to any item in the list. 
If there are multiple list views you want to know which one is involved in the item click, this is why we need to pass in parent (Just professor's speculation)

