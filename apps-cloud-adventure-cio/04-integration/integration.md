# Integration

## Introduction

We're delighted to take you on a journey that will uncover the incredible capabilities of Fusion Cloud's REST API integration tools for auditing supplier address changes. This adventure is designed to offer a holistic understanding of how these tools can streamline your supply chain security management, providing an efficient way to keep track of supplier information changes.

In the office of the Chief Information Officer (CIO), supply chain management is a complex web of interconnected processes. Our goal is to navigate this complexity and equip you with the skills to audit supplier address changes effectively. You'll learn how to leverage the power of Fusion Cloud's REST APIs, a game-changing solution that will revolutionize your operations.

We've designed this journey to be interactive and engaging. Make sure to answer the Adventure Check Point questions along the way, ensuring you capture the full potential of this experience. These check points are your path to becoming a master auditor, so pay close attention!

With your adventure hat on and a curious mind, prepare for an exhilarating exploration of Fusion Cloud's REST API integration features. Let's embark on this thrilling journey together!


Estimated Time: 15 minutes


### Objectives

In this activity you will learn the power and ease of integrating Fusion SaaS application with upstream and downstream systems



## Task 1: Use REST API to pull Fusion SaaS Application audit data for use in any external system


1. We’re going to login to Fusion Cloud ERP

    > Navigate to your Oracle Cloud ERP Demo Environment Instance and sign in with the Username and Password provided

    ![Application login page](images/image001.png)

2. Let’s navigate to the Suppliers work area to modify a supplier’s address information

    > Click the **Procurement** tab

    ![Application Homepage](images/image002.png)

    > Click the **Show More** button

    ![Procurement View](images/image003.png)

    > Click the **Manage Suppliers** button

    ![Show More View](images/image004.png)


3. Next, we’re going to search for the Supplier you’ve been assigned, e.g. “A1…”

    > Click in the **Keywords** search bar

    ![Manage Suppliers View](images/image005.png)  

    > (1) Type the name of your assigned supplier, **e.g. “a1…”** <br>

    > (2) Click the **Search** button

    ![Keywords search bar](images/image006.png)  

    > Click the **Edit** button in the ‘Search Results’ area

    ![Search Results](images/image007.png)  


4. We’re going to navigate to the Supplier’s addresses tab and edit that information 
   
    > Click the **Addresses** tab

    ![Suppliers View](images/image008.png)  

5. **Note:** If a supplier has multiple addresses, select an address that has "Address Name" filled in.

    > Click **Edit** to edit the Supplier’s address

    ![Edit Suppliers View](images/image009.png)  


6. We’re going to add a Suite (999) to the Supplier’s address information that was missing before.

    > Click in the 88Address Line 2** text entry field 

    ![Edit Suppliers View](images/image010.png)

    > Type new information into **Address Line 2**, e.g. ‘Suite 999’

    ![Edit Suppliers View](images/image011.png)

    > Click **Save and Close** 

    ![Edit Suppliers View](images/image012.png)

    > Click **Submit** 

    ![Edit Suppliers View](images/image013.png)

    > Click **OK** on the resulting confirmation box. 

    ![Suppliers View](images/image014.png)

    > Click **Done**

    ![Suppliers View](images/image015.png)



7. Let’s navigate back to the Fusion Cloud home screen.

    > Click the **Home** button

    ![Suppliers View](images/image016.png)



8. Now, we’re going to discover how we can audit several pieces of information that’s relevant to our cloud adventure today: user access (sign in / sign out) as well as supplier address information changes via REST API integrations.

    > At the home screen, navigate to **Integration** tab

    ![Home](images/image017.png)

    > Click on **Audit Report REST Endpoints**

    ![Integrations View](images/image018.png)


9. Let’s review the REST API endpoints that we can use to review Auditable data that can be extracted from Fusion Cloud.

    ![Audit Report REST Endpoints](images/image019.png)

    > Click on **Get an audit report** under **Audit Report**

    ![Audit Report REST Endpoints](images/image020.png)    

    > Click **Jump to** and select **Examples**

    ![Get an audit report](images/image021.png)   

    > Scroll down the page, review the first **Example Request Payload** and **Example of Response Body**

    ![API Examples](images/image022.png)   



10. Let’s now return to Fusion Cloud so we can audit the supplier address change we made previously using the Audit REST APIs we’ve just learned about.

    > Press **Ctrl + Tab** in your web browser to navigate back to the Fusion Cloud ERP browser tab.

    ![Application Home](images/image023.png)

    > In the Integration tab: Click on the **API Integration** tile 

    ![Integration Tab](images/image024.png)



11. Now we’re going to use the Audit REST API we just reviewed to extract auditable information from Fusion Cloud via a custom Oracle APEX application integrated with our demo environment

    > Click on **Administration** 

    ![API Application Administration](images/image025.png)
    

12. We’re going to authenticate our integration APEX application with the same ERP instance name and password we used to login into Fusion Cloud

    > Type in the provided **ERP Instance** and **ERP Password** credentials on your Cloud Adventure note card 

    ![credentials ](images/image026.png)

    > Click the **Save** button

    ![credentials ](images/image027.png)

    > Click **OK** when the **Connection is successful** message pop-up is displayed

    ![API Integration Application](images/image028.png)


13. After authenticating, we’ll navigate to the Sign on Audit area to review which users have been accessing Fusion Cloud, along with other pertinent audit details.

    > Click the **Hamburger, or triple bar** menu button

    ![credentials](images/image029.png)

    > Click the **Sign on Audit** menu button

    ![credentials](images/image030.png)

    > Click the **Get Sign on Audit Events** button

    ![Sign on Audit](images/image031.png)

    > Review the results of the user access audit REST API GET command

    ![Sign on Audit Results](images/image032.png)

    > Scroll down, Click / Expand the **Demo Flow** drop-down tab

    ![Sign on Audit Results](images/image033.png)

    > Review the Demo Flow for the Sign on Audit REST API

    ![Demo Flow](images/image034.png)

    > Click the **API Details** tab

    ![Demo Flow](images/image035.png)

    > Review a sample of the Sign on Audit REST API, including the endpoint, method, and sample response.

    ![Sample Sign on Audit](images/image036.png)


14. Now let’s review Supplier address changes recently made in the corresponding Fusion Cloud business object with the ‘Audit History’ 

    > Click the **Audit History** menu button

    ![Audit History](images/image037.png)

    > Click the **Get Audit History** button

    ![Audit History](images/image038.png)

    > Review the results of the user access audit REST API GET command

    ![Audit History Results](images/image039.png)

    > Scroll down, Click / Expand the ‘Demo Flow’ drop-down tab

    ![Audit History Results](images/image040.png)

    > Review the Demo Flow for the Audit History Audit REST API

    ![Demo Flow](images/image041.png)

    > Click the **API Details** tab

    ![API Details](images/image042.png)

    > Review a sample of the Audit History Audit REST API, including the endpoint, method, and sample response.

    ![API Details](images/image043.png)
	

15. Adventure awaits, click on the image, show what you know and rise to the top of the leader board!!!
    
    [![Cloud Adventure](images/cloud-adventure-checkpoint-image.png)](https://apex.oracle.com/pls/apex/f?p=159406:20:::::QN:13) 


## Summary (MISSING)

**You have successfully completed the Activity!**

## Acknowledgements
* **Author** - Jamil Orfali, Senior Sales Consultant, Advanced Technology Services
* **Contributors** -  
* **Last Updated By/Date** - Jamil Orfali, August 2024