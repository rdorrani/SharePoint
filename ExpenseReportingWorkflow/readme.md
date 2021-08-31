
[![Everything Is AWESOME](http://img.youtube.com/vi/gb_FUeRjgg4/maxresdefault.jpg)](https://www.youtube.com/watch?v=gb_FUeRjgg4 "Power Automate Multi Level Approval Workflow with SharePoint")
**Click image to view video**

# SharePoint Expense Reporting Solution

### Step 1
Create a SP list with the following name: **Expense Types**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true.</td> </tr>
</table>

** *Enter Expense Type & Approver data in list.** <br> 

### Step 2
Create a SP list with the following name: **Expense Reports**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Start Date</td>  <td>Date and time</td> <td>  </td> </tr>
   <tr> <td>End Date</td>  <td>Date and time</td> <td>  </td> </tr>
   <tr> <td>Amount</td>  <td>Currency</td> <td>  </td> </tr>
     <tr> <td>Description</td>  <td>Multi lines of Text</td> <td>  </td> </tr>
       <tr> <td>Approval Status</td>  <td>Choice</td> Set Choice values as 'New, Approved, Pending, Rejected'. Set Default value of column to New.<td>  </td> </tr>
   <tr> <td>Approval History</td>  <td>Multi lines of Text</td> <td>  </td> </tr>
  <tr> <td>Expense Type</td>  <td>Lookup</td> <td> Lookup Title column of "Expense Types" list created earlier. To create lookup column go to list settings.  </td> </tr>
    <tr> <td>Approvers</td>  <td>Person</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true. </td> </tr>
    <tr> <td>Approver Index</td>  <td>Number</td> <td> Set "Number of decimal places" for column to 0. </td> </tr>
</table>

Ensure all of the columns mentioned in the above table + "Created By" column are a part of the "All Items" View.

For "Approval Status" column > apply column formatting > add json as provided in link below.
[Import JSON](https://github.com/rdorrani/PowerApps/blob/master/DocLibraryBrowser/DocumentLibraryExplorer_20210608135241.zip).

For "All Items" view switch to Tiles view and apply the json as provided in link below
[Import JSON](https://github.com/rdorrani/PowerApps/blob/master/DocLibraryBrowser/DocumentLibraryExplorer_20210608135241.zip).
For Tiles view > format current view > advanced mode > add the JSON.
Save the view.


### Step 3
Go to Power Automate (flow.microsoft.com) and import the following flow:
[Import flow](https://github.com/rdorrani/PowerApps/blob/master/DocLibraryBrowser/DocumentLibraryExplorer_20210608135241.zip).
Once imported, ensure you update all the SharePoint actions to point to your newly created lists.



