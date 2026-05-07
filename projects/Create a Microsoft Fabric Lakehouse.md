1. Navigate to the Microsoft Fabric home page at in a browser, and sign in with your Fabric credentials.
2. In the menu bar on the left, select Workspaces 
3. Create a new workspace with a name of your choice, selecting a licensing mode in the Advanced section that includes Fabric capacity (Trial, Premium, or Fabric).
4. When your new workspace opens, it should be empty.

<img width="2801" height="1997" alt="image" src="https://github.com/user-attachments/assets/83aeddfe-c9f1-49b0-a9ee-0695ee98264c" />

# Create a lakehouse 

1. On the menu bar on the left, select Create. In the New page, under the Data Engineering section, select Lakehouse. Give it a unique name of your choice. Make sure the “Lakehouse schemas (Public Preview)” option is disabled.
2. After a minute or so, a new lakehouse will be created:
<img width="2801" height="1997" alt="image" src="https://github.com/user-attachments/assets/38ab160b-54ae-4c4a-b55f-55cc372617d7" />
3. View the new lakehouse, and note that the Lakehouse explorer pane on the left enables you to browse tables and files in the lakehouse:

-  The Tables folder contains tables that you can query using SQL semantics. Tables in a Microsoft Fabric lakehouse are based on the open source Delta Lake file format, commonly used in Apache Spark.
-  The Files folder contains data files in the OneLake storage for the lakehouse that aren’t associated with managed delta tables. You can also create shortcuts in this folder to reference data that is stored externally.

Currently, there are no tables or files in the lakehouse.

Upload a file
- Fabric provides multiple ways to load data into the lakehouse
- built-in support for pipelines that copy data from external sources
- data flows (Gen 2) that you can define using visual tools based on Power Query
- the simplest ways to ingest small amounts of data is to upload files or folders from your local computer.

Download the sales.csv file on your local computer.

-  Return to the web browser tab containing your lakehouse, and in the … menu for the Files folder in the Explorer pane, select New subfolder, and create a subfolder named data.
-  In the menu for the new data folder, select Upload and Upload files, and then upload the sales.csv file from your local computer (or lab VM if applicable).
-  After the file has been uploaded, select the Files/data folder and verify that the sales.csv file has been uploaded, as shown here:

 <img width="1917" height="493" alt="image" src="https://github.com/user-attachments/assets/c900f7eb-5a7c-4774-b09a-bdd030588e5b" />


Explore shortcuts
- In many scenarios, the data you need to work with in your lakehouse may be stored in some other location.
- While there are many ways to ingest data into the OneLake storage for your lakehouse, another option is to instead create a shortcut.
- Shortcuts enable you to include externally sourced data in your analytics solution without the risk of data inconsistency associated with copying it.

1. In the Explorer pane, select the Files/data folder so you can see the sales.csv file it contains.
2. In the … menu for the sales.csv file, select Load to Tables > New table.
3. In Load to table dialog box, set the table name to sales and confirm the load operation. Then wait for the table to be created and loaded.
4. Select CSV for the file type. Then wait for the table to be created and loaded.
5. In the Explorer pane, select the sales table that has been created to view the data.
<img width="2669" height="910" alt="image" src="https://github.com/user-attachments/assets/103a22d5-9835-4aaf-a0db-081d38f30e62" />
6. In the menu for the sales table, select View files to see the underlying files for this table.
   Note -  Files for a delta table are stored in Parquet format, and include a subfolder named _delta_log in which details of transactions applied to the table are logged.
- 
