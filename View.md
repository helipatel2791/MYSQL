* A view is nothing more than a saved SQL query. A view can also be considered as a virtual table.
```
Create view VWEmployeeByCategory as Employee_ID, Name, Gender, Category from Employee join Category  
       on Employee.Category_ID = Category.ID;
```
* It can be used to reduce the coplexity of the database scema
* Can be used to improve row and column security (by only selecting columns/rows need to be displayed to others)

```
To modify a view: ALTER VIEW Viewname AS Select_Statement;
To Drop a view: DROP VIEW Viewname;
```

* It is possible to INSERT, UPDATE OR DELETE from the base table through the view. But, if a view is based on multiple tables, and if you update a view, it may not update the underlying base table correctly. To correctly update a view, that is based on multiple table, Instead off triggers are used.
* When you create an index on view, the view gets materialized. This means , he view is now capable of storing data.
