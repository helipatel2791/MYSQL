* Index helps to execute querry faster, it uses B-tree to refer to the row. Two type of indexes - Clusterd, Non-Clusterd

| Clusterd                                                                | Non-Clusterd                                                                                                                   |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Only one clustered index per table                                      | More than one non clustered index possible per table                                                                                             |
| Analogues to telephone directory                                        | Analogues to book index                                                                                                        |
| Faster than non-cluster                                                 | Slower than Clustered, because clustered index has to refer back to the table, if the selected column not present in the index |
| Doesn't requite additional disk spaceas it determines the storage order | Additional storage space required, as it is stored separately from the table                                                   |
|                                                                         |                                                                                                                                |

##### Unique Index

* UNIQUENESS is a poperty, not a different type of index. So, both clusterd & Non-Clusterd indexes can be unique
* Primary key actully uses unique clusterd index by default behind the scens for enforcement
* When you add a unique constraint, a unique index gets created behind the scenes. (Non-Clustred by default)

##### Disadvantages of Indexes

* Additional Disk space - For Non-Clustered
* Insert, Updat & Delete statements can become slow


** Covering query: If all columns  that you have requested in the SELECT clause of query are present in the index, then there is no need to lookup in the table again, that is called a covering query.
