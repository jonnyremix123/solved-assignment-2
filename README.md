Download Link: https://assignmentchef.com/product/solved-assignment-2
<br>
Assignment 2

2.1 Configure an Oracle user for yourself.

<ol>

 <li>As you did last assignment, start the OracleXE server, start sqlplusas the system</li>

 <li>Create a database user for yourself by saying</li>

</ol>

CREATE USER <em><u>yourId</u></em> IDENTIFIED BY <em><u>yourPassword</u></em>;

GRANT CREATE SESSION, CREATE TABLE, CREATE VIEW, CREATE MATERIALIZED VIEW, UNLIMITED TABLESPACE, CREATE SEQUENCE TO <em><u>yourID</u></em>;

<ol>

 <li>You can now logout ( exit) and log back in as yourself ( sqlplus <em><u>yourId</u></em>/<em><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="344d5b414664554747435b4650746c71">[email protected]</a></u></em> ).</li>

</ol>

2.2 Study the DDL command file for the movies database and then try the following, noting what happens and why. The sql source code can be located in Blackboard

<ol>

 <li>Try adding records to the movie relation that cause these intra-relation issues:

  <ol>

   <li>a repeated <em>primary key</em>value</li>

   <li>a NULL primary key value</li>

  </ol></li>

</ol>

<ul>

 <li>a violation of a CHECK constraint</li>

</ul>

<ol>

 <li>a violation of an SQL datatype constraint</li>

 <li>a negative score value</li>

</ol>

<ol>

 <li>Try adding records that cause these inter-relation issues:

  <ol>

   <li>a new record with a NULL value for a foreign key value</li>

   <li>a <em>foreign key</em>value in a <em>referencing</em> (aka child) table that doesn’t match any key value in the parent tableTry this on the status field of a casting record, for which the schema disallows any values not explicitly listed in the StatusValue “legal values” table.</li>

  </ol></li>

</ol>

<ul>

 <li>a key value in a <em>referenced</em>(aka parent) table with no related records in the referencing table</li>

</ul>

<ol>

 <li>Try deleting/modifying records as follows:

  <ol>

   <li>Delete a referenced record that is referenced by a referencing record.</li>

   <li>Delete a referencing record that references a referenced record.</li>

  </ol></li>

</ol>

<ul>

 <li>Modify the ID of a movie record that is referenced by a casting record.</li>

</ul>

Redo these delete/modify test cases with ON DELETE CASCADE specified in the schema for the foreign key constraints in the casting table. Note that though the text discusses it, Oracle doesn’t support ON UPDATE CASCADE .

<ol>

 <li>Can you add a constraint the requires that movies having a non-NULL score value implies that they have more than 1000 votes? If so, include theCHECKconstraint in your exercise 2 command file. If not, explain why not.</li>

</ol>

It would be wise to test the contents of your tables using simple DML commands.

2.3 Implement the ERD shown here as an Oracle database. Include a schema and 2-3 sample records for each table. Use the movies command file from lab 2 as a model for your implementation and be sure to set the constraints appropriately.

Be sure to include primary and foreign key constraints as appropriate.





