# LAB Business Process Flows and Business Rules

**Source:** PL-100

In this lab you will enhance the data model and improve the app behavior by adding a business process flow and a business rule.

---

<br/>

### Exercise 1: Import existing solution
In this exercise, you will import existing solution and add data to the Dataverse tables.

1. Create solution named PL-100 with pl100 prefix.

1. Download the following files
    * [Company311_1_0_0_1.zip](https://github.com/MicrosoftLearning/PL-100-Microsoft-Power-Platform-App-Maker/blob/master/Instructions/Labs/02-1/Completed/Company311_1_0_0_1.zip?raw=true)
    * [DataImport.zip](https://github.com/MicrosoftLearning/PL-100-Microsoft-Power-Platform-App-Maker/blob/master/Instructions/Labs/02-1/Resources/DataImport.zip?raw=true)

1. Import Company311_1_0_0_1.zip solution.

1. Publish all customizations.

1. Add the following departments in **Departments** table at **Company 311** solution.
    * Human Resources
    * Marketing

1. Add the following buildings in **Buildings** table at **Company 311** solution.
    * San Francisco Main Campus
    * London Paddington

1. Add the following issue in **Problem Report** table at **Company 311** solution.
  
    |Title | Building | Department | Details  |
    | --- | --- | --- | --- |
    | Enter Broken door for Title | San Francisco Main Campus | Maintenance |The main entrance door will not open all the way |

1. Import DataImport.zip solution.

1. Publish all customizations.

1.  Open the **Data Import** solution you imported.

1. Select the **Import Data** flow.

    ![image](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-1/media/image90.png)

1. Click **Run** to execute the flow.

1. Wait for the flow run to complete. Select the Refresh Flow runs button to check if the flow run completes successfully.

    ![image](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-1/media/image93.png)

1. Return to **Company 311** solution. 

1. Check that the **Problem Report** table contains new data.

<br/>

### Exercise 2: Create business rule

#### Task 1: Customize Table

In this task, you will add a lookup Column to the problem report table.

1.  Navigate to the [Power Apps maker portal](https://make.powerapps.com/) page and make sure you are in the correct environment.

2.  Select **Solutions** and open the **Company 311** solution.

3.  Locate and open the **Problem Report** table. 

4.  Select **+ New**, then select **Column**. 

5.  Enter **Assign to** for **Display name**, select **Lookup** for **Data type**, select **User** for **Related table**, and select **Save**.

    ![A screenshot of the column properties panel for Assign To column with all relevant values in each field](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image1.png)

6.  Select **All** in the **Objects** navigation tree.

7.  Select **Publish all customizations** and wait for the publishing to complete.


#### Task 2: Create business process flow

In this task, you will create a business process flow for the Problem Report table.

1.  Navigate to the [Power Apps maker portal](https://make.powerapps.com/) page and make sure you are in the correct environment.

2.  Select **Solutions** and open the **Company 311** solution.

3.  Select **+ New > Automation > Process > Business process flow**.

    ![image-20221004145025636](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image2.png)

4.  In the **New business process flow** panel enter **Problem resolution process** for **Display name**, select **Problem Report** for **Table**, and select **Create**.

    ![A screenshot of New business process flow panel with relevant field values.](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image3.png)

5.  Open the **Problem resoultion Process**' Business Process flow created in the previous step. Select the **New stage**, go to the **Properties** pane, change the **Display Name** to **Route**, and select **Apply**.

    ![A screenshot of the new stage and properties pane](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image4.png)

6.  Expand **Details** of the **Route** stage.

    ![A Screenshot with an arrow pointing to the details button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image5.png)

7.  Select **Data Step \#1**, go to the **Properties** pane, select **Building** for **Data Field**, and select **Apply**.

    ![A screenshot of the new stage with data step one selected and the properties pane open](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image6.png)

8.  Select **+ Add** and select **Add Data Step**.

    ![A Screenshot with an arrow pointing to the add button and a border around add data step button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image7.png)

9.  Select the **+** option to add the data step below the **Building** data step.

    ![A screenshot of a data step being about to be added to the process stage](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image27.png)

10. Select the new data step, go to the **Properties** pane, select **Location** for **Data Field**, and select **Apply**.

11. Select **+ Add** again and select **Add Data Step**.

12. Select the new data step, go to the **Properties** pane, select **Department** for **Data Field**, and select **Apply**.

13. The **Route** stage should now look like the image below.

    ![A screenshot of the completed route stage with three data steps: building, location, and department](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image8.png)

14. Select **+ Add** and select **Add Stage**.

15. Add the new stage after the **Route** stage.

16. Select the stage, go to the **Properties** pane, enter **Fix** for **Display Name**, and select **Apply**.

17. Expand **Details** of the **Fix** stage.

18. Select **Data Step \#1** of the **Fix** stage.

19. Go to the **Properties** pane, select **Assign to** for **Data Field** and select **Apply**.

20. Select **+ Add** and select **Add Stage**.

21. Add the new stage after the **Fix** stage.

22. Select the new stage, go to the **Properties** pane, enter **Resolve** for **Display Name** and select **Apply**.

23. Expand **Details** of the **Resolve** stage.

24. Select **Data Step \#1** of the **Resolve** stage.

25. Go to the **Properties** pane, select **Resolution** for **Data Field** and select **Apply**.

26. Select **+ Add** and select **Add Data Step**.

27. Add the new data step below the **Resolution** data step.

28. Select the new data step, go to the **Properties** pane, select **Resolved on** for **Data Field** and select **Apply**.

29. The Business process flow should now look like the image below. Select **Save**.

    ![A screenshot of a Business Process Designer with an arrow pointing to the save button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image9.png)

30. Select **Activate**.

31. Select **Activate** again on the pop-up.

32. Confirm that Status: **Active** shows at the bottom left of the Business Process Flow canvas.

    ![A screeshot of a high-level overview of a business process with the words "Status: Active" highlighted in the left bottom corner](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image28.png)

33. Close the process editor browser window or tab.

34. Select **Done**.

<br/>

### Exercise 3: Create business rule

In this exercise, you will create a business rule that will block completion of problems without resolution.

#### Task 1: Create business rule

1.  Navigate to the [Power Apps maker portal](https://make.powerapps.com/) page and make sure you are in the correct environment.

2.  Select **Solutions** and open the **Company 311** solution.

3.  Locate and open the **Problem Report** Table.

4.  Select **+ New** and under **Customizations**, select **Business rule**.

    ![A screenshot of the flyout New menu with the cursor positioned over the highlighted Business rule entry](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image12.png)

5.  Make sure the **Scope** is set to **Entity** and select the **Show details** chevron.

    ![A Screenshot with an arrow pointing to the drop down icon next to the text problem report: new business rule and a border around the scope set to entity on the right hand side of the page](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image13.png)

6.  Change **Business rule name** to **Completion rule** and select the **Hide details** chevron.

    ![A screenshot of a business rules property pane with an arrow pointing to the shevron that collapses the entire property pane](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image29.png)
 
7.  Select the **Condition**.

8.  Go to the **Properties** pane and change the **Display name** to **Resolution required**.

9.  Scroll down the **Rules** section, select **Status Reason** for **Field**, select **Equals** for **Operator**, select **Value** for **Type**, select **Completed** for **Value**, and select **Apply**.

    ![A screenshot of the rules panel](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image14.png)

10. Select **+ New**.

    ![A Screenshot with an arrow pointing to the new button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image15.png)

11. Scroll down to **Rule 2**, select **Resolution** for **Field**, select **Does not contain data** for **Operator**, make sure **And** is selected for **Rule Logic**, and select **Apply**.

    ![A screenshot of the rules panel if you scroll further down with the relevant text in each field](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image16.png)

12. Select **+ Add**.

    ![A Screenshot with an arrow pointing to the add button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image17.png)

13. Select **Add Show Error Message**.

14. Add the action on the **true** path of the condition.

    ![A Screenshot with an arrow pointing to the add button on the true path of the condition](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image18.png)

15. Select the new action, go to the **Properties** pane, enter **Show message** for **Display Name**, select **Status Reason** for **Field**, enter **The Problem must have a resolution before it can be closed** for **Message**, and select **Apply**.

    ![A screenshot of the properties panel with the relevant text in the fields](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image19.png)

16. The business rule should now look like the image below. Select **Save**.

    ![A Screenshot with an arrow pointing to the save button](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image20.png)

17. Select **Activate**.

18. Select **Activate** again on the pop-up.

19. Confirm activation. The **Activate** button will change to **Deactivate** and it will show **Activated** in the bottom left of the Business Rule canvas.

20. Close the process editor browser window or tab.

21. Select **Done**.

<br/>

### Exercise 4: Test processes

In this exercise, you will test the business process flow and the business rule you created.

#### Task 1: Test processes

1.  Navigate to the [Power Apps maker portal](https://make.powerapps.com/) page and make sure you are in the correct environment.

2.  Select **Apps** and open the **Company 311 Admin** application.

    ![A Screenshot with an arrow pointing to the company 311 admin option in apps](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image21.png)

3.  Select **Problem Reports** and select **+ New**.

4.  You should see the business process flow stages. Enter **Dark parking lot** for **Title**, select **London Paddington** for **Building**, enter **There are no lights at the north end of the parking lot** for **Details**, and select **Save**.

    ![A screenshot of the new problem report](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image22.png)

5.  Select the **Route** stage.

    ![A Screenshot with an arrow pointing to the route stage at the top of the page](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image23.png)

6.  Enter **North-end** for **Location**, select **Facility Maintenance** for **Department** and select the **Next stage** button.

    > **NOTE**
    >
    > If the **Next Stage** button is not visible, then refresh the page.

    ![A screenshot of the drop down from the route stage with the relevant options selected and entered](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image24.png)

7.  Select a user for **Assign to** and select **Next Stage**.

8.  Select date and time for the **Resolved on** and leave the **Resolution** value empty.

9.  Scroll down to the **Resolution details** section and select **Completed** for **Status Reason**. You should see the business rule error message defined earlier.

    ![A screenshot of the error message under status reason](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image25.png)

10. Provide a value for **Resolution**. The error message should go away.

    ![A screenshot of the form without the error message after resolution](https://microsoftlearning.github.io/PL-100-Microsoft-Power-Platform-App-Maker/Instructions/Labs/02-2/media/image26.png)

11. Select **Save** to save the Problem Report.
