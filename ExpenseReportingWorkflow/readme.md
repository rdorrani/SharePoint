
[![Everything Is AWESOME](http://img.youtube.com/vi/gb_FUeRjgg4/maxresdefault.jpg)](https://www.youtube.com/watch?v=gb_FUeRjgg4 "Power Automate Multi Level Approval Workflow with SharePoint")
**Click image to view video**

# SharePoint Expense Reporting Solution

### Step 1
Create a SP list with the following name: **Expense Types**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person</td> <td> Set "allow multiple selections" for column to true. </td> </tr>
</table>

**Enter Expense Type & Approver data in list.** <br> 

### Step 2
Create new List in Modern SharePoint site.
Name the list "Expense Types"
<br>
Create a column of type **Person** and name it **Approvers**. <br>
Set "allow multiple selections" for column to true. <br>
Enter Expense Type & Approver data in list. <br> 
<br> <br> 

### Step 2
[Import App zip file](https://github.com/rdorrani/PowerApps/blob/master/DocLibraryBrowser/DocumentLibraryExplorer_20210608135241.zip) in Power Apps. 

### Step 3
Edit the App.<br>Remove the SharePoint data source from the App & add a new SharePoint data source connection pointing to your Document Library.<br> On App OnStart function set your document library relative path.  **Set(varCurrentPath,"Shared Documents/")**

