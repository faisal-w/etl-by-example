ETL By Example
=========

The purpose of this project is to provide a collaborative environment for learning how to perform "Extract Transform Load" (ETL) processes using Hadoop.

The hope is that through sample code and detailed explanations in the wiki, the learning process for data ETL will be simplified. We are encouraging others to contribute.

Please refer to the project wiki for further information (https://github.com/Lab41/etl-by-example/wiki)

What the code does
============
The actual code in this project ingests "SampleRecords" from a CSV file generated by the Generate class.  We read the files with a mapper, convert to Avro in the reducer, pivoting on a time field in each record.  When running via oozie, we then move the original files to an archive, and then move the converted files to a directory intended for querying.


Getting Started
========

1. Clone the project
2. mvn package
3. create sample data Generator.java
3. Run the project (Two ways)
      - Via a driver ->  ./bin/run.sh
      - Via oozie -> use workflow in src/main/workflow

Contributing
========

Contributions are most welcome to both the wiki and the code.  To contribute, issue a pull request, make the changes, and we will merge it back into the trunk. 