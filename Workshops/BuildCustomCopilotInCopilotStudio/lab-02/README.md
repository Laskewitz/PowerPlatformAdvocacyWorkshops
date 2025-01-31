# Lab 02 - Build a custom copilot with Microsoft Copilot Studio

Copilot Studio empowers teams to quickly and easily create powerful copilots using a guided, no-code graphical experience without needing data scientists or developers.

There are two ways to create a custom copilot
* Start with a template
* Describe your copilot to create it using natural language

Each method allows you to connect your data and knowledge sources to enable your custom copilot to access information and complete tasks.

In this lab, you will learn how to do the following:
* [2.1 Available templates to create a custom copilot](#21-available-templates-to-create-a-custom-copilot)
* [2.2 Use natural language to create a custom copilot](#22-use-natural-language-to-create-a-custom-copilot)
* [2.3 Adding an internal knowledge source using a SharePoint site](#223-adding-an-internal-source-using-a-sharepoint-site)

## 2.1 Available templates to create a custom Copilot

In this part of the lab, you will learn of the several templates available to quickly get started in creating your own custom copilot.
In the Home landing page of Microsoft Copilot Studio, you’ll see three areas
* Describe your copilot to create it – use natural language to build your copilot
* Templates – these are a preview feature and helps you get started in creating your copilot
* Learning resources – multiple resources for further learning

    ![Copilot Studio Home](assets/2.1_01_CopilotStudioHome.jpg)

1. To start with a template, select the **Weather template**.

    ![Select Weather template](assets/2.1_02_SelectTemplate.jpg)
    
1.	You’ll see that the template already has some details filled in already

    - **Name** – the name of the copilot.
    - **Description** – describes the purpose of the Weather copilot and how it can help.
    - **Instructions** – the primary purpose of the Weather Copilot and how it should act.
    - **Connect your data** – authenticate to a Power Platform connector to enable Copilot to complete tasks and access information. In this template the MSN Weather connector is used.
    - **Language** – the primary language of the copilot.
    - **Knowledge** – add enterprise data from Power Platform, Dynamics 365 data, and external systems to enable Copilot to provide relevant information and insights for end users.
    
    ![Weather copilot template](assets/2.1_03_WeatherCopilotTemplate.jpg)

1.	Scroll down to **Connect your data**, select the ellipsis (. . .) and select **Edit**.

    ![Connect data source](assets/2.1_04_ConnectDataSource.jpg)

1.	The Connection setup window will appear and a green tick will appear to let you know that the MSN Weather connector is now authenticated using your credentials. Select **Confirm**.

    ![Confirm connection](assets/2.1_05_ConfirmConnectionSetup.jpg)

1.	The status of the MSN Weather connector will now display as _Connected_ with a green tick.

    ![Connected](assets/2.1_06_Connected.jpg)

1.	Next, take a look at the Advanced Settings of the Copilot by selecting the ellipsis **(. . .)** and select **Edit advanced settings**.

    ![Edit advanced settings](assets/2.1_07_AdvancedSettings.jpg)

1.	This is where you can define the following settings,

    - **Solution** – select the solution to create your copilot in. This allows you to deploy the copilot to a target environment by exporting the solution. By default Common Data Services Default Solution will be selected.
    - **Schema Name** – by default this will be the name of your copilot. This is the unique name which can be used to embed or connect your copilot to other applications or services.
    - **Classic copilot** – there’s also an option to create a classic copilot which is not covered in this lab.
    
    ![Advanced settings](assets/2.1_08_AdvancedSettings.jpg)

1.  Select Cancel to exit Advanced Settings.

1.  Select Create to create your Weather Copilot.

    ![Create Weather copilot](assets/2.1_09_CreateWeatherCopilot.jpg)

1.  Copilot Studio will be in the process of setting up the Weather Copilot and when complete, the Weather Copilot will be displayed in the center of Copilot Studio, followed by the testing pane on the right hand side.

    ![Weather copilot created](assets/2.1_10_WeatherCopilotCreated.jpg)

1.  Scroll down and you’ll see that the Topics and Actions are already configured from the template, enabling you to quickly create a Weather Copilot.

    ![Copilot Topics and Actions](assets/2.1_11_TopicsActions.jpg)

1.  You can now test the Weather copilot using the right hand side pane. Select the _What can I ask?_ question to see a list of suggested questions to ask the Weather copilot.

    ![Suggested questions](assets/2.1_12_TestCopilot.jpg)
    
1.  A list of questions will appear. Select _What is the current weather?_

    ![Weather copilot created](assets/2.1_13_SelectQuestion.jpg)

1.  Enter a city for example,

    ```
    Seattle
    ```

    ![Eneter city](assets/2.1_14_EnterCity.jpg)

1.  Copilot will respond with a summary of the current weather for the city entered.

    ![Weather copilot response](assets/2.1_15_Response.jpg)

🎓 You’ve created a custom copilot using a template. Let’s next learn how to use natural language to build a custom copilot from scratch.

## 2.2 Use natural language to create a custom Copilot

You can now use a conversation first approach to create a custom Copilot where natural language is used to describe the custom Copilot that you’d like to create.

1.  Select Home on the left hand side menu and in the Describe your copilot to create it field, describe in natural language what your copilot should do. For example,

    ```
    I want you to be a question and answering copilot that can answer common questions from users using the content of a website and a SharePoint site
    ```

    ![City](assets/2.2_01_DescribeToCreate.jpg)

1. Microsoft Copilot Studio then proceeds to use AI to ask you several questions to define the Copilot you want to build. For example the first question may be based on how your copilot will assist users. You can either select _What should I say?_ which will provide guidance or you can enter and describe what you’d like your copilot to do. The following is an example,

    ```
    help answer common product and support questions using the content of a website, and help answer HR questions from a SharePoint site
    ```

    ![City](assets/2.2_02_DescribeTypeOfAssistance.jpg)

1. The second question may be based on the tone of the Copilot. Again, a list of suggestions can be provided by selecting _What should I say?_

    ![Further guidance](assets/2.2_03_Further%20guidance.jpg)

1.  A list of suggestions will appear for guidance. Enter a tone, for example,

    ```
    Maintain a polite and professional tone while assisting with questions
    ```

    ![Tone](assets/2.2_04_Tone.jpg)

1.  Next question will be based on what external knowledge source the Copilot can refer to answer questions asked by users. A guide can be provided by selecting _Any tips?_

    ![Further guidance](assets/2.2_05_Tips.jpg)

1.  Guidance will appear on adding websites for your Copilot. Next enter a public facing website URL address. For example, enter the following,

    ```
    www.microsoft.com
    ```

    ![Further guidance](assets/2.2_06_TipsForWebsites.jpg)

1.  The final question will be based on what topics or tasks the Copilot should not help with. For example, enter the following,

    ```
    If asked religion or politics, politely decline to discuss and offer assistance with other inquiries.
    ```

    ![Topics to dismiss](assets/2.2_07_TopicsTasksToDismiss.jpg)

1.  There are no further questions to answer but you can enter more details to make adjustments. Notice how on the right hand side pane that all your requirements are listed for you based on the natural language used to answer the questions asked. Select **I’m done**.

    ![Done building copilot](assets/2.2_08_Done.jpg)

1.  Notice how your Copilot has automatically been given a name based on the natural language used earlier to describe what your Copilot will help and assist with.

    Before creating you Copilot, there’s also the options of

    - Skip to configure – where you exit from this conversation first approach and create a custom copilot by not answering questions
    - Select the ellipsis for additional options  (. . .) 
        - **Restart copilot creation** – clears all answers in response to the question asked and starts at the beginning
        - **Edit advanced settings** – update the solution and schema name as previously covered in 2.1 Available templates to create a custom Copilot
        - **Cancel copilot creation** – cancels creating the copilot

    ![Additional settings](assets/2.2_09_AdditionalSettings.jpg)

1.  Select **Create** to create your custom Copilot.

    ![Create copilot](assets/2.2_10_CreateCopilot.jpg)

1. Copilot Studio will be in the process of setting up your custom Copilot.

    ![Create copilot](assets/2.2_11_SettingUp.jpg)

1.  When complete, the custom Copilot will be displayed in the center of Copilot Studio, followed by the testing pane on the right hand side.

    ![Copilot created](assets/2.2_12_CustomCopilotCreated.jpg)

1.  If you scroll down, you’ll see the description, the instructions and the knowledge source with the public website already configured. You can now test your copilot by entering the following question,

    ```
    What is Copilot Studio?
    ```
    ![Ask a question](assets/2.2_13_TestCopilot.jpg)

1. Copilot uses the external link previously provided, www.microsoft.com, to return an answer in plain natural language. Notice that there are references with a hyperlink to where the information is sourced from so that you can validate it. You can also provide feedback by selecting the thumbs down or thumbs up icons.

    Try asking another question,
    
    ```
    What is the latest Xbox model?
    ```

    Copilot will respond again using information from the external link, www.microsoft.com. This is useful because it allows you to build copilots using existing information rather than creating specific topics based on requests that might be made by users.

    ![Create copilot](assets/2.2_14_TestCopilot.jpg)

🎓 You've created a copilot using natural language and can answer questions based on the website provided. Let's learn how to add an internal resource.

## 2.3 Adding an internal source using a SharePoint site

Knowledge in Microsoft Copilot Studio allows you to add enterprise data from Power Platform, Dynamics 365 data, and external systems, so your copilots provide relevant information and insights for your end users. In addition, knowledge can be incorporated with [generative answers](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-boost-conversations) in copilots. Published copilots that contain knowledge use the configured knowledge sources to ground the published copilot.

Next, you'll learn how to add an internal data source, SharePoint, for generative answers in your copilot.

1. In the Overview tab, select **+Add Knowledge**.

    ![Add knowledge](assets/2.3_01_AddKnowledge.jpg)

1. A list of knowledge sources will appear. Select SharePoint and OneDrive.

    ![Add SharePoint internal source](assets/2.3_02_AddDataSource.jpg)

1.  Paste the SharePoint site URL from the SharePoint site you created earlier in the sources field and select Add.

    ![SharePoint URL](assets/2.3_03_DataSourceURL.jpg)

> [!TIP]  
> To recopy the SharePoint site URL, head to the [⏪ previous lab](../lab-01/README.md/#relaunch-sharepoint-site) to copy the SharePoint site URL and return to this lab to proceed.

4.  The SharePoint site is added as a Knowledge Source. Please note that the SharePoint Site will only be available to authenticated end-users, [learn more](https://learn.microsoft.com/en-us/microsoft-copilot-studio/nlu-generative-answers-sharepoint-onedrive). Select Add.

    ![Add data source](assets/2.3_04_AddDataSource.jpg)

1.  The SharePoint site has now been added as a knowledge source for the Copilot.

    ![Data source URL](assets/2.3_05_KnowledgeSources.jpg)

1.  Before we can test, the generative AI feature needs to be enabled. Select Settings on the top right of the Copilot.

    ![Settings](assets/2.3_06_Settings.jpg)

1.  Select Generative AI in the Settings menu on the left hand side pane, followed by selecting the Generative (preview) setting and select Save.

    ![Settings](assets/2.3_07_GenerativeSetting.jpg)
    
1.  Select the X icon on the right hand side to return to the Copilot.  We can now test copilot to confirm SharePoint is now a data source for generative answers. Select the refresh icon and enter the question,

    ```
    What happens if I'm sick and cannot work?
    ```

1.  This time Copilot uses the internal link [https://m365x73059307.sharepoint.com/](https://m365x73059307.sharepoint.com) to return the answer it found in a document in plain natural language. References are provided once again with a hyperlink to where the information is sourced from so that you can validate it.

    ![Time off question](assets/2.3_08_Question1.jpg)

1.  Try entering another question, 

    ```
    What holidays do Contoso employees have off?
    ```

![Holidays question](assets/2.3_09_Question2.jpg)

1.  You’ll see another response from Copilot that uses the SharePoint data source to answer the question entered in plain natural language.

    ![Holidays for Contoso employees](assets/2.3_10_AnswerToQuestion2.jpg)

## Next lab

Congratulations! 👏🏻  You've created a copilot with external and internal data sources for Generative Answers. 

This is the end of Lab 02 - Build a custom copilot with Microsoft Copilot Studio, select the link below to move to the next lab.

[⏭️ Move to Lab 03 - Create an AI Plugin using a Power Platform component for Generative Actions](../lab-03/README.md)