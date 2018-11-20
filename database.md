# Databases

#### Concepts
* Connection pooling
  - keep database connections open so that it can be reused
* DB cursor
  - pointer to a row within query resultset
  - FORWARD_ONLY: start at the first, end at last, next by next
  - SCROLL: more options to navigate result, first, last, next, prior
  - allows something like streaming of data
  - Data sensitivity
    - STATIC: changes to db do not reflect in cursor
    - KEYSET: changes made to fetched rows are seen but not the new ones
    - DYNAMIC: all changes are seen


#### Links
 * https://stackoverflow.com/questions/3861558/what-are-the-benefits-of-using-database-cursor
 * https://stackoverflow.com/questions/4041114/what-is-database-pooling
