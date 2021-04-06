# what's database normalization:
- Database normalization is a process used to organize a database into tables and columns. The idea is that a table should be about a specific topic and that only those columns which support that topic are included.

  - Reasons for Normalization:
   - There are three main reasons to normalize a database. The first is to minimize duplicate data, the second is to minimize or avoid data modification issues, and the third is to simplify queries. 



    - Data Duplication and Modification Anomalies:
     - ![](https://www.codeproject.com/KB/database/832221/2bd01c59-ee13-4b57-8e0e-ef4bb44c164a.Png)
      - The first thing to notice is this   table serves many purposes including:

       - 1. Identifying the organization’s salespeople
       - 2. Listing the sales offices and phone numbers
       - 3. Associating a salesperson with a sales office
       - 4. Showing each salesperson’s customers

       - Data Duplication and Modification Anomalies:
        - Duplicated information presents two problems:
        - 1. It increases storage and decreases performance.
        - 2. It becomes more difficult to maintain data changes.

        - Insert Anomaly:
         - in order to create the record, we need provide a primary key.
         
         - Update Anomaly:
          - ![](https://www.codeproject.com/KB/database/832221/383ff737-57ca-4bf9-bce9-ddbf7e35b865.Png)
           - The same information is recorded in multiple rows. For instance, if the office number changes, then there are multiple updates that need to be made. If these updates are not successfully completed across all rows, then an inconsistency occurs.

           - Deletion Anomaly:
            - ![](https://www.codeproject.com/KB/database/832221/1000917c-9468-4263-b683-62baf052d962.Png)

            - Definition of Normalization:
             - There are three common forms of normalization: 1st, 2nd, and 3rd normal form.
              - First Normal Form – The information is stored in a relational table and each column contains atomic values, and there are not repeating groups of columns.
            - Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
          - Third Normal Form – The table is in second normal form and all of its columns are not transitively dependent on the primary key. 






