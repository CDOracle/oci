# Create AI

<!-- rem ## Path 1: Create AI - Benefits Advisor Agent -->

## Create Policy Advisor Tool and Agent (RAG) using AI Agent Studio

### Introduction

AI Agent Studio for Fusion Applications is a comprehensive platform for creating, extending, deploying and managing AI Agents and Agent Teams across the enterprise. Oracle AI Agent Studio delivers easy-to-use tools, including advanced testing, robust validation, and built-in security, that helps Oracle Fusion Applications customers and partners create and manage AI agents. Leveraging the same technology that Oracle uses to create AI agents, Oracle AI Agent Studio enables users to easily extend pre-packaged agents and/or create new agents and then deploy and manage them.

### **Objectives**

In this activity you will use Oracle Fusion AI Agent Studio to
* Create a Benefits Advisor Document Tool that references you policy documents.
* Create a Benefits Advisor Agent for the above Tool.

### **Begin Exercise**

1. In this activity you will learn the power and ease building Agentic AI with the Oracle AI Agent Studio

    ![AI RAG Objectives](../05a-rag-agent-hcm/images/raghcmimage001.jpg)

2. The first step is to navigate to AI Agent Studio.

    > (1) Click on the **Tools** tab
    > (2) Select the **AI Agent Studio** tile

    ![Navigate to AI Agent Studio](../05a-rag-agent-hcm/images/raghcmimage002.jpg)

3. Next, we're going to create a Tool.

    > (1) Click the ![Tools](../05a-rag-agent-hcm/images/tools.jpg) button/tab at the bottom of the page

    ![Open tools](../05a-rag-agent-hcm/images/raghcmimage003.jpg)


4. Tool Creation

    > (1) Click the ![add tool](images/plusadd.jpg) button to create a new tool

    ![Create Tool](../05a-rag-agent-hcm/images/raghcmimage004.jpg)

5. Here, you will define your first Tool, a Document Tool.  This will allow the Agent to use the content of the documents to respond to user questions.

    > (1) Enter the following fields:
    * Tool Type: select **Document** from the dropdown<br>
    * Tool Name: Enter **CIOXX Benefits Document Tool**, where **##** is replaced with your user number.<br>
    * Family: select **HCM** from the dropdown<br>
    * Product: select **Benefits** from the dropdown<br>
    * Description: Enter **Benefits Document Tool** <br>

    > (2) Click the ![button](../05a-rag-agent-hcm/images/addw.jpg) button under **Documents** <br><br>

    > (3) **Scroll Down** to see the Documents fields and upload your document.

      ![Edit tool info](../05a-rag-agent-hcm/images/raghcmimage005.jpg)


6. ![flag](../05a-rag-agent-hcm/images/cautionflagextrasmalltransparent2.png) **Note:**  Now you’ll add the documents to our tool.  The documents you will add are located in the **ai documents** folder on your laptop's Desktop.

     > (1) Enter the following fields:
    * Name: Enter **CA Benefits Documents** <br>
    * Status: Select **Ready to publish** from the dropdown<br>
    * Description: Enter **Benefits Documents**<br>

     > (2) Click on the ![Drag-and-drop](../05a-rag-agent-hcm/images/dandd.jpg) region and then select the file (Cloud Adventure Benefits Highlights.pdf) from the **ai-documents** folder on the Desktop. Alternatively, drag and drop the files that folder to the Drag and Drop region.<br>

     > (3) Click the **Save** ![Home Icon](../05a-rag-agent-hcm/images/save.jpg) button on the bottom right<br>

     > (4) Click the **Create button** ![Create Button](../05a-rag-agent-hcm/images/createw.jpg) on the top right corner of the screen.<br>

      ![tool create](../05a-rag-agent-hcm/images/raghcmimage006.jpg)

7. Now, you'll create your first Agent!  You'll do that from the Agent screen within the AI Agent Studio.

    >  (1) Click the  **Agents** button/tab ![Agent Image](../05a-rag-agent-hcm/images/agentteams.jpg) at the bottom of the page.

    ![Agents Page](../05a-rag-agent-hcm/images/raghcmimage007.jpg)

8. Here you can see any existing agents.  But you want to create one.

    > (1) Click the **+ Add** button ![Add button Image](../05a-rag-agent-hcm/images/plusadd.jpg).

    ![Add Agent](../05a-rag-agent-hcm/images/raghcmimage008.jpg)

9. Define the details of the Agent.

    > (1) First, you'll enter the fields as described below:<br>
    * Agent Name: **CIO## Benefits Advisor Agent** where ## is replaced with your user nnumber.<br>
    * Family: Select **HCM** from the dropown<br>
    * Product: Select  **Benefits** from the dropdown<br>
    * Maximum Interactions: **10** <br>
    * Description: **Benefits Advisor Agent** <br>
    * Prompt: ![Alert Flat](images/cautionflagextrasmalltransparent2.png) ***Please note that the Prompt is a critical part of the Agent Definition as it provides guidance for the Agent.***  To streamline this step, we've pre-created the prompt. The prompt text is available in the **Prompt - CA Benefits Advisor Agent.txt** file in the **ai-prompts** folder on your desktop.  So, please open this file and copy the contents into the Prompt field.  Alternatively, you can copy the prompt from the **copy block** below. <br>

    > (2) **Scroll Down** to confirm that the entire prompt has been copied into the Prompt field.<br>
    > (3) Click the Create Button ![Create Button](images/createb.jpg) <br>

    ![Create Agent](../05a-rag-agent-hcm/images/raghcmimage009.jpg)

```
<copy>
AGENT ROLE

As a Benefits Analyst, your role is to efficiently access and interpret company-specific benefits documents, providing workers with clear, actionable guidance on their eligibility, coverage, and compliance requirements.

RESPONSIBILITIES

Your responsibilities include:

Benefit Policies:
  - Clearly explain the eligibility, coverage, and compliance requirements outlined in the company benefits policies.
  - Use the CA_Benefits_Document_Tool tool to retrieve policy details when answering questions.

IMPORTANT GUIDELINES
  - Provide concise, factual answers based strictly on the data retrieved.
  - Never fabricate or assume information.
  - Format your responses clearly and professionally for easy readability. </copy>
```

10. Now that you have the Agent, you need to add Tools to it.

    > (1) Click the **Tools** ![Tool Icon](../05a-rag-agent-hcm/images/toolhammericon.jpg) button on the left icon bar.<br>
    > (2) Enter **CIOXX** in the Ask Oracle field, where XX is replaced with your user number, and press the **<enter>** key or select **CIOXX** from the resulting dropdown.<br>
    > (3) Click the ![Agent Image](../05a-rag-agent-hcm/images/plusicon.jpg) icon next to the CA Benefits Document Tool. You may need to click it twice.

    ![add tool](../05a-rag-agent-hcm/images/raghcmimage010.jpg)


11. You can confirm the details of tool and continue

    > (1) Click the **+ Add** button ![Add button Image](../05a-rag-agent-hcm/images/addb.jpg).

    ![Add Agent](../05a-rag-agent-hcm/images/raghcmimage011.jpg)

12. That's it!  If necessary, you can add additional tools to your agent.  But no additional ones are required for this lab, so you can finish the Agent creation.

    > (1) Click the ![Create button Image](../05a-rag-agent-hcm/images/createw.jpg) button on the top right.

    ![Create Agent](../05a-rag-agent-hcm/images/raghcmimage012.jpg)

13. You’ve just created your first AI Agent.  In the next lab you will put this agent to work as part of an Agent Team.

      ![Add Tools Create](../05a-rag-agent-hcm/images/raghcmimage013.jpg) <br>

<!-- rem ## Path 2: Create AI - External Recall Agent -->

## Create an External Agent and Assemble a Team

### Introduction

AI Agent Studio for Fusion Applications is a comprehensive platform for creating, extending, deploying and managing AI Agents and Agent Teams across the enterprise. Oracle AI Agent Studio delivers easy-to-use tools, including advanced testing, robust validation, and built-in security, that helps Oracle Fusion Applications customers and partners create and manage AI agents. Leveraging the same technology that Oracle uses to create AI agents, Oracle AI Agent Studio enables users to easily extend pre-packaged agents and/or create new agents and then deploy and manage them.


### **Objectives**

In this activity you will use Oracle Fusion AI Agent Studio to
* Create an External API Agent that leverages an existing External API to access vehicle recall information.
* Create and assemble an Agent Team that includes the Maintenance Work Order Agent, Install Base Asset Agent, and the External API Agent you just created.
* Perform a quick test of the Agent team and publish.


### **Begin Exercise**


1. In this activity you will learn the power and ease building Agentic AI with the Oracle AI Agent Studio

    ![AI RAG Objectives](../06a-external-agent-scm/images/scmaconfigimage001.jpg)

2. The first step is to navigate to AI Agent Studio.

    > (1) Click on the **Tools** tab <br>
    > (2) Select the **AI Agent Studio** tile

    ![Navigate to AI Agent Studio](../06a-external-agent-scm/images/scmaconfigimage002.jpg)

3. Next, you'll create an AI Agent.

    > 1. Click the ![Agents](images/agentsbutton.jpg) button/tab at the bottom of the page

    ![Open tools](../06a-external-agent-scm/images/scmaconfigimage003.jpg)


4. Add an Agent.

    > 1. Click the ![add tool](images/plusadd.jpg) button to create a new Agent

    ![Create Agent Team](../06a-external-agent-scm/images/scmaconfigimage004.jpg)

5. Define the Agent.

     > (1) Enter the fields as described below:
     * Agent Name: **CIOXX External Vehicle Recall Agent** where XX is replaced with your user number. <br>
     * Family: Select **SCM** from the dropdown <br>
     * Product: Select  **Maintenance** from the dropdown <br>
     * Maximum Interactions: **10** <br>
     * Description: **External Vehicle Recall Agent** <br>
     * Prompt: ![Alert Flat](images/cautionflagextrasmalltransparent2.png) ***Please note that the Prompt is a critical part of the Agent Definition as it provides guidance for the Agent.***  To streamline this step, we've pre-created the prompt. The prompt text is available in the **Prompt - External Vehicle Recall Agent.txt** file in the **ai-prompts** folder on your desktop.  So, please open this file and copy the contents into the Prompt field.  Alternatively, you can copy the prompt from the **copy block** below.  <br>

    > (2) **Scroll Down** to confirm that the entire prompt has been copied into the Prompt field.<br>
    > (3) Click the Create Button ![Create Button](images/createb.jpg) <br>

     ![Create Tool](../06a-external-agent-scm/images/scmaconfigimage005.jpg)

```
<copy>AGENT ROLE
As a Vehicle Recall Analyst, your role is to efficiently access vehicle recall information, providing users with clear information on any recalls related to their vehicle based on vehicle make, vehicle model and vehicle model year.

RESPONSIBILITIES

Your responsibilities include:

Vehicle Recall Information:

- Clearly provide with clear information on any recalls related to their vehicle based on vehicle make, vehicle model and vehicle model year.
- Use the 1st word of the Asset description as vehicle make.
- Use the 2nd word of the Asset description as vehicle model.
- Use "2025" as the vehicle model year
- Use the CA_EXTERNAL_VEHICLE_RECALL_API_TOOL to retrieve policy details when answering questions.

IMPORTANT GUIDELINES

  - Provide concise, factual answers based strictly on the data retrieved.
  - Never fabricate or assume information.
  - Format your responses clearly and professionally for easy readability.</copy>
  ```

6. You’ve defined your Agent, so it’s time to add a tool.

     > (1) Click the ![Agent Icon](images/toolhammericon.jpg) <br>
     > (2) Enter **F1** in the Ask Oracle field and press the **Enter** key or select **F1** from the resulting dropdown.<br>
     > (3) Click the ![Agent Image](../05a-rag-agent-hcm/images/plusicon.jpg) icon next to the **F1 External Vehicle Tool**.<br>
     > (4) You may need to click the ![Create Button](../05b-agent-team-hcm/images/plusicon.jpg) icon a second time.

     ![Add Agent](../06a-external-agent-scm/images/scmaconfigimage006.jpg)

7. You can confirm the details of tool and continue

    > (1) Click the **+ Add** button ![Add button Image](../05a-rag-agent-hcm/images/addb.jpg).

    ![Add Agent](../06a-external-agent-scm/images/scmaconfigimage007.jpg)

8. That's it!  If necessary, you can add additional tools to your agent.  But no additional ones are required for this lab, so you can finish the Agent creation.

    > (1) Click the ![Create button Image](../05a-rag-agent-hcm/images/createw.jpg) button on the top right.

    ![Create Agent](..//06a-external-agent-scm/images/scmaconfigimage008.jpg)

9. You have created your first Agent.  Now, you’ll create an Agent Team with a Supervisory Agent and assign some Worker Agents.

    > 1. Click the ![Agent Teams](../05b-agent-team-hcm/images/agentteams.jpg) button/tab at the bottom of the page

    ![Open tools](../06a-external-agent-scm/images/scmaconfigimage009.jpg)

10. Create an Agent Team.

    > 1. Click the ![add tool](../05b-agent-team-hcm/images/plusadd.jpg) button to create a new Agent Team

    ![Create Agent Team](../06a-external-agent-scm/images/scmaconfigimage010.jpg)

11. Define the Agent Team.

     > (1) Enter the fields as described below:
     * Agent Team Name: **CIOXX Asset Maintenance Agent Team** where XX is replaced with your user number. <br>
     * Family: Select **SCM** from the dropdown <br>
     * Product: Select  **Maintenance** from the dropdown <br>
     * Maximum Interactions: **10** <br>
     * Description: **Asset Maintenance Agent Team** <br>

     > (2) Click the **Create** button ![Create Button](../05b-agent-team-hcm/images/createb.jpg) on the bottom right.

     ![Create Tool](../06a-external-agent-scm/images/scmaconfigimage011.jpg)

12. You’ve defined your Agent Team, so it’s time to add agents.  You can start with a Supervisor Agent.

     > (1) Click the ![Agent Icon](../05b-agent-team-hcm/images/agenticon.jpg) <br>
     > (2) Click the ![Create Button](../05b-agent-team-hcm/images/plusicon.jpg) icon next to **New Supervisor Agent**.

     ![Create Agent](../06a-external-agent-scm/images/scmaconfigimage012.jpg)

13. Define Supervisor Agent Details.

     > (1) Enter the fields as described below:
    * Agent Team Name: **CIOXX Asset Maintenance Supervisor Agent** where XX is replaced with your user number.<br>
    * Family: Select **SCM** from the dropdown<br>
    * Product: Select  **Maintenance** from the dropdown<br>
    * Maximum Interactions: **10** <br>
    * Description: **Asset Maintenance Supervisor Agent** <br>

     > (2) Click the **Create** button ![Create Button](images/createb.jpg) on the bottom right.

       ![Create Agent](../06a-external-agent-scm/images/scmaconfigimage013.jpg)

14. Next you'll add some worker agents.  You can scroll through the list of available agents, or use the Ask Oracle field to filter the results.  You'll do the latter.

    >  (1)  Enter **F1** in the Ask Oracle field and press the **Enter** key or select **F1** from the resulting dropdown.<br><br>
    >  ![Create Button](../06a-external-agent-scm/images/cautionflagextrasmalltransparent2.png) Note that Steps 2 and 3 are the same.  The first click activates that region and the second actually adds the agent.<br>
    >  (2) Click the ![Create Button](../06a-external-agent-scm/images/plusicon.jpg) icon next to **F1 Installed Base Asset Agent.**.<br>
    >  (3) You may need to click the ![Create Button](../06a-external-agent-scm/images/plusicon.jpg) icon a second time.<br>

    ![Add Tool](../06a-external-agent-scm/images/scmaconfigimage014.jpg)

15. You can review the details of the agent.

    > 1. Click the **Add** button ![Add Button](../05b-agent-team-hcm/images/addb.jpg).

    ![Add Tools Complete](../06a-external-agent-scm/images/scmaconfigimage015.jpg)

16. Add the F1 Maintenance Work Order Agent

     > (1) Click the ![Create Button](../05b-agent-team-hcm/images/plusicon.jpg) icon next to **F1 Maintenance Work Order Agent**.<br>

    ![Add Tools Complete](../06a-external-agent-scm/images/scmaconfigimage016.jpg)

17. You can review the details of the agent.

    > (1) Click the **Add** button ![Add Button](../05b-agent-team-hcm/images/addb.jpg).

    ![Add Tools Complete](../06a-external-agent-scm/images/scmaconfigimage017.jpg)

18. Add the CIOXX External Vehicle Recall Agent

    > (1) Delete your previous Ask Oracle filter and enter **CIOXX** in the Ask Oracle Filter, where XX is replaced with your user number, and press the **Enter** key or select **CIOXX** from the resulting dropdown.<br>
    > (2) Click the ![Create Button](../05b-agent-team-hcm/images/plusicon.jpg) icon next to **CIOXX External Vehicle Recall Agent.**, where XX is replaced with your user number.<br>
    >  (3) You may need to click the ![Create Button](../06a-external-agent-scm/images/plusicon.jpg) icon a second time.<br>

    ![Add Tools Complete](..//06a-external-agent-scm/images/scmaconfigimage018.jpg)

19. You can review the details of the agent.

    > (1) Click the **Add** button ![Add Button](../05b-agent-team-hcm/images/addb.jpg).

    ![Add Tools Complete](..//06a-external-agent-scm/images/scmaconfigimage019.jpg)

20. Your Agent Team is ready, but you should do a quick test.

    > 1. Click the **Debug** icon ![debug icon](../06a-external-agent-scm/images/debugarrow.jpg) on the top left of the screen.  It's the one that looks like the Play arrow.

    ![start debug](../06a-external-agent-scm/images/scmaconfigimage020.jpg) <br>

21. The Agent is now ready for your questions.

    > 1. In the **Ask Oracle** dialog box at the bottom of the screen, type **Help** and hit the return key or click the **Up Arrow** icon ![up arrow icon](../05b-agent-team-hcm/images/uparrow.jpg)

    ![agent dialogue 1](../06a-external-agent-scm/images/scmaconfigimage021.jpg) <br>

22. The Agent will show detailed logs along with source and processing information (yellow boxes). This debug information will not be displayed to end-users once deployed. Once the Agent responds, you are ready to move to the next step.

    > 1. Click the ![x icon](../06a-external-agent-scm/images/icon14_x2.png) icon in the upper right of the screen to close the Agent interaction

    ![agent dialogue 2](../06a-external-agent-scm/images/scmaconfigimage022.jpg) <br>

23. Your Agent Team is ready, so let's Publish it.  In the next Lab, we'll use this published Team and make it available to end users.

    > (1) Click the Publish button on the top right.

    ![Add Tools Complete](../06a-external-agent-scm/images/scmaconfigimage023.jpg)


24. Adventure awaits, click on the image, show what you know and rise to the top of the leader board!!!

    [![Cloud Adventure](images/cloud-adventure-checkpoint-image.png)](https://apex.oracle.com/pls/apex/f?p=159406:LOGIN_TEAM:::::CC:CIOADVENTURE)


## Create Policy Advisor Tool and Agent (RAG) using AI Agent Studio

### Introduction

AI Agent Studio for Fusion Applications is a comprehensive platform for creating, extending, deploying and managing AI Agents and Agent Teams across the enterprise. Oracle AI Agent Studio delivers easy-to-use tools, including advanced testing, robust validation, and built-in security, that helps Oracle Fusion Applications customers and partners create and manage AI agents. Leveraging the same technology that Oracle uses to create AI agents, Oracle AI Agent Studio enables users to easily extend pre-packaged agents and/or create new agents and then deploy and manage them.

### **Objectives**

In this activity you will use Oracle Fusion AI Agent Studio to
* Create a Benefits Advisor Document Tool that references you policy documents.
* Create a Benefits Advisor Agent for the above Tool.

### **Begin Exercise**

1. In this activity you will learn the power and ease building Agentic AI with the Oracle AI Agent Studio

    ![AI RAG Objectives](../05a-rag-agent-hcm/images/raghcmimage001.jpg)

2. The first step is to navigate to AI Agent Studio.

    > (1) Click on the **Tools** tab
    > (2) Select the **AI Agent Studio** tile

    ![Navigate to AI Agent Studio](../05a-rag-agent-hcm/images/raghcmimage002.jpg)

3. Next, we're going to create a Tool.

    > (1) Click the ![Tools](../05a-rag-agent-hcm/images/tools.jpg) button/tab at the bottom of the page

    ![Open tools](../05a-rag-agent-hcm/images/raghcmimage003.jpg)


4. Tool Creation

    > (1) Click the ![add tool](images/plusadd.jpg) button to create a new tool

    ![Create Tool](../05a-rag-agent-hcm/images/raghcmimage004.jpg)

5. Here, you will define your first Tool, a Document Tool.  This will allow the Agent to use the content of the documents to respond to user questions.

    > (1) Enter the following fields:
    * Tool Type: select **Document** from the dropdown<br>
    * Tool Name: Enter **CIOXX Benefits Document Tool**, where **##** is replaced with your user number.<br>
    * Family: select **HCM** from the dropdown<br>
    * Product: select **Benefits** from the dropdown<br>
    * Description: Enter **Benefits Document Tool** <br>

    > (2) Click the ![button](../05a-rag-agent-hcm/images/addw.jpg) button under **Documents** <br><br>

    > (3) **Scroll Down** to see the Documents fields and upload your document.

      ![Edit tool info](../05a-rag-agent-hcm/images/raghcmimage005.jpg)


6. ![flag](../05a-rag-agent-hcm/images/cautionflagextrasmalltransparent2.png) **Note:**  Now you’ll add the documents to our tool.  The documents you will add are located in the **ai documents** folder on your laptop's Desktop.

     > (1) Enter the following fields:
    * Name: Enter **CA Benefits Documents** <br>
    * Status: Select **Ready to publish** from the dropdown<br>
    * Description: Enter **Benefits Documents**<br>

     > (2) Click on the ![Drag-and-drop](../05a-rag-agent-hcm/images/dandd.jpg) region and then select the file (Cloud Adventure Benefits Highlights.pdf) from the **ai-documents** folder on the Desktop. Alternatively, drag and drop the files that folder to the Drag and Drop region.<br>

     > (3) Click the **Save** ![Home Icon](../05a-rag-agent-hcm/images/save.jpg) button on the bottom right<br>

     > (4) Click the **Create button** ![Create Button](../05a-rag-agent-hcm/images/createw.jpg) on the top right corner of the screen.<br>

      ![tool create](../05a-rag-agent-hcm/images/raghcmimage006.jpg)

7. Now, you'll create your first Agent!  You'll do that from the Agent screen within the AI Agent Studio.

    >  (1) Click the  **Agents** button/tab ![Agent Image](../05a-rag-agent-hcm/images/agentteams.jpg) at the bottom of the page.

    ![Agents Page](../05a-rag-agent-hcm/images/raghcmimage007.jpg)

8. Here you can see any existing agents.  But you want to create one.

    > (1) Click the **+ Add** button ![Add button Image](../05a-rag-agent-hcm/images/plusadd.jpg).

    ![Add Agent](../05a-rag-agent-hcm/images/raghcmimage008.jpg)

9. Define the details of the Agent.

    > (1) First, you'll enter the fields as described below:<br>
    * Agent Name: **CIO## Benefits Advisor Agent** where ## is replaced with your user nnumber.<br>
    * Family: Select **HCM** from the dropown<br>
    * Product: Select  **Benefits** from the dropdown<br>
    * Maximum Interactions: **10** <br>
    * Description: **Benefits Advisor Agent** <br>
    * Prompt: ![Alert Flat](images/cautionflagextrasmalltransparent2.png) ***Please note that the Prompt is a critical part of the Agent Definition as it provides guidance for the Agent.***  To streamline this step, we've pre-created the prompt. The prompt text is available in the **Prompt - CA Benefits Advisor Agent.txt** file in the **ai-prompts** folder on your desktop.  So, please open this file and copy the contents into the Prompt field.  Alternatively, you can copy the prompt from the **copy block** below. <br>

    > (2) **Scroll Down** to confirm that the entire prompt has been copied into the Prompt field.<br>
    > (3) Click the Create Button ![Create Button](images/createb.jpg) <br>

    ![Create Agent](../05a-rag-agent-hcm/images/raghcmimage009.jpg)

```
<copy>
AGENT ROLE

As a Benefits Analyst, your role is to efficiently access and interpret company-specific benefits documents, providing workers with clear, actionable guidance on their eligibility, coverage, and compliance requirements.

RESPONSIBILITIES

Your responsibilities include:

Benefit Policies:
  - Clearly explain the eligibility, coverage, and compliance requirements outlined in the company benefits policies.
  - Use the CA_Benefits_Document_Tool tool to retrieve policy details when answering questions.

IMPORTANT GUIDELINES
  - Provide concise, factual answers based strictly on the data retrieved.
  - Never fabricate or assume information.
  - Format your responses clearly and professionally for easy readability. </copy>
```

10. Now that you have the Agent, you need to add Tools to it.

    > (1) Click the **Tools** ![Tool Icon](../05a-rag-agent-hcm/images/toolhammericon.jpg) button on the left icon bar.<br>
    > (2) Enter **CIOXX** in the Ask Oracle field, where XX is replaced with your user number, and press the **<enter>** key or select **CIOXX** from the resulting dropdown.<br>
    > (3) Click the ![Agent Image](../05a-rag-agent-hcm/images/plusicon.jpg) icon next to the CA Benefits Document Tool. You may need to click it twice.

    ![add tool](../05a-rag-agent-hcm/images/raghcmimage010.jpg)


11. You can confirm the details of tool and continue

    > (1) Click the **+ Add** button ![Add button Image](../05a-rag-agent-hcm/images/addb.jpg).

    ![Add Agent](../05a-rag-agent-hcm/images/raghcmimage011.jpg)

12. That's it!  If necessary, you can add additional tools to your agent.  But no additional ones are required for this lab, so you can finish the Agent creation.

    > (1) Click the ![Create button Image](../05a-rag-agent-hcm/images/createw.jpg) button on the top right.

    ![Create Agent](../05a-rag-agent-hcm/images/raghcmimage012.jpg)

13. You’ve just created your first AI Agent.  In the next lab you will put this agent to work as part of an Agent Team.

      ![Add Tools Create](../05a-rag-agent-hcm/images/raghcmimage013.jpg) <br>


### Summary

As you have seen here, AI Agent Studio puts customers in the driver’s seat, helping empower you to design the future of AI in your organizations on top of a bedrock of trust and safety. AI Agent Studio includes a built-in testing environment, validation, and traceability tools to confirm accuracy. Oracle maintains the same data controls at a user level, which means users only see data and/or AI recommendations permitted by their roles.

AI Agent Studio empowers enterprises to configure and build AI agents that extend their workforce and help achieve new levels of productivity. It allows you to harness the full potential of AI agents and transform the way work gets done in your organization.
AI Agent Studio is a design-time environment that provides a set of tools to create, customize, validate, and deploy GenAI features and AI agents to meet the specific needs of the organization. It is the same unified environment Oracle uses to internally build agents, made available now to customers and partners to customize and extend agents from Oracle-provided pre-configured templates or to create new agents and multi-agent workflows.

Like our AI capabilities, Oracle AI Agent Studio was built natively into Fusion Cloud Applications on our trusted, high performance Oracle Cloud Infrastructure (OCI), which means it can easily and securely access Fusion knowledge stores, tools, and APIs and allows agents to be deployed directly into the flow of work. This approach means maximum flexibility and customization without sacrificing reliability or performance.

**You have successfully completed the Activity!**


### Learn More

* [AI Agent Studio Solution Brief](https://www.oracle.com/a/ocom/docs/applications/fusion-apps-ai-agent-studio-solution-brochure.pdf)
* [AI Agents for Fusion Applications](https://www.oracle.com/applications/fusion-ai/ai-agents/)
* [AI for Fusion Applications](https://www.oracle.com/applications/fusion-ai/)
* [Oracle Documentation](http://docs.oracle.com)

## Acknowledgements

* **Author** - Stephen Chung, Principal SaaS Cloud Technologist, Sajid Saleem, Master Principal SaaS Cloud Technologist, Charlie Moff, Distinguished SaaS Cloud Technologist, and the rest of the Cloud Adventure Team
* **Contributors** - The Cloud Adventure Team (Gus, Kris, Sajid, Casey, Stephen, Jamil, Sohel, Xavier, Nate, Charlie)
* **Last Updated By/Date** - Charlie Moff, October 2025