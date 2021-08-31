
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

**Enter Expense Type & Approver sample data in list.** <br> 

### Step 2
Create a SP list with the following name: **Expense Reports**

<table>
  <th>Column Name</th>  <th>Column Type</th>    <th>Required</th> <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>Yes</td><td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Start Date</td>  <td>Date and time</td> <td>Yes</td><td>  </td> </tr>
   <tr> <td>End Date</td>  <td>Date and time</td> <td>Yes</td><td>  </td> </tr>
   <tr> <td>Amount</td>  <td>Currency</td> <td> <td>Yes</td> </td> </tr>
     <tr> <td>Description</td>  <td>Multi lines of Text</td> <td>Yes</td><td>  </td> </tr>
       <tr> <td>Approval Status</td>  <td>Choice</td> <td> Set Choice values as 'New, Approved, Pending, Rejected'. Set Default value of column to New. </td> </tr>
   <tr> <td>Approval History</td>  <td>Multi lines of Text</td> <td>  </td> </tr>
  <tr> <td>Expense Type</td>  <td>Lookup</td><td>Yes</td> <td> Lookup Title column of "Expense Types" list created earlier. To create lookup column go to list settings.  </td> </tr>
    <tr> <td>Approvers</td>  <td>Person</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true. </td> </tr>
    <tr> <td>Approver Index</td>  <td>Number</td> <td> Set "Number of decimal places" for column to 0. </td> </tr>
</table>

Ensure all of the columns mentioned in the above table + "Created By" column are a part of the "All Items" View.

For "Approval Status" column > apply column formatting > add json as provided in link below.<br> 
[Import JSON](https://github.com/rdorrani/SharePoint/blob/master/ExpenseReportingWorkflow/Approval%20Status%20Column.json).

For "All Items" view switch to Gallery view and apply the json as provided in link below.<br> 
[Import JSON](https://github.com/rdorrani/SharePoint/blob/master/ExpenseReportingWorkflow/Tiles%20Formatting%20for%20All%20Items%20View.json).<br> 
For Gallery view > format current view > advanced mode > add the JSON. <br> 
Save the view.<br> <br> 

Form Configuration for list.<br> 
Header JSON [Import JSON](https://github.com/rdorrani/SharePoint/blob/master/ExpenseReportingWorkflow/header.JSON)<br> 
Body JSON  [Import JSON](https://github.com/rdorrani/SharePoint/blob/master/ExpenseReportingWorkflow/body.JSON)<br> 
Edit columns for form configuration and hide the following columns : Approval Status, Approval History, Approvers & Approver Index.<br> 


### Step 3
Go to Power Automate (flow.microsoft.com) and import the following flow:<br> 
[Import flow](https://github.com/rdorrani/SharePoint/blob/master/ExpenseReportingWorkflow/%F0%9F%92%B2ExpenseReportApprovalWorkflow_20210831225203.zip). <br> <br> 
Once imported, ensure you update all the SharePoint actions to point to your newly created lists.  <br> 
Follow Video to see the lists being referenced in specific actions in flow. <br>
Make sure to turn the flow on.<br><br>
If Import fails then click on "Save as a new flow" link option in error message.



