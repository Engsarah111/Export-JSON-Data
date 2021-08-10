# Export-JSON-Data


Import or export JSON data
You can use the importFile() and exportFile() Java™ APIs to import or export JSON data from a Db2® database.

You can use the com.ibm.nosql.json.api.DBCollection#importFile(String) method to import files with the *.js extension. A second integer parameter of this method indicates the commit frequency.

The following snippet from a Java program demonstrates how to import JSON data:
//Import data and commit after every 100 rows
db.collection.importFile("/temp/myjsondata.js", 100)

You can use the DBCollection.exportFile(String) method to export files with the *.js extension.

The following snippet from a Java program demonstrates how to export JSON data:
//Export data 
 db.collection.exportFile("/temp/myjsondata.js") 

Each of the *.js import or export files contains one JSON object on each line of the file in plain text format.

You can also use the JSON Java API to import files, where the first row of the file identifies field names. To import a csv file, the name must end with .csv instead of .js. The file extension provides input information to the API about the file format.
