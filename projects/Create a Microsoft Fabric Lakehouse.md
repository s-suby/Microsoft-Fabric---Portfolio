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
-       Fabric provides multiple ways to load data into the lakehouse
-       built-in support for pipelines that copy data from external sources
-       data flows (Gen 2) that you can define using visual tools based on Power Query
-       the simplest ways to ingest small amounts of data is to upload files or folders from your local computer.

Download the sales.csv file on your local computer.

-  Return to the web browser tab containing your lakehouse, and in the … menu for the Files folder in the Explorer pane, select New subfolder, and create a subfolder named data.
-  In the menu for the new data folder, select Upload and Upload files, and then upload the sales.csv file from your local computer (or lab VM if applicable).
-  fter the file has been uploaded, select the Files/data folder and verify that the sales.csv file has been uploaded, as shown here:
 
