# Configure & Extend

<!-- rem ## Path 1: Configure -->
## **Configure the Change Salary Experience**

### **Introduction**

Oracle offers hundreds of prebuilt pages, workflows and forms “out of the box” as part of the Oracle Fusion Cloud.  Many of our customers want to configure these pages and workflows to meet their specific business needs.  You can unify your experience in our applications by using Redwood.

Oracle Redwood is Oracle Fusion’s new design system that enhances the user experience through a visually stimulating, easy-to-use interface. By uniting customer-inspired design philosophies with industry-leading technology solutions, Oracle Redwood helps companies reduce costs, foster efficiency, revitalize the customer journey, and evolve continuously toward the future.

### **Objectives**

In this lab, you will use Redwood to quickly and efficiently improve the user experience in Oracle Fusion Cloud.

Estimated Time: 15 minutes

Do not forget to answer the Adventure Check Point questions at the end of the exercise!

### **Begin Exercise**

1. You will use Redwood, Oracle’s next-generation design system, and Visual Builder to quickly and efficiently update Change Salary Page for Non-HR managers.

    ![Configuration Objectives](../02-configure/images/configure_objs_hcm.png)

2. You will first navigate to the Change Salary Page.

    > (1) From the application home page, click on the **My Team** tab.

    ![Application Home Page](../02-configure/images/hcmconfigimage002.jpg).

3. You can access Change Salary from an individual worker record, from the search bar, or via the Quick Actions feature.

    > (1) Click on **Change Salary** under **Quick Actions**.

    ![My Team Page](../02-configure/images/hcmconfigimage003.jpg)

4. By default this screen shows information on any Direct Reports.  Since you don't have any, you can remove this filter.

    > (1) Click on the ![x icon](../02-configure/images/icon011_x.png)  **Icon** to remove the Direct Reports Filter because your user does not have any direct reports.  This action allows you to see other people.

    ![My Team Page](../02-configure/images/hcmconfigimage004.jpg)


5. Now you will enter the Change Salary Form so we can make the required changes using Visual Builder Studio.  Now you will select a person so you can enter the Change Salary form.

    > (1) Search for **Barrett Reed** in the search field. <br>

    > (2) Select **Barrett Reed** in the drop down. <br>

    ![Change Salary Page](../02-configure/images/hcmconfigimage005.jpg)

6.  You have entered the Change Salary Form.  Now you will quickly review the current configuration of the Change Salary Form.  You need to enter in some information to access the form


    > (1) When does the salary will start?: Type a **future date** <br>

    > (2) What is the action name?: Select **Change Salary**. <br>

    > (3) Why you are changing the salary?: Select **Career Progression**. <br>

    > (4) Click **Continue** once complete.

    ![Change Salary Page](../02-configure/images/hcmconfigimage006.jpg)


7. You will now create new rule that hides Annualized Full-Time Salary because it is repetitive.  You will also hide Compa-Raito since this is mainly used by HR.  You also want to show the action reason in this section of the Change Salary Form.  We can make these configuration changes by leveraging the embedded Vision Studio Builder capabilities.

    > (1) No action is required for Step 1.  Just note that the Annualized Full-Time Salary and Compa-Ratio fields are visible. <br>
    > (2) Click the **logged in user icon** icon ![co image](../02-configure/images/icon012_co.png) next to the bell icon in the top right corner of the screen and select **Edit Page in Visual Builder Studio** from the resulting drop-down.

    ![Change Salary Page 2nd page](../02-configure/images/hcmconfigimage007.jpg)


8.  Welcome to Oracle Visual Builder Studio (VB Studio), a robust application development platform that helps your team effectively plan and manage your work throughout all stages of the app dev lifecycle: design, build, test, and deploy. Now we will use VB Studio to make the required changes to the Change Salary Form.

    > (1) Click on **Configure Fields and Regions** button.

    ![VB Studio](../02-configure/images/hcmconfigimage008.jpg)


9. First we will create a new form rule for change salary.

    > (1) Click on the ![plus icon](../02-configure/images/icon015_plus.png)  **Icon** to add a new form rule.

    ![Fields and Regions](../02-configure/images/hcmconfigimage009.jpg)


10. You can name your new rule and optionally include a description.

    > (1) Label: Type **Change Salary Non-HR**. <br>

    > (2) Click the **Create** button.

    ![Fields and Regions](../02-configure/images/hcmconfigimage010.jpg)


11.  You will add the Conditions for this rule to apply to all non-HR personnel.

    > (1) Click on the **Edit button.**

    ![Fields and Regions](../02-configure/images/hcmconfigimage011.jpg)

12.  You can complete the additional fields in User Roles condition in the first line. This configuration displays this version of the Change Salary Form to all people who are not assigned to the Human Resource Manager Role.

    > (1) For 2nd column in the **User Roles** row, select **does not contain** from the drop down.  <br>

    > (2) For 3nd column in the **User Roles**, type **Human Resource Manager** and select **Human Resource Manager** from the resulting dropdown.<br>

    > (3) Click on the **Drop Down** ![drop down icon](../02-configure/images/icon013_dropdown.png)  Icon to the left of Salary to expand the salary section

      ![Fields and Regions](../02-configure/images/hcmconfigimage012.jpg)


13.  Now you want to add and hide fields.

     > (1) Action Reason: select **Visible**     <br>

     > (2) Annualized Full-Time Salary: select **Hidden**   <br>

     > (3) Compa-Ratio: select **Hidden**  <br>

     > (4) Click the ![done icon](../02-configure/images/icon_done.png) icon to complete the definition of this rule.<br>

     > (5) Click the ![x icon](../02-configure/images/icon101_x.png) to close the Fields and Regions section.

     ![Salary Fields and Regions](../02-configure/images/hcmconfigimage013.jpg)


14. Now you will add a validation step for the Adjustment Percentage.  You do not want users to enter in a Salary Percentage Greater than 15%

    > (1) Click on **Configure Validations**

    ![Fields and Regions](../02-configure/images/hcmconfigimage014.jpg)

15. You can see any existing Validations and/or create new ones.

    > Click on **+ Validation**

    ![Validation](../02-configure/images/hcmconfigimage015.jpg)

16. Your first step is the name your Validation.

    > (1) Label: type **Adjustment Percentage**.    <br>

    > (2) Click the **Create** button.

    ![Validation](../02-configure/images/hcmconfigimage016.jpg)


17.  Now you will set the conditions for this rule so that the form will not accept any adjustment percentage greater than 15%.

     > (1) Click on **Edit**.

     ![Create Validation](../02-configure/images/hcmconfigimage017.jpg)

18.  Instead of using the pre-define condition rows, you'll create a new one.

     > (1) Click on **+ Condition**.

     ![Create Condition](../02-configure/images/hcmconfigimage018.jpg)

19.  For the first field on the condition, you'll want to use the Adjustment Percentage.  <br>![caution](../02-configure/images/cautionflagextrasmalltransparent2.png)**Note:** **Adjustment Percentage** will appear multiple times in the list of values, so be sure to select the correct one as described below.

     > (1) Type **Adjustment Percentage** in the box and select the 1st **# Adjustment Percentage** under **Salary Details** from the resulting list of values.    <br>

     ![Create Validation](../02-configure/images/hcmconfigimage019.jpg)

20.  For the second field on the condition, you'll specify the operator.

     > (1) Select **greater than** from the dropdown.   <br>

     ![Create Validation](../02-configure/images/hcmconfigimage020.jpg)

21.  For the third field on the condition, you'll specify the comparison value. <br>![caution](../02-configure/images/cautionflagextrasmalltransparent2.png)**Note:** if the 3rd data entry field is obscured by the list of values, press the esc key on the upper left of your laptop keyboard.

    > (1) Type **15**

    ![Create Validation](../02-configure/images/hcmconfigimage021.jpg)

22. Now you will configure the error message users will see if they enter an Adjustment Percentage greater than 15%.

     > (1) Summary: type **Adjustment Percentage is too high**.    <br>

     > (2) Severity:  Select **Error**. <br>

     > (3) Detail:  type **The Adjustment Percentage must be lower than 15%**. <br>

     > (4) Click the ![done icon](../02-configure/images/icon_done.png) icon to complete the definition of this rule.<br>

     > (5) Click the ![x icon](../02-configure/images/icon101_x.png) to close the Validations section.

     ![Create Validation](../02-configure/images/hcmconfigimage022.jpg)


23.  Well done.  You have configured a new rule for Non-HR personnel.  You can quickly review your changes as they appear in the application.

    > (1) Click on the **Preview** ![preview icon](../02-configure/images/icon014_preview.png) icon in the top right of the screen.
       <br>![caution](../02-configure/images/cautionflagextrasmalltransparent2.png)**Note:** This will open the application in a new browser tab.<br>

       ![Create Validation](../02-configure/images/hcmconfigimage023.jpg)

24.  You have re-entered the Change Salary Form.  Let’s review the changes.  You need to enter the required information before you can move to the next screen.

    > (1) When does the salary will start?: Type a **future date** <br>

    > (2) What is the action name?: Select **Change Salary**. <br>

    > (3) Why you are changing the salary?: Select **Career Progression**. <br>

    > (4) Click **Continue** once complete.

     ![Change Salary Page 2nd page](../02-configure/images/hcmconfigimage024.jpg)


25.  Note that Annualized Full-Time Salary and Compa-Ratio are no longer visible and Action Reason is now Visible. Now you will test the validation for the Adjustment Amount Percentage.

    > (1) Enter an Adjustment Percentage that is greater than 15% and either **tab** out of the field or press the **Enter** key on the keybord.

    ![Change Salary Screen 2](../02-configure/images/hcmconfigimage025.jpg)

26.  The system will not allow the user to continue because the Adjustment Percentage exceeds 15%!

    ![Change Salary Screen 2 error message](../02-configure/images/hcmconfigimage026.jpg)

27.  Congratulations!  ![checkered flag](../02-configure/images/checkeredflag.jpg)

    > You've completed this Adventure.  Please close this tab and the Visual Builder tab and get ready for your next Adventure.

27. Adventure awaits, click on the image, show what you know and rise to the top of the leader board!!!

    [![Checkpoint](../02-configure/images/cloud-adventure-checkpoint-image.png)](https://apex.oracle.com/pls/apex/f?p=159406:LOGIN_TEAM:::::CC:CIOADVENTURE)

<!-- rem ## Path 2: Extend -->

## **Extend with new Supplier Screen**

### **Introduction**

Oracle Cloud Applications include an embedded tool called Visual Builder.  Visual Builder is the same tool that Oracle uses to develop application screens and it's available for you to create additional screens.  These screens can leverage both Oracle Cloud Application data and, if necessary, data from external systems.

### **Objectives**

In this lab, you will use Visual Builder to create additional screens

Estimated Time: 15 minutes

Do not forget to answer the Adventure Check Point questions at the end of the exercise!

### **Begin Exercise**

1. In this lab, you will Use Visual Builder to build a new Supplier Screen.

    ![New Screen Process Flow](../03-extend/images/supplierscreenobjs2.png)

2. We will now create a new application screen to allow editing of specific supplier information.  Oracle Cloud Applications include an embedded tool called Visual Builder.  Visual Builder is the same tool that Oracle uses to develop application screens and it's available for you to create additional screens.  These screens can leverage both Oracle Cloud Application data and, if necessary, data from external systems.

    > (1) **Click** on the **‘Configuration’** tab. <br>
    > (2) **Click** on the **‘Visual Builder’** tile <br>

    ![Open Visual Builder](../03-extend/images/image001.png)

3. We have pre-defined a Project.  A project collects all the people, tools, and processes you need to complete a unit of work.  You can use a project to host source code files, track issues, collaborate on code, and build and deploy your applications. If your team is extending Oracle Cloud Applications, you’ll probably want to set things up so that you have a single project dedicated to work with a single repository for each Application.

    > **Click** on the **‘CloudAdventure’** project

    ![open project](../03-extend/images/image002.png)

4. Workspaces allow you to segregate units of work within a Project.

    > **Click** on the **‘Manage Workspaces’** link.  If your Project has no pre-existing workspaces, you'll be presented with a **‘Go to Workspaces’** button to click instead.  The following screenshots show both potential screens.

    ![workspace](../03-extend/images/image003.png)
    ![workspace](../03-extend/images/image003b.png)

5. We'll create a new workspace for our simplified supplier screen

    > (1) **Click** on the **‘New’** ![New drop down](../03-extend/images/icon017_dropdown.png) dropdown <br>
    > (2) **Select** **‘New Application Extension’** from the resulting dropdown

    ![workspace](../03-extend/images/image004.png)

6. We'll name our new Extension.

    > (1) **Enter** **‘QuickSupplier#’** in the "'Extension Name'" field.<br>
    > (2) **Click** the **‘Create’** button

    ![create extension](../03-extend/images/image005.png)

7. We're now at the Visual Builder homepage.  We can configure existing screens, create new ones, or build whole new applications.  We can also leverage REST APIs to access Fusion SaaS Data.  Supplier data from Oracle ERP/SCM Cloud, so we'll leverage the embedded integration via REST APIs.

    > (1) **Click** the **‘Services’** ![Services Icon](../03-extend/images/icon018_services.png) icon on the left menu.

    ![add UI Screen](../03-extend/images/image006.png)

8. We can add services from Oracle Cloud Applications or other accessible data sources.

    > (1) **Click** on the **‘+ Service Connection’** button.

    ![create UI](../03-extend/images/image007.png)

9. There are multiple ways to reference a service.  We'll use the included catalog of Oracle Cloud Application services.

    > **Click** on the **‘Select from Catalog’** tile.

    ![view default screen template](../03-extend/images/image008.png)

10. Services are available for functionality across the Oracle Cloud Applications.

    > **Click** on the **‘‘Enterprise Resource Planning and Supply Chain’** tile.

    ![manage services](../03-extend/images/image009.png)

11. We'll use the Supplier Service from the ERP/SCM Catalog.

    > (1) **Enter** ‘Suppliers’ in the 'Supplier Name' field. <br>
    > (2) Enter ‘Suppliers’ in the ‘Filter Objects/Endpoints’ field. <br>
    > (3) Click the ‘Checkbox’ next to ‘Suppliers’. <br>
    > (4) Click the ‘Create’ button. <br>

    ![create service connect](../03-extend/images/image010.png)

12. The resulting screen shows additional configuration options for our supplier service, but we'll just use the default settings.  We can also see the Endpoints details related to our Suppliers service.

    > **Click** on the **‘Endpoints’** tab as shown.

    ![select from catalog](../03-extend/images/image011.png)

13. Here we see the various operations and data objects available.  This includes Get, Post and Patch operations allowing for query, create and update actions  Scrolling this window we can see that other related information is also available, including addresses, attachments, contacts, descriptive flexfields and more. Now we want to start creating our new screen.

    > **Click** on the **‘App UIs’** ![App UIs Icon](../03-extend/images/icon019_apps_uis.png) icon in the left toolbar

    ![select from catalog](../03-extend/images/image012.png)

14. You can now see the App UI panel on the left hand side.  This allows you to create you new page.

    > **Click** on the **‘+ App UI’** button.

    ![select ERP/SCM](../03-extend/images/image013.png)

15. You can name your App UI.

    > (1) **Enter** **‘QuickSupplierUI’** in the "'App UI Name'" field.<br>
    > (2) **Click** the **‘Create’** button.

    ![get supplier service](../03-extend/images/image014.png)

16. Visual Builder has automatically created a default UI leveraging the Oracle provided Redwood template.  Redwood is Oracle's design methodology and pre-defined templates, and design patterns are included in Visual Builder to allow you to create applications that look and function just like Oracle delivered applications.

    > **Double-Click** the **‘main-start’** object.

    ![create supplier service](../03-extend/images/image015.png)

17. Here we see our blank template and a list of some of the provided Redwood design components.  We want to start by adding some components to the screen to hold our data.

    > (1) Confirm you’re in the **Components** tab. <br>
    > (2) Type **Panel** in the **‘filter’** field. <br>
    > (3) Drag **Panel** to the dashed rectangle object and drop it in the blue columns that appear (4) shown.

    ![create supplier service](../03-extend/images/image016.png)

18. Next, you'll add a component to the panel.  The first component we add with be an Input Text field to allow for searching.

    > (1) Confirm you’re in the **Components** tab. <br>
    > (2) Type **text** in the **‘filter’** field. <br>
    > (3) Drag **Input Text**  and drop in the blue section that appears when you drop into the Panel (4).

    ![create supplier service](../03-extend/images/image017.png)

19. In the next 2 steps, you'll add label to your search field and create a page variable.  You can start with the label.

    > (1) Type **Enter Supplier Name Search** in the **Label Hint** field on the **General** tab of the **Properties** panel on the right. <br>
    > (2) Click the **Data** tab in the **Properties** panel. <br>

    ![create supplier service](../03-extend/images/image018.png)

20. Create a page variable to save the contents of your new Input Text field

    > (1) Click the (x) icon on the top right of the Value field.  If the (x) is not showing, move your cursor to the Value field and it will appear. <br>
    > (2) The **Variables** pop-up window will appear.  Click **Create** next to the **Page** option.

    ![create supplier service](../03-extend/images/image019.png)

21. Name your page variable.

    > (1) Type **SupplierSearchString** in the ID Field.<br>
    > (2) Click the **Create** button.

    ![create supplier service](../03-extend/images/image020.png)

22. You’ll now add a Table component to the Panel.

    > (1) Enter  **Table** in the **‘filter’** field. <br>
    > (2) Drag **Table** Table to the white space below your text field.  Be sure that it’s in the white space just below the text field and not in the brown section further down.

    ![add supplier service to screen](../03-extend/images/image021.png)

23. You now have a table to hold the data. Next, you’ll add the Supplier data from our REST API. You can use the Quick Start feature to help with this task.

    > (1) Click in the newly created **Table** region.<br>
    > (2) You should now see the Table Properties region appear on the right.

    ![table layout](../03-extend/images/image022.png)

24. The Quick Start features simply common tasks.  You can use the Add Data Quick Start feature to show data from the Supplier REST API.

    > (1) Click the **'Quick Start'** table in the Table Properties area. <br>
    > (2) Click the **'Add Data'** tile.

    ![select supplier fields](../03-extend/images/image023.png)

25. You can see the various Supplier related data available from the Supplier REST API.  You’ll just use the Suppliers data for this scenario.

    > (1)  Click **'Suppliers'** to expand the Suppliers region. <br>
    > (2)  Click **'Suppliers'** tile. <br>
    > (3) Click the **Next** button.

    ![finish supplier fields](../03-extend/images/image024.png)

26. You’ll select a few fields to display on the new screen.  This screen will be used to search for Suppliers and allow for quick update of a few pieces of Supplier Data.

    > (1)  Click **'Checkbox'** next to the following fields.  You’ll need to scroll the Endpoint Structure to see the Supplier field: <br>
           - Alias <br>
           - AlternateName<br>
           - Supplier<br>
    > (2) Confirm the list of selected fields. <br>
    > (3) Click the **Next** button.

    ![widen screen handle](../03-extend/images/image025.png)

27. Here you can configure the search field.

    > (1) Click on the **filterCriterion** field in the Target section of the screen.  This will cause a **Click to add condition** option to appear at the bottom of the screen. <br>
    > (2) Click the **Click to add condition** link.

    ![widen screen](../03-extend/images/image026.png)

28. The next 3 steps will configure the Condition for the filterCriterion.

    > (1) Type **Supplier** in the first field and pick **Supplier** from the resulting pop-up list (2).

    ![widen screen](../03-extend/images/image027.png)

29. Next you'll select the Operator

    > (1) Click in the **Operator** field and select **contains ($co)** from the resulting pop-up list (2).

    ![operator selection](../03-extend/images/image028.png)

30. And now you'll reference the page variable that we created earlier.

    > (1) Click in the **Attribute** field.<br>
    > (2) Select **$variables.SupplierSearchString** from the resulting pop-up list. <br>
    > (3) Click in the **Finish** button.

    ![widen screen](../03-extend/images/image029.png)

31. Notice that the screen auto-queried Supplier Information.  You can easily move between Design, Live and Code views of our application.  But next, you want the ability to edit data.  So, you’ll use the Quick Start again to add an edit page.

    > (1) Confirm that you're on the **Quick Start** tab. <br>
    > (2) Click the **Add Edit Page** tile.

    ![edit page quick start](../03-extend/images/image030.png)

32. You can select the same or different fields for out Edit Page.  Since the request was to create a simple page, you'll just add a few fields.

     > (1)  Click **'Checkbox'** next to the following fields.  Note that you will likely need to scroll the list of fields: <br>

      - Supplier<br>
      - SupplierNumber<br>
      - TaxpayerId<br>

    > (2)  Confirm the list of selected fields. <br>
    > (3) Click the **Finish** button.

    ![edit page quick start](../03-extend/images/image031.png)

33. You're ready to try your new page.

    > Click the **Preview** ![Preview Icon](../03-extend/images/icon016_preview.png) icon on the top right of the screen.

    ![select edit page fields](../03-extend/images/image032.png)

34. A new browser tab is launched showing our completed application.  You now have a fully functioning screen that supports query and update capabilities.

    > (1) Enter your search criteria by entering a string in the **Enter Supplier Name Search** field.  You can use **Corp** like shown in the screenshot or enter your **user number (##)** to find the Supplier with your number included as part of the name.  <br>
    > (2) Select a Supplier record by clicking on it (the row will highlight) <br>
    > (2) Click the **Edit Supplier** button.

    ![finish edit page fields](../03-extend/images/image033.png)

35. You Edit Supplier screen allows you to update the information and save. The new screen leverages the security and business rules of the application via the standard REST API.

    > (1) Note that the Supplier Number field is non-enterable.  That field is non-updateable and that condition automatically carries through to our new screen.  <br>
    > (2) The Taxpayer ID is enterable, but we’ll end here without doing the update.

    ![preview](../03-extend/images/image034.png)

36. Adventure awaits, click on the image and show what you know, and rise to the top of the leader board!!!

    [![Cloud Adventure](../00-introduction/images/adventure-checkpoint.png)](https://apex.oracle.com/pls/apex/f?p=159406:LOGIN_TEAM:::::CC:CIOADVENTURE)

### Summary

The two tasks of this Extension adventure introduced you to a few of the capabilities that customers can leverage to extend Oracle Fusion Cloud applications.  These features allow you to fine tune your Oracle Fusion Cloud Applications for peak performance, business processes tailored to you requirements, and fast, efficient usage.

You learned how to extend the applications using Oracle Visual Builder Studio to create new screens that leverage both Oracle and non-Oracle data. You also learned how to setup and defined a Guided Journey, which provides your users with the real-time, inline guidance and information required to complete their tasks.

You also learned how to leverage 3rd party Generative AI capabilities by leveraging external LLMs directly from the Guided Journey feature of Oracle Fusion Cloud Applications.
So, check your with you team, double-check your racing harness and get ready for our next Adventure.

### Learn More

- [Extending Oracle Cloud Applications with Visual Builder Studio](https://docs.oracle.com/en/cloud/paas/visual-builder/visualbuilder-building-appui)
- [Overview of Guided Journeys](https://docs.oracle.com/en/cloud/saas/human-resources/24c/faijh/overview-of-guided-journeys.html)
- [Configure User Defined Content Task Type for a Journey](https://docs.oracle.com/en/cloud/saas/human-resources/24c/faijh/configure-user-defined-content-task-type-for-a-journey.html)
- [Oracle Documentation](http://docs.oracle.com)



## Acknowledgements
* **Author** - Charlie Moff, Distinguished Cloud Technologist, Advanced Technology Services; Casey Doody, Cloud Technologist , Advanced Technology Services
* **Contributors** -  Sajid Saleem, Master Principal Cloud Technologist, Advanced Technology Services
* **Last Updated By/Date** - Casey Doody, August 2025



