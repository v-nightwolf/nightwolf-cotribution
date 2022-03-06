## Microsoft Azure Administrator

   QUESTION 1:

        You have an Azure Active Directory (Azure AD) tenant named Adatum and an Azure Subscription named 
        Subscription1. Adatum contains a group named Developers. Subscription1 contains a resource group named Dev.
        You need to provide the Developers group with the ability to create Azure logic apps in the Dev resource
        group.

        Solution: On Dev, you assign the Contributor role to the Developers group. Does this meet the goal?
        A. Yes
        B. No

        Correct Answer: A 

        Explanation:
        The Contributor role can manage all resources (and add resources) in a Resource Group.

   QUESTION 2

        You have an Azure Active Directory (Azure AD) tenant named Adatum and an Azure Subscription named 
        Subscription1. Adatum contains a group named Developers. Subscription1 contains a resource group named Dev.
        You need to provide the Developers group with the ability to create Azure logic apps in the Dev resource 
        group.

        Solution: On Subscription1, you assign the Logic App Operator role to the Developers group. Does this meet the goal?
        A. Yes
        B. No

        Correct Answer: B

        Explanation:
        You would need the Logic App Contributor role. References:
        https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app

   QUESTION 3

        You have an Azure Active Directory (Azure AD) tenant named Adatum and an Azure Subscription named
        Subscription1. Adatum contains a group named Developers. Subscription1 contains a resource group named Dev.
        You need to provide the Developers group with the ability to create Azure logic apps in the Dev resource group.

        Solution: On Dev, you assign the Logic App Contributor role to the Developers group. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: A

        Explanation:
        The Logic App Contributor role lets you manage logic app, but not access to them. It provides access to view,
        edit, and update a logic app.

        References:
        https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app

   QUESTION 4

        You have an Azure subscription named Subscription1 that contains an Azure Log Analytics workspace named
        Workspace1.
        You need to view the error events from a table named Event. Which query should you run in Workspace1?

        A. Get-Event Event | where ($_.EventType –eq "error")
        B. Get-Event Event | where ($_.EventType == "error")
        C. search in (Event) * | where EventType –eq "error"
        D. search in (Event) "error"
        E. select *from Event where EventType == "error"
        F. Event | where EventType is "error"

        Correct Answer: D

        Explanation:
        To search a term in a specific table, add in (table-name) just after the search operator

        References:
        https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/search-queries https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-portal

        QUESTION 5

        You have an Azure subscription named Subscription1. Subscription1 contains the resource groups in the following table.
        RG1 has a web app named WebApp1. WebApp1 is located in West Europe. You move WebApp1 to RG2.
        What is the effect of the move?
        A. The App Service plan for WebApp1 moves to North Europe. Policy2 applies to WebApp1.
        B. The App Service plan for WebApp1 remains in West Europe. Policy2 applies to WebApp1.
        C. The App Service plan for WebApp1 moves to North Europe. Policy1 applies to WebApp1.
        D. The App Service plan for WebApp1 remains in West Europe. Policy1 applies to WebApp1.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can move an app to another App Service plan, as long as the source plan and the target plan are in the same resource group and geographical region.
        The region in which your app runs is the region of the App Service plan it's in. However, you cannot change an App Service plan's region.
        References:
        https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage
        QUESTION 6
        You have an Azure subscription that contains a resource group named RG1. RG1 contains 100 virtual machines.
        Your company has three cost centers named Manufacturing, Sales, and Finance. You need to associate each virtual machine to a specific cost center.
        What should you do?
        A. Configure locks for the virtual machine.
        B. Add an extension to the virtual machines.
        C. Assign tags to the virtual machines.
        D. Modify the inventory settings of the virtual machine.
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        References:
        https://docs.microsoft.com/en-us/azure/billing/billing-getting-started https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-using-tags
        QUESTION 7
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1 contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1.
        Solution: From the Subscriptions blade, you select the subscription, and then click Programmatic deployment.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        QUESTION 8
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1 contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1.
        Solution: From the Subscriptions blade, you select the subscription, and then click Resource providers. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        QUESTION 9
        Note: This question is part of a series of questions that present the same scenario. Each question
        in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1 contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1. Solution: From the RG1 blade, you click Automation script.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        QUESTION 10
        HOTSPOT
        You have an Azure subscription.
        You plan to use Azure Resource Manager templates to deploy 50 Azure virtual machines that will be part of the same availability set.
        You need to ensure that as many virtual machines as possible are available if the fabric fails or during servicing.
        How should you configure the template? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Use two fault domains.
        2 or 3 is max value, depending on which region you are in.
        Use 20 for platformUpdateDomainCount
        Increasing the update domain (platformUpdateDomainCount) helps with capacity and availability planning when the platform reboots nodes. A higher number for the pool (20 is max) means that fewer of their nodes in any given availability set would be rebooted at once.
        References:
        https://www.itprotoday.com/microsoft-azure/check-if-azure-region-supports-2-or-3-fault-domains-managed- disks
        https://github.com/Azure/acs-engine/issues/1030
        QUESTION 11
        HOTSPOT
        You have an Azure subscription named Subscription1 that has a subscription ID of c276fc76-9cd4-44c9- 99a7-4fd71546436e.
        You need to create a custom RBAC role named CR1 that meets the following requirements: Can be assigned only to the resource groups in Subscription1
        Prevents the management of the access permissions for the resource groups
        Allows the viewing, creating, modifying, and deleting of resource within the resource groups
        What should you specify in the assignable scopes and the permission elements of the definition of CR1? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        References:
        https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles
        https://docs.microsoft.com/en-us/azure/role-based-access-control/resource-provider- operations#microsoftresources
        QUESTION 12
        HOTSPOT
        You have an Azure Active Directory (Azure AD) tenant that contains three global administrators named Admin1, Admin2, and Admin3.
        The tenant is associated to an Azure subscription. Access control for the subscription is configured as shown in the Access control exhibit. (Click the Exhibit tab.)
        You sign in to the Azure portal as Admin1 and configure the tenant as shown in the Tenant exhibit. (Click the Exhibit tab.)
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        QUESTION 13
        You have an Azure policy as shown in the following exhibit.
        What is the effect of the policy?
        A. You are prevented from creating Azure SQL Servers in ContosoRG1 only.
        B. You can create Azure SQL servers in ContosoRG1 only.
        C. You can create Azure SQL servers in any resource group within Subscription1.
        D. You are prevented from creating Azure SQL servers anywhere in Subscription1.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You are prevented from creating Azure SQL servers anywhere in Subscription 1 with the exception of
        ContosoRG1
        QUESTION 14
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure Active Directory (Azure AD) tenant named Adatum and an Azure Subscription named Subscription1. Adatum contains a group named Developers. Subscription1 contains a resource group named Dev.
        You need to provide the Developers group with the ability to create Azure logic apps in the Dev resource group.
        Solution: On Subscription1, you assign the DevTest Labs User role to the Developers group. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        DevTest Labs User role only lets you connect, start, restart, and shutdown virtual machines in your Azure DevTest Labs.
        The Logic App Contributor role lets you manage logic app, but not access to them. It provides access to view, edit, and update a logic app.
        References: https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app
        QUESTION 15
        You have an Azure Active Directory (Azure AD) tenant that contains 5,000 user accounts. You create a new user account named AdminUser1.
        You need to assign the User administrator administrative role to AdminUser1. What should you do from the user account properties?
        A. From the Directory role blade, modify the directory role.
        B. From the Licenses blade, assign a new license.
        C. From the Groups blade, invite the user account to a new group.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Assign a role to a user
        1. Sign in to the Azure portal with an account that's a global admin or privileged role admin for the directory.
        2. Select Azure Active Directory, select Users, and then select a specific user from the list.
        3. For the selected user, select Directory role, select Add role, and then pick the appropriate admin roles from the Directory roles list, such as Conditional access administrator.
        4. Press Select to save.
        References: https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-users-assign-role- azure-portal
        QUESTION 16
        HOTSPOT
        You have an Azure subscription named Subscription1.
        You plan to deploy an Ubuntu Server virtual machine named VM1 to Subscription1.
        You need to perform a custom deployment of the virtual machine. A specific trusted root certification authority (CA) must be added during the deployment.
        What should you do? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Cloud-init.txt
        Cloud-init.txt is used to customize a Linux VM on first boot up. It can be used to install packages and write files, or to configure users and security. No additional steps or agents are required to apply your configuration.
        Box 2: The az vm create command
        Once Cloud-init.txt has been created, you can deploy the VM with az vm create cmdlet, sing the --custom- data parameter to provide the full path to the cloud-init.txt file.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-automate-vm-deployment
        QUESTION 17
        You have an Azure subscription named Subscription1. In Subscription1, you create an alert rule named Alert1.
        The Alert1 action group is configured as shown in the following exhibit.
        Alert1 alert criteria is triggered every minute.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: 60
        One alert per minute will trigger one email per minute.
        Box 2: 12
        No more than 1 SMS every 5 minutes can be send, which equals 12 per hour.
        Note: Rate limiting is a suspension of notifications that occurs when too many are sent to a particular phone number, email address or device. Rate limiting ensures that alerts are manageable and actionable.
        The rate limit thresholds are:
        SMS: No more than 1 SMS every 5 minutes. Voice: No more than 1 Voice call every 5 minutes. Email: No more than 100 emails in an hour.
        Other actions are not rate limited.
        References: https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/monitoring-and-diagnostics/monitoring- overview-alerts.md
        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message: "Licenses not assigned. License assignment failed for one user."
        You verify that the Azure subscription has the available licenses.
        Requirements Planned Changes
        Humongous Insurance plans to open a new office in Paris. The Paris office will contain 1,000 users who will
        be hired during the next 12 months. All the resources used by the Paris office users will be hosted in Azure.
        Planned Azure AD Infrastructure
        The on-premises Active Directory domain will be synchronized to Azure AD.
        All client computers in the Paris office will be joined to an Azure AD domain.
        Planned Azure Networking Infrastructure
        You plan to create the following networking resources in a resource group named All_Resources:
        Default Azure system routes that will be the only routes used to route traffic
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a separate resource group. The initial configuration of the web apps will be identical. The web administrators have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO) when accessing resources in Azure.
        QUESTION 1
        You need to resolve the licensing issue before you attempt to assign the license again. What should you do?
        A. From the Groups blade, invite the user accounts to a new group.
        B. From the Profile blade, modify the usage location.
        C. From the Directory role blade, modify the directory role.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        License cannot be assigned to a user without a usage location specified.
        Scenario: Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message: "Licenses not assigned. License agreement failed for one user."
        You verify that the Azure subscription has the available licenses.
        QUESTION 2
        You need to resolve the Active Directory issue. What should you do?
        A. Run the IdFix tool then use the Update actions.
        B. From Active Directory Domains and Trusts, modify the list of UPN suffixes.
        C. From Azure AD Connect, modify the outbound synchronization rule.
        D. From Active Directory Users and Computers, select the user accounts and then modify the UPN suffix value.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        IdFix is used to perform discovery and remediation of identity objects and their attributes in an on-premises Active Directory environment in preparation for migration to Azure Active Directory. IdFix is intended for the Active Directory administrators responsible for directory synchronization with Azure Active Directory.
        Scenario: Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some of the characters are unsupported in Azure AD.
        References: https://www.microsoft.com/en-us/download/details.aspx?id=36832
        QUESTION 3
        You need to define a custom domain name for Azure AD to support the planned infrastructure. Which domain name should you use?
        A. ad.humongousinsurance.com
        B. humingousinsurance.onmicrosoft.com
        C. humongousinsurance.com
        D. humongousinsurance.local
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Every Azure AD directory comes with an initial domain name in the form of domainname.onmicrosoft.com. The initial domain name cannot be changed or deleted, but you can add your corporate domain name to Azure AD as well. For example, your organization probably has other domain names used to do business and users who sign in using your corporate domain name. Adding custom domain names to Azure AD allows you to assign user names in the directory that are familiar to your users, such as ‘alice@contoso.com.’ instead of 'alice@domain name.onmicrosoft.com'.
        Scenario:
        Network Infrastructure: Each office has a local data center that contains all the servers for that office. Each office has a dedicated connection to the Internet.
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com
        Planned Azure AD Infrastructure: The on-premises Active Directory domain will be synchronized to Azure AD.
        References: https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-custom-domain
        Question Set 1
        QUESTION 1
        You plan to use the Azure Import/Export service to copy files to a storage account.
        Which two files should you create before you prepare the drives for the import job? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. a driveset CSV file
        B. a JSON configuration file
        C. a PowerShell PS1 file
        D. an XML manifest file
        E. a dataset CSV file
        Correct Answer: AE Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        A: Modify the driveset.csv file in the root folder where the tool resides.
        E: Modify the dataset.csv file in the root folder where the tool resides. Depending on whether you want to import a file or folder or both, add entries in the dataset.csv file
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-import-export-data-to-files
        QUESTION 2
        DRAG DROP
        You have an on-premises file server named Server1 that runs Windows Server 2016. You have an Azure subscription that contains an Azure file share.
        You deploy an Azure File Sync Storage Sync Service, and you create a sync group. You need to synchronize files from Server1 to Azure.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Install the Azure File Sync agent on Server1
        The Azure File Sync agent is a downloadable package that enables Windows Server to be synced with an Azure file share
        Step 2: Register Server1.
        Register Windows Server with Storage Sync Service
        Registering your Windows Server with a Storage Sync Service establishes a trust relationship between your server (or cluster) and the Storage Sync Service.
        Step 3: Add a server endpoint
        Create a sync group and a cloud endpoint.
        A sync group defines the sync topology for a set of files. Endpoints within a sync group are kept in sync with each other. A sync group must contain one cloud endpoint, which represents an Azure file share and one or more server endpoints. A server endpoint represents a path on registered server.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-deployment-guide
        QUESTION 3
        You create an Azure Storage account named contosostorage. You plan to create a file share named data.
        Users need to map a drive to the data file share from home computers that run Windows 10. Which outbound port should you open between the home computers and the data file share?
        A. 80
        B. 443
        C. 445
        D. 3389
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Ensure port 445 is open: The SMB protocol requires TCP port 445 to be open; connections will fail if port 445 is blocked.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows
        QUESTION 4
        HOTSPOT
        You have several Azure virtual machines on a virtual network named VNet1. You configure an Azure Storage account as shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: always
        Endpoint status is enabled.
        Box 2: Never
        After you configure firewall and virtual network settings for your storage account, select Allow trusted Microsoft services to access this storage account as an exception to enable Azure Backup service to access the network restricted storage account.
        Reference: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows
        https://azure.microsoft.com/en-us/blog/azure-backup-now-supports-storage-accounts-secured-with-azure- storage-firewalls-and-virtual-networks/
        QUESTION 5
        HOTSPOT
        You have an Azure subscription named Subscription1 that contains the resources shown in the following table.
        The status of VM1 is Running.
        You assign an Azure policy as shown in the exhibit. (Click the Exhibit tab.)
        You assign the policy by using the following parameters:
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        QUESTION 6
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed: Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 2
        You plan to store media files in the rg1lod9172796 storage account.
        You need to configure the storage account to store the media files. The solution must ensure that only users who have access keys can download the media files and that the files are accessible only over HTTPS.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        We should create an Azure file share.
        Step 1: In the Azure portal, select All services. In the list of resources, type Storage Accounts. As you begin typing, the list filters based on your input. Select Storage Accounts.
        On the Storage Accounts window that appears. Step 2: Locate the rg1lod9172796 storage account.
        Step 3: On the storage account page, in the Services section, select Files.
        Step 4: On the menu at the top of the File service page, click + File share. The New file share page drops down.
        Step 5: In Name type myshare. Click OK to create the Azure file share. References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal
        QUESTION 7
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        
        Task 1
        You plan to migrate a large amount of corporate data to Azure Storage and to back up files stored on old hardware to Azure Storage.
        You need to create a storage account named corpdata9172795n1 in the corpdatalod9172795 resource group. The solution must meet the following requirements:
        Corpdata9172795n1 must be able to host the virtual disk files for Azure virtual machines. The cost of accessing the files must be minimized.
        Replication costs must be minimized.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: In the Azure portal, click All services. In the list of resources, type Storage Accounts. As you begin typing, the list filters based on your input. Select Storage Accounts.
        Step 2: On the Storage Accounts window that appears, choose Add. Step 3: Select the subscription in which to create the storage account. Step 4: Under the Resource group field, select corpdatalod9172795.
        Step 5: Enter a name for your storage account: corpdata9172795n1
        Step 6: For Account kind select: General-purpose v2 accounts (recommended for most scenarios) General-purpose v2 accounts is recommended for most scenarios. . General-purpose v2 accounts deliver the lowest per-gigabyte capacity prices for Azure Storage, as well as industry-competitive transaction
        prices.
        Step 7: For replication select: Read-access geo-redundant storage (RA-GRS)
        Read-access geo-redundant storage (RA-GRS) maximizes availability for your storage account. RA-GRS provides read-only access to the data in the secondary location, in addition to geo-replication across two regions.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview
        QUESTION 8
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        Task 2
        You plan to move backup files and documents from an on-premises Windows file server to Azure Storage. The backup files will be stored as blobs.
        You need to create a storage account named corpdata9172795n2. The solution must meet the following requirements:
        Ensure that the documents are accessible via drive mappings from Azure virtual machines that run Windows Server 2016.
        Provide the highest possible redundancy for the documents. Minimize storage access costs.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: In the Azure portal, click All services. In the list of resources, type Storage Accounts. As you begin typing, the list filters based on your input. Select Storage Accounts.
        Step 2: On the Storage Accounts window that appears, choose Add.
        Step 3: Select the subscription in which to create the storage account.
        Step 4: Under the Resource group field, select Create New. Create a new Resource
        Step 5: Enter a name for your storage account: corpdata9172795n2
        Step 6: For Account kind select: General-purpose v2 accounts (recommended for most scenarios) General-purpose v2 accounts is recommended for most scenarios. General-purpose v2 accounts deliver the lowest per-gigabyte capacity prices for Azure Storage, as well as industry-competitive transaction prices.
        Step 7: For replication select: Read-access geo-redundant storage (RA-GRS)
        Read-access geo-redundant storage (RA-GRS) maximizes availability for your storage account. RA-GRS provides read-only access to the data in the secondary location, in addition to geo-replication across two regions.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview
        QUESTION 9
        You have an Azure subscription that contains the resources in the following table.
        Store1 contains a file share named Data. Data contains 5,000 files.
        You need to synchronize the files in Data to an on-premises server named Server1.
        Which three actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Download an automation script.
        B. Register Server1.
        C. Create a sync group.
        D. Create a container instance.
        E. Install the Azure File Sync agent on Server1.
        Correct Answer: BCE Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1 (E): Install the Azure File Sync agent on Server1
        The Azure File Sync agent is a downloadable package that enables Windows Server to be synced with an Azure file share
        Step 2 (B): Register Server1.
        Register Windows Server with Storage Sync Service
        Registering your Windows Server with a Storage Sync Service establishes a trust relationship between your server (or cluster) and the Storage Sync Service.
        Step 3 (C): Create a sync group and a cloud endpoint.
        A sync group defines the sync topology for a set of files. Endpoints within a sync group are kept in sync with each other. A sync group must contain one cloud endpoint, which represents an Azure file share and one or more server endpoints. A server endpoint represents a path on registered server.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-deployment-guide
        QUESTION 10
        DRAG DROP
        You have an Azure subscription named Subscription1.
        You create an Azure Storage account named contosostorage, and then you create a file share named data.
        Which UNC path should you include in a script that references files from the data file share? To answer, drag the appropriate values to the correct targets. Each value may be used once, more than once, or not at all. You may need to drag the split bar between panes or scroll to view content.
        NOTE: Each correct selection is worth one point.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: contosostorage The name of account
        Box 2: file.core.windows.net
        Box 3: data
        The name of the file share is data. Example:
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows
        QUESTION 11
        DRAG DROP
        You have an Azure subscription that contains a storage account.
        You have an on-premises server named Server1 that runs Windows Server 2016. Server1 has 2 TB of data.
        You need to transfer the data to the storage account by using the Azure Import/Export service.
        In which order should you perform the actions? To answer, move all actions from the list of actions to the answer area and arrange them in the correct order.
        NOTE: More than one order of answer choices is correct. You will receive credit for any of the correct orders you select.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        At a high level, an import job involves the following steps:
        Step 1: Attach an external disk to Server1 and then run waimportexport.exe
        Determine data to be imported, number of drives you need, destination blob location for your data in Azure storage.
        Use the WAImportExport tool to copy data to disk drives. Encrypt the disk drives with BitLocker.
        Step 2: From the Azure portal, create an import job.
        Create an import job in your target storage account in Azure portal. Upload the drive journal files.
        Step 3: Detach the external disks from Server1 and ship the disks to an Azure data center. Provide the return address and carrier account number for shipping the drives back to you. Ship the disk drives to the shipping address provided during job creation.
        Step 4: From the Azure portal, update the import job
        Update the delivery tracking number in the import job details and submit the import job. The drives are received and processed at the Azure data center.
        The drives are shipped using your carrier account to the return address provided in the import job.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-import-export-service
        QUESTION 12
        You have the Azure virtual machines shown in the following table.
        You have a Recovery Services vault that protects VM1 and VM2. You need to protect VM3 and VM4 by using Recovery Services. What should you do first?
        A. Create a new backup policy.
        B. Configure the extensions for VM3 and VM4.
        C. Create a storage account.
        D. Create a new Recovery Services vault.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        A Recovery Services vault is a storage entity in Azure that houses data. The data is typically copies of data, or configuration information for virtual machines (VMs), workloads, servers, or workstations. You can use Recovery Services vaults to hold backup data for various Azure services
        References: https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-tutorial-enable-replication
        QUESTION 13
        HOTSPOT
        You have an Azure subscription named Subscription1 that is associated to an Azure Active Directory (Azure AD) tenant named AAD1.
        Subscription1 contains the objects in the following table.
        You plan to create a single backup policy for Vault1.
        To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Share1 only
        Box 2: 99 years
        With the latest update to Azure Backup, customers can retain their data for up to 99 years in Azure. Note: A backup policy defines a matrix of when the data snapshots are taken, and how long those snapshots are retained.
        The backup policy interface looks like this:
        References: https://docs.microsoft.com/en-us/azure/backup/backup-azure-files
        https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-first-look-arm#defining-a-backup-policy
        https://blogs.microsoft.com/firehose/2015/02/16/february-update-to-azure-backup-includes-data-retention- up-to-99-years-offline-backup-and-more/
        QUESTION 14
        HOTSPOT
        You have an Azure subscription named Subscription1.
        In Subscription1, you create an Azure file share named share1.
        You create a shared access signature (SAS) named SAS1 as shown in the following exhibit.
        To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Will have no access
        The IP 193.77.134.1 does not have access on the SAS.
        Box 2: Will have read, write, and list access
        The net use command is used to connect to file shares.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-dotnet-shared-access-signature-part-1
        https://docs.microsoft.com/en-us/azure/vs-azure-tools-storage-manage-with-storage-explorer? tabs=windows
        QUESTION 15
        HOTSPOT
        You have Azure Storage accounts as shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: storageaccount1 and storageaccount2 only Box 2: All the storage accounts
        Note: The three different storage account options are: General-purpose v2 (GPv2) accounts, General- purpose v1 (GPv1) accounts, and Blob storage accounts.
        General-purpose v2 (GPv2) accounts are storage accounts that support all of the latest features for blobs, files, queues, and tables.
        Blob storage accounts support all the same block blob features as GPv2, but are limited to supporting only block blobs.
        General-purpose v1 (GPv1) accounts provide access to all Azure Storage services, but may not have the latest features or the lowest per gigabyte pricing.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-account-options
        QUESTION 16
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 1
        You plan to prevent users from accidentally deleting blob data from Azure.
        You need to ensure that administrators can recover any blob data that is deleted accidentally from the storagelod9272261 storage account for 14 days after the deletion occurred.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Task A: Create a Recovery Services vault (if a vault already exists skip this task, go to Task B below) A1. From Azure Portal, On the Hub menu, click All services and in the list of resources, type Recovery Services and click Recovery Services vaults.
        If there are recovery services vaults in the subscription, the vaults are listed. A2. On the Recovery Services vaults menu, click Add.
        A3. The Recovery Services vault blade opens, prompting you to provide a Name, Subscription, Resource group, and Location
        Task B. Create a backup goal
        B1. On the Recovery Services vault blade (for the vault you just created), in the Getting Started section, click Backup, then on the Getting Started with Backup blade, select Backup goal.
        The Backup Goal blade opens. If the Recovery Services vault has been previously configured, then the Backup Goal blades opens when you click Backup on the Recovery Services vault blade.
        B2. From the Where is your workload running? drop-down menu, select Azure.
        B3. From the What do you want to backup? menu, select Blob Storage, and click OK. B4. Finish the Wizard.
        Task C. create a backup schedule
        C1. Open the Microsoft Azure Backup agent. You can find it by searching your machine for Microsoft Azure Backup.
        C2. In the Backup agent's Actions pane, click Schedule Backup to launch the Schedule Backup Wizard.
        C3. On the Getting started page of the Schedule Backup Wizard, click Next. C4. On the Select Items to Backup page, click Add Items.
        The Select Items dialog opens.
        C5. Select Blob Storage you want to protect, and then click OK. C6. In the Select Items to Backup page, click Next.
        On the Specify Backup Schedule page, specify Schedule a backup every day, and click Next.
        C7. On the Select Retention Policy page, set it to 14 days, and click Next.
        C8. Finish the Wizard.
        References: https://docs.microsoft.com/en-us/azure/backup/backup-configure-vault
        QUESTION 17
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time
        appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 2
        Your company plans to store several documents on a public website.
        You need to create a container named bios that will host the documents in the storagelod9272261 storage account. The solution must ensure anonymous access and must ensure that users can browse folders in the container.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Azure portal create public container
        To create a container in the Azure portal, follow these steps:
        Step 1: Navigate to your new storage account in the Azure portal.
        Step 2: In the left menu for the storage account, scroll to the lob service section, then select Blobs. Select the + Container button.
        Type a name for your new container: bios
        Set the level of public access to the container: Select anonymous access.
        Step 3: Select OK to create the container. References: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-portal
        QUESTION 18
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 3
        Your company plans to host in Azure the source files of several line-of-business applications.
        You need to create an Azure file share named corpsoftware in the storagelod9272261 storage account. The solution must ensure that corpsoftware can store only up to 250 GB of data.
        What should you do from the Azure portal?
        Correct Answer: See explanation below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Go to the Storage Account blade on the Azure portal:
        Step 2: Click on add File Share button:
        Step 3: Provide Name (storagelod9272261) and Quota (250 GB).
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-create-file-share
        QUESTION 19
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 6
        You recently created a virtual machine named Web01.
        You need to attach a new 80-GB standard data disk named Web01-Disk1 to Web01. What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Add a data disk
        Step 1: In the Azure portal, from the menu on the left, select Virtual machines. Step 2: Select the Web01 virtual machine from the list.
        Step 3: On the Virtual machine page, , in Essentials, select Disks.
        Step 4: On the Disks page, select the Web01-Disk1 from the list of existing disks. Step 5: In the Disks pane, click + Add data disk.
        Step 6: Click the drop-down menu for Name to view a list of existing managed disks accessible to your Azure subscription. Select the managed disk Web01-Disk1 to attach:
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal
        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Contoso, Ltd. is a manufacturing company that has offices worldwide. Contoso works with partner organizations to bring products to market.
        Contoso products are manufactured by using blueprint files that the company authors and maintains.
        Existing Environment
        Currently, Contoso uses multiple types of servers for business operations, including the following: File servers
        Domain controllers
        Microsoft SQL Server servers
        Your network contains an Active Directory forest named contoso.com. All servers and client computers are joined to Active Directory.
        You have a public-facing application named App1. App1 is comprised of the following three tiers: A SQL database
        A web front end
        A processing middle tier
        Each tier is comprised of five virtual machines. Users access the web front end by using HTTPS only.
        Requirements Planned Changes
        Contoso plans to implement the following changes to the infrastructure:
        Move all the tiers of App1 to Azure.
        Move the existing product blueprint files to Azure Blob storage.
        Create a hybrid directory to support an upcoming Microsoft Office 365 migration project.
        Technical Requirements
        Contoso must meet the following technical requirements:
        Move all the virtual machines for App1 to Azure.
        Minimize the number of open ports between the App1 tiers.
        Ensure that all the virtual machines for App1 are protected by backups. Copy the blueprint files to Azure over the Internet.
        Ensure that the blueprint files are stored in the archive storage tier. Ensure that partner access to the blueprint files is secured and temporary.
        Prevent user passwords or hashes of passwprds from being stored in Azure. Use unmanaged standard storage for the hard disks of the virtual machines.
        Ensure that when users join devices to Azure Active Directory (Azure AD), the users use a mobile phone to verify their identity
        Minimize administrative effort whenever possible
        User Requirements
        Contoso identifies the following requirements for users:
        Ensure that only users who are part of a group named Pilot can join devices to Azure AD. Designate a new user named Admin1 as the service admin for the Azure subscription.
        Admin1 must receive email alerts regarding service outages.
        Ensure that a new user named User3 can create network objects for the Azure subscription.
        QUESTION 1
        HOTSPOT
        You need to identify the storage requirements for Contoso.
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Yes
        Contoso is moving the existing product blueprint files to Azure Blob storage.
        Use unmanaged standard storage for the hard disks of the virtual machines. We use Page Blobs for these. Box 2: No
        Box 3: No
        QUESTION 2
        You need to move the blueprint files to Azure. What should you do?
        A. Use Azure Storage Explorer to copy the files.
        B. Use the Azure Import/Export service.
        C. Generate a shared access signature (SAS). Map a drive, and then copy the files by using File Explorer.
        D. Generate an access key. Map a drive, and then copy the files by using File Explorer.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Azure Storage Explorer is a free tool from Microsoft that allows you to work with Azure Storage data on Windows, macOS, and Linux. You can use it to upload and download data from Azure blob storage.
        Scenario:
        Planned Changes include: move the existing product blueprint files to Azure Blob storage. Technical Requirements include: Copy the blueprint files to Azure over the Internet.
        References: https://docs.microsoft.com/en-us/azure/machine-learning/team-data-science-process/move-data-to-azure- blob-using-azure-storage-explorer
        QUESTION 3
        You need to implement a backup solution for App1 after the application is moved. What should you create first?
        A. a recovery plan
        B. a Recovery Services vault
        C. an Azure Backup Server
        D. a backup policy
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        A Recovery Services vault is a logical container that stores the backup data for each protected resource, such as Azure VMs. When the backup job for a protected resource runs, it creates a recovery point inside the Recovery Services vault.
        Scenario:
        There are three application tiers, each with five virtual machines. Move all the virtual machines for App1 to Azure.
        Ensure that all the virtual machines for App1 are protected by backups.
        References: https://docs.microsoft.com/en-us/azure/backup/quick-backup-vm-portal
        Testlet 3
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message: "Licenses not assigned. License assignment failed for one user."
        You verify that the Azure subscription has the available licenses.
        Requirements Planned Changes
        Humongous Insurance plans to open a new office in Paris. The Paris office will contain 1,000 users who will
        be hired during the next 12 months. All the resources used by the Paris office users will be hosted in Azure.
        Planned Azure AD Infrastructure
        The on-premises Active Directory domain will be synchronized to Azure AD.
        All client computers in the Paris office will be joined to an Azure AD domain.
        Planned Azure Networking Infrastructure
        You plan to create the following networking resources in a resource group named All_Resources:
        Default Azure system routes that will be the only routes used to route traffic
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a separate resource group. The initial configuration of the web apps will be identical. The web administrators have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO) when accessing resources in Azure.
        QUESTION 1
        DRAG DROP
        You need to prepare the environment to ensure that the web administrators can deploy the web apps as quickly as possible.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1:
        First you create a storage account using the Azure portal.
        Step 2:
        Select Automation options at the bottom of the screen. The portal shows the template on the Template tab. Add the storage account to the library.
        Step 3:
        Share the template.
        Scenario: Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a separate resource group. The initial configuration of the web apps will be identical. The web administrators have permission to deploy web apps to resource groups.
        References: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-quickstart-create- templates-use-the-portal
        Question Set 1
        QUESTION 1
        You plan to automate the deployment of a virtual machine scale set that uses the Windows Server 2016 Datacenter image.
        You need to ensure that when the scale set virtual machines are provisioned, they have web server components installed.
        Which two actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Modify the extensionProfile section of the Azure Resource Manager template.
        B. Create an automation account.
        C. Upload a configuration script.
        D. Create a new virtual machine scale set in the Azure portal.
        E. Create an Azure policy.
        Correct Answer: AD Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Virtual Machine Scale Sets can be used with the Azure Desired State Configuration (DSC) extension handler. Virtual machine scale sets provide a way to deploy and manage large numbers of virtual machines, and can elastically scale in and out in response to load. DSC is used to configure the VMs as they come online so they are running the production software.
        References: https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-dsc
        QUESTION 2
        DRAG DROP
        You have two Azure virtual machines named VM1 and VM2. VM1 has a single data disk named Disk1. You need to attach Disk1 to VM2. The solution must minimize downtime for both virtual machines.
        Which four actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Stop VM1.
        Step 2: Detach Disk1 from VM1.
        Step 3: Attach Disk1 to VM2 Attach an existing disk
        Follow these steps to reattach an existing available data disk to a running VM.
        1. Select a running VM for which you want to reattach a data disk.
        2. From the menu on the left, select Disks.
        3. Select Attach existing to attach an available data disk to the VM.
        4. From the Attach existing disk pane, select OK.
        Step 4: Start VM1.
        Detach a data disk using the portal
        1. In the left menu, select Virtual Machines.
        2. Select the virtual machine that has the data disk you want to detach and click Stop to deallocate the VM.
        3. In the virtual machine pane, select Disks.
        4. At the top of the Disks pane, select Edit.
        5. In the Disks pane, to the far right of the data disk that you would like to detach, click the Detach button image detach button.
        6. After the disk has been removed, click Save on the top of the pane.
        7. In the virtual machine pane, click Overview and then click the Start button at the top of the pane to restart the VM.
        8. The disk stays in storage but is no longer attached to a virtual machine.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/detach-disk https://docs.microsoft.com/en-us/azure/lab-services/devtest-lab-attach-detach-data-disk
        QUESTION 3
        HOTSPOT
        You have an Azure subscription named Subscription1. Subscription1 contains a virtual machine named VM1.
        You install and configure a web server and a DNS server on VM1.
        VM1 has the effective network security rules shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1:
        Rule2 blocks ports 50-60, which includes port 53, the DNS port. Internet users can reach the Web server, since it uses port 80.
        Box 2:
        If Rule2 is removed internet users can reach the DNS server as well.
        Note: Rules are processed in priority order, with lower numbers processed before higher numbers, because lower numbers have higher priority. Once traffic matches a rule, processing stops. As a result, any rules that exist with lower priorities (higher numbers) that have the same attributes as rules with higher priorities are not processed.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/security-overview
        QUESTION 4
        DRAG DROP
        You have an Azure Linux virtual machine that is protected by Azure Backup. One week ago, two files were deleted from the virtual machine.
        You need to restore the deleted files to an on-premises computer as quickly as possible.
        Which four actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        To restore files or folders from the recovery point, go to the virtual machine and choose the desired recovery point.
        Step 0. In the virtual machine's menu, click Backup to open the Backup dashboard. Step 1. In the Backup dashboard menu, click File Recovery.
        Step 2. From the Select recovery point drop-down menu, select the recovery point that holds the files you want. By default, the latest recovery point is already selected.
        Step 3: To download the software used to copy files from the recovery point, click Download Executable (for Windows Azure VM) or Download Script (for Linux Azure VM, a python script is generated).
        Step 4: Copy the files by using AzCopy
        AzCopy is a command-line utility designed for copying data to/from Microsoft Azure Blob, File, and Table storage, using simple commands designed for optimal performance. You can copy data between a file
        system and a storage account, or between storage accounts.
        References: https://docs.microsoft.com/en-us/azure/backup/backup-azure-restore-files-from-vm https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy
        QUESTION 5
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 3
        You plan to protect on-premises virtual machines and Azure virtual machines by using Azure Backup.
        You need to prepare the backup infrastructure in Azure. The solution must minimize the cost of storing the backups in Azure.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        First, create Recovery Services vault.
        Step 1: On the left-hand menu, select All services and in the services list, type Recovery Services. As you type, the list of resources filters. When you see Recovery Services vaults in the list, select it to open the Recovery Services vaults menu.
        Step 2: In the Recovery Services vaults menu, click Add to open the Recovery Services vault menu.
        Step 3: In the Recovery Services vault menu, for example, Type myRecoveryServicesVault in Name.
        The current subscription ID appears in Subscription. If you have additional subscriptions, you could choose another subscription for the new vault.
        For Resource group select Use existing and choose myResourceGroup. If myResourceGroup doesn't exist, select Create new and type myResourceGroup.
        From the Location drop-down menu, choose West Europe. Click Create to create your Recovery Services vault.
        References: https://docs.microsoft.com/en-us/azure/backup/tutorial-backup-vm-at-scale
        QUESTION 6
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        
        Task 3
        You need to deploy two Azure virtual machines named VM1003a and VM1003b based on an Ubuntu Server image. The deployment must meet the following requirements:
        Provide a Service Level Agreement (SLA) of 99.95 percent availability. Use managed disks.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Open the Azure portal.
        Step 2: On the left menu, select All resources. You can sort the resources by Type to easily find your images.
        Step 3: Select the image you want to use from the list. The image Overview page opens. Step 4: Select Create VM from the menu.
        Step 5: Enter the virtual machine information.
        Select VM1003a as the name for the first Virtual machine.
        The user name and password entered here will be used to log in to the virtual machine. When complete, select OK. You can create the new VM in an existing resource group, or choose Create new to create a new resource group to store the VM.
        Step 6: Select a size for the VM. To see more sizes, select View all or change the Supported disk type filter. Step 7: Under Settings, make changes as necessary and select OK.
        Step 8: On the summary page, you should see your image name listed as a Private image. Select Ok to start the virtual machine deployment.
        Repeat the procedure for the second VM and name it VM1003b. References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-generalized-managed
        QUESTION 7
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        
        Task 4
        You need to deploy an Azure virtual machine named VM1004a based on an Ubuntu Server image, and then configure VM1004a to meet the following requirements:
        The virtual machine must contain data disks that can store at least 15 TB of data. The data disks must be able to provide at least 2.000 IOPS.
        Storage costs must be minimized.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Open the Azure portal.
        Step 2: On the left menu, select All resources. You can sort the resources by Type to easily find your images.
        Step 3: Select the image you want to use from the list. The image Overview page opens. Step 4: Select Create VM from the menu.
        Step 5: Enter the virtual machine information.
        Select VM1004a as the name for the first Virtual machine.
        The user name and password entered here will be used to log in to the virtual machine. When complete, select OK. You can create the new VM in an existing resource group, or choose Create new to create a new resource group to store the VM.
        Step 6: Select a size for the VM. To see more sizes, select View all or change the Supported disk type filter. To support 15 TB of data you would need a Premium disk.
        Step 7: Under Settings, make changes as necessary and select OK.
        Step 8: On the summary page, you should see your image name listed as a Private image. Select Ok to start the virtual machine deployment.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-generalized-managed
        QUESTION 8
        You have an Azure subscription that contains a virtual machine named VM1. VM1 hosts a line-of-business application that is available 24 hours a day. VM1 has one network interface and one managed disk. VM1 uses the D4s v3 size.
        You plan to make the following changes to VM1: Change the size to D8s v3.
        Add a 500-GB managed disk. Add the Puppet Agent extension.
        Attach an additional network interface.
        Which change will cause downtime for VM1?
        A. Add the Puppet Agent extension.
        B. Change the size to D8s v3.
        C. Add a 500-GB managed disk.
        D. Attach an additional network interface.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        While resizing the VM it must be in a stopped state.
        References: https://azure.microsoft.com/en-us/blog/resize-virtual-machines/
        QUESTION 9
        You have an Azure virtual machine named VM1 that you use for testing. VM1 is protected by Azure Backup. You delete VM1.
        You need to remove the backup data stored for VM1. What should you do first?
        A. Delete the Recovery Services vault.
        B. Delete the storage account.
        C. Stop the backup
        D. Modify the backup policy.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Azure Backup provides backup for virtual machines — created through both the classic deployment model and the Azure Resource Manager deployment model — by using custom-defined backup policies in a Recovery Services vault.
        With the release of backup policy management, customers can manage backup policies and model them to meet their changing requirements from a single window. Customers can edit a policy, associate more virtual machines to a policy, and delete unnecessary policies to meet their compliance requirements.
        Incorrect Answers:
        B: You can't delete a Recovery Services vault if it is registered to a server and holds backup data. If you try to delete a vault, but can't, the vault is still configured to receive backup data.
        References: https://azure.microsoft.com/en-in/updates/azure-vm-backup-policy-management/
        QUESTION 10
        You have an Azure subscription named Subscription1.
        You deploy a Linux virtual machine named VM1 to Subscription1. You need to monitor the metrics and the logs of VM1.
        What should you use?
        A. the AzurePerformanceDiagnostics extension
        B. Azure HDInsight
        C. Linux Diagnostic Extension (LAD) 3.0
        D. Azure Analysis Services
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can use extensions to configure diagnostics on your VMs to collect additional metric data.
        The basic host metrics are available, but to see more granular and VM-specific metrics, you need to install the Azure diagnostics extension on the VM. The Azure diagnostics extension allows additional monitoring and diagnostics data to be retrieved from the VM.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-monitoring
        QUESTION 11
        DRAG DROP
        You have an availability set named AS1 that contains three virtual machines named VM1, VM2, and VM3.
        You attempt to reconfigure VM1 to use a larger size. The operation fails and you receive an allocation failure message.
        You need to ensure that the resize operation succeeds.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the
        list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Stop VM1, VM, and VM3.
        If the VM you wish to resize is part of an availability set, then you must stop all VMs in the availability set before changing the size of any VM in the availability set. The reason all VMs in the availability set must be stopped before performing the resize operation to a size that requires different hardware is that all running VMs in the availability set must be using the same physical hardware cluster. Therefore, if a change of
        physical hardware cluster is required to change the VM size then all VMs must be first stopped and then restarted one-by-one to a different physical hardware clusters.
        Step 2: Resize VM1.
        Step 3: Start VM1, VM2, and VM3. References: https://azure.microsoft.com/es-es/blog/resize-virtual-machines/
        QUESTION 12
        You plan to back up an Azure virtual machine named VM1.
        You discover that the Backup Pre-Check status displays a status of Warning. What is a possible cause of the Warning status?
        A. VM1 is stopped.
        B. VM1 does not have the latest version of WaAppAgent.exe installed.
        C. VM1 has an unmanaged disk.
        D. A Recovery Services vault is unavailable.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        The Warning state indicates one or more issues in VM’s configuration that might lead to backup failures and provides recommended steps to ensure successful backups. Not having the latest VM Agent installed, for example, can cause backups to fail intermittently and falls in this class of issues.
        References: https://azure.microsoft.com/en-us/blog/azure-vm-backup-pre-checks/
        QUESTION 13
        You have an Azure subscription named Subscription1 that is used by several departments at your company. Subscription1 contains the resources in the following table.
        Another administrator deploys a virtual machine named VM1 and an Azure Storage account named Storage2 by using a single Azure Resource Manager template.
        You need to view the template used for the deployment.
        From which blade can you view the template that was used for the deployment?
        A. Container1
        B. RG1
        C. VM1
        D. Storage2
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        View template from deployment history
        1. Go to the resource group for your new resource group. Notice that the portal shows the result of the last deployment. Select this link.
        2. You see a history of deployments for the group. In your case, the portal probably lists only one deployment. Select this deployment.
        3. The portal displays a summary of the deployment. The summary includes the status of the deployment and its operations and the values that you provided for parameters. To see the template that you used for the deployment, select View template.
        References: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-export-template
        QUESTION 14
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure virtual machine named VM1. VM1 was deployed by using a custom Azure Resource Manager template named ARM1.json.
        You receive a notification that VM1 will be affected by maintenance. You need to move VM1 to a different host immediately.
        Solution: From the Overview blade, you move the virtual machine to a different subscription. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You would need to redeploy the VM.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/redeploy-to-new-node
        QUESTION 15
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure virtual machine named VM1. VM1 was deployed by using a custom Azure Resource Manager template named ARM1.json.
        You receive a notification that VM1 will be affected by maintenance. You need to move VM1 to a different host immediately.
        Solution: From the Redeploy blade, you click Redeploy. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        When you redeploy a VM, it moves the VM to a new node within the Azure infrastructure and then powers it back on, retaining all your configuration options and associated resources.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/redeploy-to-new-node
        QUESTION 16
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You have an Azure virtual machine named VM1. VM1 was deployed by using a custom Azure Resource Manager template named ARM1.json.
        You receive a notification that VM1 will be affected by maintenance. You need to move VM1 to a different host immediately.
        Solution: From the Update management blade, you click Enable. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You would need to redeploy the VM.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/redeploy-to-new-node
        QUESTION 17
        HOTSPOT
        You have an Azure subscription named Subscription1. Subscription1 contains two Azure virtual machines named VM1 and VM2. VM1 and VM2 run Windows Server 2016.
        VM1 is backed up daily by Azure Backup without using the Azure Backup agent. VM1 is affected by ransomware that encrypts data.
        You need to restore the latest backup of VM1.
        To which location can you restore the backup? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        QUESTION 18
        You download an Azure Resource Manager template based on an existing virtual machine. The template will be used to deploy 100 virtual machines.
        You need to modify the template to reference an administrative password. You must prevent the password from being stored in plain text.
        What should you create to store the password?
        A. an Azure Key Vault and an access policy
        B. a Recovery Services vault and a backup policy
        C. Azure Active Directory (AD) Identity Protection and an Azure policy
        D. an Azure Storage account and an access policy
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can use a template that allows you to deploy a simple Windows VM by retrieving the password that is stored in a Key Vault. Therefore, the password is never put in plain text in the template parameter file.
        References: https://azure.microsoft.com/en-us/resources/templates/101-vm-secure-password/
        QUESTION 19
        HOTSPOT
        You create a virtual machine scale set named Scale1. Scale1 is configured as shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1:
        The Autoscale scale out rule increases the number of VMs by 2 if the CPU threshold is 80% or higher. The initial instance count is 4 and rises to 6 when the 2 extra instances of VMs are added.
        Box 2:
        The Autoscale scale in rule decreases the number of VMs by 4 if the CPU threshold is 30% or lower. The initial instance count is 4 and thus cannot be reduced to 0 as the minimum instances is set to 2. Instances are only added when the CPU threshold reaches 80%.
        References: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/autoscale-overview https://docs.microsoft.com/en-us/azure/azure-monitor/platform/autoscale-best-practices https://docs.microsoft.com/en-us/azure/azure-monitor/platform/autoscale-common-scale-patterns
        QUESTION 20
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 4
        You plan to back up all the Azure virtual machines in your Azure subscription at 02:00 Coordinated Universal Time (UTC) daily.
        You need to prepare the Azure environment to ensure that any new virtual machines can be configured quickly for backup. The solution must ensure that all the daily backups performed at 02:00 UTC are stored
        for only 90 days.
        What should you do from your Recovery Services vault on the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Task A: Create a Recovery Services vault (if a vault already exists skip this task, go to Task B below) A1. From Azure Portal, On the Hub menu, click All services and in the list of resources, type Recovery Services and click Recovery Services vaults.
        If there are recovery services vaults in the subscription, the vaults are listed. A2. On the Recovery Services vaults menu, click Add.
        A3. The Recovery Services vault blade opens, prompting you to provide a Name, Subscription, Resource group, and Location
        Task B.
        B1. On the Recovery Services vault blade (for the vault you just created), in the Getting Started section, click Backup, then on the Getting Started with Backup blade, select Backup goal.
        The Backup Goal blade opens. If the Recovery Services vault has been previously configured, then the Backup Goal blades opens when you click Backup on the Recovery Services vault blade.
        B2. From the Where is your workload running? drop-down menu, select Azure.
        B3. From the What do you want to backup? menu, select Virtual Machine, and click OK.
        B4. Finish the Wizard.
        Task C. create a backup schedule
        C1. Open the Microsoft Azure Backup agent. You can find it by searching your machine for Microsoft Azure Backup.
        C2. In the Backup agent's Actions pane, click Schedule Backup to launch the Schedule Backup Wizard.
        C3. On the Getting started page of the Schedule Backup Wizard, click Next. C4. On the Select Items to Backup page, click Add Items.
        The Select Items dialog opens.
        C5. Select Blob Storage you want to protect, and then click OK. C6. In the Select Items to Backup page, click Next.
        On the Specify Backup Schedule page, specify Schedule a backup every: day
        At the following times: 2.00 AM
        C7. On the Select Retention Policy page, set it to 90 days, and click Next.
        C8. Finish the Wizard.
        References: https://docs.microsoft.com/en-us/azure/backup/backup-configure-vault
        QUESTION 21
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task5
        You plan to connect several virtual machines to the VNET01-USEA2 virtual network.
        In the Web-RGlod9272261 resource group, you need to create a virtual machine that uses the Standard_B2ms size named Web01 that runs Windows Server 2016. Web01 must be added to an availability set.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Choose Create a resource in the upper left-hand corner of the Azure portal.
        Step 2: In the Basics tab, under Project details, make sure the correct subscription is selected and then choose Web-RGlod9272261 resource group
        Step 3: Under Instance details type/select: Virtual machine name: Web01
        Image: Windows Server 2016 Size: Standard_B2ms size Leave the other defaults.
        Step 4: Finish the Wizard
        Testlet 2 Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Contoso, Ltd. is a consulting company that has a main office in Montreal and two branch offices in Seattle and New York.
        The Montreal office has 2,000 employees. The Seattle office has 1,000 employees. The New York office has 200 employees.
        All the resources used by Contoso are hosted on-premises.
        Contoso creates a new Azure subscription. The Azure Active Directory (Azure AD) tenant uses a domain named contoso.onmicrosoft.com. The tenant uses the P1 pricing tier.
        Existing Environment
        The network contains an Active Directory forest named contoso.com. All domain controllers are configured as DNS servers and host the contoso.com DNS zone.
        Contoso has finance, human resources, sales, research, and information technology departments. Each department has an organizational unit (OU) that contains all the accounts of that respective department. All the user accounts have the department attribute set to their respective department. New users are added frequently.
        Contoso.com contains a user named User1. All the offices connect by using private links.
        Contoso has data centers in the Montreal and Seattle offices. Each data center has a firewall that can be configured as a VPN device.
        All infrastructure servers are virtualized. The virtualization environment contains the servers in the following table.
        Contoso uses two web applications named App1 and App2. Each instance on each web application requires 1GB of memory.
        The Azure subscription contains the resources in the following table.
        The network security team implements several network security groups (NSGs).
        Planned Changes
        Contoso plans to implement the following changes: Deploy Azure ExpressRoute to the Montreal office.
        Migrate the virtual machines hosted on Server1 and Server2 to Azure. Synchronize on-premises Active Directory to Azure Active Directory (Azure AD). Migrate App1 and App2 to two Azure web apps named WebApp1 and WebApp2.
        Technical requirements
        Contoso must meet the following technical requirements:
        Ensure that WebApp1 can adjust the number of instances automatically based on the load and can scale up to five instances.
        Ensure that VM3 can establish outbound connections over TCP port 8080 to the applications servers in the Montreal office.
        Ensure that routing information is exchanged automatically between Azure and the routers in the Montreal office.
        Ensure Azure Multi-Factor Authentication (MFA) for the users in the finance department only. Ensure that webapp2.azurewebsites.net can be accessed by using the name app2.contoso.com Connect the New York office to VNet1 over the Internet by using an encrypted connection.
        Create a workflow to send an email message when the settings of VM4 are modified. Create a custom Azure role named Role1 that is based on the Reader role.
        Minimize costs whenever possible.
        QUESTION 1
        You discover that VM3 does NOT meet the technical requirements. You need to verify whether the issue relates to the NSGs.
        What should you use?
        A. Diagram in VNet1
        B. the security recommendations in Azure Advisor
        C. Diagnostic settings in Azure Monitor
        D. Diagnose and solve problems in Traffic Manager profiles
        E. IP flow verify in Azure Network Watcher
        Correct Answer: E Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Scenario: Contoso must meet technical requirements including:
        Ensure that VM3 can establish outbound connections over TCP port 8080 to the applications servers in the Montreal office.
        IP flow verify checks if a packet is allowed or denied to or from a virtual machine. The information consists of direction, protocol, local IP, remote IP, local port, and remote port. If the packet is denied by a security group, the name of the rule that denied the packet is returned. While any source or destination IP can be chosen, IP flow verify helps administrators quickly diagnose connectivity issues from or to the internet and from or to the on-premises environment.
        References: https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-ip-flow-verify-overview
        Question Set 1
        QUESTION 1
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        Your company registers a domain name of contoso.com.
        You create an Azure DNS zone named contoso.com, and then you add an A record to the zone for a host named www that has an IP address of 131.107.1.10.
        You discover that Internet hosts are unable to resolve www.contoso.com to the 131.107.1.10 IP address. You need to resolve the name resolution issue.
        Solution: You modify the name servers at the domain registrar. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Modify the Name Server (NS) record.
        References: https://docs.microsoft.com/en-us/azure/dns/dns-delegate-domain-azure-dns
        QUESTION 2
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        Your company registers a domain name of contoso.com.
        You create an Azure DNS zone named contoso.com, and then you add an A record to the zone for a host named www that has an IP address of 131.107.1.10.
        You discover that Internet hosts are unable to resolve www.contoso.com to the 131.107.1.10 IP address. You need to resolve the name resolution issue.
        Solution: You modify the SOA record in the contoso.com zone. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B
        Section: [none]
        Explanation
        Explanation/Reference:
        Explanation:
        Modify the NS record, not the SOA record.
        Note: The SOA record stores information about the name of the server that supplied the data for the zone; the administrator of the zone; the current version of the data file; the number of seconds a secondary name server should wait before checking for updates; the number of seconds a secondary name server should wait before retrying a failed zone transfer; the maximum number of seconds that a secondary name server can use data before it must either be refreshed or expire; and a default number of seconds for the time-to- live file on resource records.
        References: https://searchnetworking.techtarget.com/definition/start-of-authority-record
        QUESTION 3
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        Your company registers a domain name of contoso.com.
        You create an Azure DNS zone named contoso.com, and then you add an A record to the zone for a host named www that has an IP address of 131.107.1.10.
        You discover that Internet hosts are unable to resolve www.contoso.com to the 131.107.1.10 IP address. You need to resolve the name resolution issue.
        Solution: You add an NS record to the contoso.com Azure DNS zone. Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Before you can delegate your DNS zone to Azure DNS, you need to know the name servers for your zone. The NS record set contains the names of the Azure DNS name servers assigned to the zone.
        References: https://docs.microsoft.com/en-us/azure/dns/dns-delegate-domain-azure-dns
        QUESTION 4
        You are troubleshooting a performance issue for an Azure Application Gateway.
        You need to compare the total requests to the failed requests during the past six hours. What should you use?
        A. NSG flow logs in Azure Network Watcher
        B. Metrics in Application Gateway
        C. Connection monitor in Azure Network Watcher
        D. Diagnostics logs in Application Gateway
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-diagnostics#metrics
        QUESTION 5
        You have two subscriptions named Subscription1 and Subscription2. Each subscription is associated to a different Azure AD tenant.
        Subscription1 contains a virtual network named VNet1. VNet1 contains an Azure virtual machine named VM1 and has an IP address space of 10.0.0.0/16.
        Subscription2 contains a virtual network named VNet2. VNet2 contains an Azure virtual machine named VM2 and has an IP address space of 10.10.0.0/24.
        You need to connect VNet1 to VNet2. What should you do first?
        A. Move VM1 to Subscription2.
        B. Modify the IP address space of VNet2.
        C. Provision virtual network gateways.
        D. Move VNet1 to Subscription2.
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        The virtual networks can be in the same or different regions, and from the same or different subscriptions. When connecting VNets from different subscriptions, the subscriptions do not need to be associated with the same Active Directory tenant.
        Configuring a VNet-to-VNet connection is a good way to easily connect VNets. Connecting a virtual network to another virtual network using the VNet-to-VNet connection type (VNet2VNet) is similar to creating a Site- to-Site IPsec connection to an on-premises location. Both connectivity types use a VPN gateway to provide a secure tunnel using IPsec/IKE, and both function the same way when communicating.
        The local network gateway for each VNet treats the other VNet as a local site. This lets you specify additional address space for the local network gateway in order to route traffic.
        References: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager- portal
        QUESTION 6
        DRAG DROP
        You have an Azure subscription that contains two virtual networks named VNet1 and VNet2. Virtual machines connect to the virtual networks.
        The virtual networks have the address spaces and the subnets configured as shown in the following table.
        You need to add the address space of 10.33.0.0/16 to VNet1. The solution must ensure that the hosts on VNet1 and VNet2 can communicate.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the list of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none]
        Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Remove peering between Vnet1 and VNet2.
        You can't add address ranges to, or delete address ranges from a virtual network's address space once a virtual network is peered with another virtual network. To add or remove address ranges, delete the peering, add or remove the address ranges, then re-create the peering.
        Step 2: Add the 10.44.0.0/16 address space to VNet1. Step 3: Recreate peering between VNet1 and VNet2 References: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-manage-peering
        QUESTION 7
        You have an Azure subscription that contains the resources in the following table.
        To which subnets can you apply NSG1?
        A. the subnets on VNet2 only
        B. the subnets on VNet2 and VNet3 only
        C. the subnets on VNet1, VNet2, and VNet3
        D. the subnets on VNet1 only
        E. the subnets on VNet3 only
        Correct Answer: E Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        All Azure resources are created in an Azure region and subscription. A resource can only be created in a virtual network that exists in the same region and subscription as the resource.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-vnet-plan-design-arm
        QUESTION 8
        HOTSPOT
        You have an Azure virtual machine named VM1 that connects to a virtual network named VNet1. VM1 has the following configurations:
        Subnet 10.0.0.0/24 Availability set: AVSet
        Network security group (NSG): None Private IP address: 10.0.0.4 (dynamic) Public IP address: 40.90.219.6 (dynamic)
        You deploy a standard, Internet-facing load balancer named slb1.
        You need to configure slb1 to allow connectivity to VM1.
        Which changes should you apply to VM1 as you configure slb1? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        QUESTION 9
        You have five Azure virtual machines that run Windows Server 2016. The virtual machines are configured as web servers.
        You have an Azure load balancer named LB1 that provides load balancing services for the virtual machines. You need to ensure that visitors are serviced by the same web server for each request.
        What should you configure?
        A. Protocol to UDP
        B. Session persistence to None
        C. Session persistence to Client IP
        D. Idle Time-out (minutes) to 20 Correct Answer: C
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can set the sticky session in load balancer rules with setting the session persistence as the client IP.
        References: https://cloudopszone.com/configure-azure-load-balancer-for-sticky-sessions/
        QUESTION 10
        You have the Azure virtual networks shown in the following table.
        To which virtual networks can you establish a peering connection from VNet1?
        A. VNet2 and VNet3 only
        B. VNet2 only
        C. VNet3 and VNet4 only
        D. VNet2, VNet3, and VNet4
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-connect-virtual-networks-portal
        QUESTION 11
        You have an Azure subscription that contains a policy-based virtual network gateway named GW1 and a virtual network named VNet1.
        You need to ensure that you can configure a point-to-site connection from VNet1 to an on-premises computer.
        Which two actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Reset GW1.
        B. Create a route-based virtual network gateway.
        C. Delete GW1.
        D. Add a public IP address space to VNet1.
        E. Add a connection to GW1.
        F. Add a service endpoint to VNet1.
        Correct Answer: BC Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        B: A VPN gateway is used when creating a VPN connection to your on-premises network.
        Route-based VPN devices use any-to-any (wildcard) traffic selectors, and let routing/forwarding tables direct traffic to different IPsec tunnels. It is typically built on router platforms where each IPsec tunnel is modeled as a network interface or VTI (virtual tunnel interface).
        C: Policy-based VPN devices use the combinations of prefixes from both networks to define how traffic is encrypted/decrypted through IPsec tunnels. It is typically built on firewall devices that perform packet filtering. IPsec tunnel encryption and decryption are added to the packet filtering and processing engine.
        Incorrect Answers:
        D: Point-to-Site connections do not require a VPN device or a public-facing IP address.
        References: https://docs.microsoft.com/en-us/azure/vpn-gateway/create-routebased-vpn-gateway-portal https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps
        QUESTION 12
        HOTSPOT
        You have an Azure subscription named Subscription1. Subscription1 contains the virtual networks in the following table.
        Subscription1 contains the virtual machines in the following table.
        The firewalls on all the virtual machines are configured to allow all ICMP traffic. You add the peerings in the following table.
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Yes
        Vnet1 and Vnet3 are peers.
        Box 2: Yes
        Vnet2 and Vnet3 are peers.
        Box 3: No
        Peering connections are non-transitive. References:
        https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke
        QUESTION 13
        You have an Azure subscription named Subscription1 that contains the resource groups shown in the following table.
        In RG1, you create a virtual machine named VM1 in the East Asia location. You plan to create a virtual network named VNET1.
        You need to create VNET1, and then connect VM1 to VNET1.
        What are two possible ways to achieve this goal? Each correct answer presents a complete solution.
        NOTE: Each correct selection is worth one point.
        A. Create VNET1 in RG2, and then set East Asia as the location.
        B. Create VNET1 in a new resource group in the West US location, and then set West US as the location.
        C. Create VNET1 in RG1, and then set East US as the location.
        D. Create VNET1 in RG2, and then set East US as the location.
        E. Create VNET1 in RG1, and then set East Asia as the location.
        Correct Answer: AE Section: [none] Explanation
        Explanation/Reference:
        QUESTION 14
        You have an Azure subscription that contains a virtual network named VNet1. VNet1 contains four subnets named Gateway, Perimeter, NVA, and Production.
        The NVA subnet contains two network virtual appliances (NVAs) that will perform network traffic inspection between the Perimeter subnet and the Production subnet.
        You need to implement an Azure load balancer for the NVAs. The solution must meet the following requirements:
        The NVAs must run in an active-active configuration that uses automatic failover.
        The NVAs must load balance traffic to two services on the Profuction subnet. The services have different IP addresses.
        Which three actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Add two load balancing rules that have HA Ports enabled and Floating IP disabled.
        B. Add a frontend IP configuration, two backend pools, and a health probe.
        C. Add two load balancing rules that have HA Ports and Floating IP enabled.
        D. Deploy a standard load balancer.
        E. Deploy a basic load balancer.
        F. Add a frontend IP configuration a backend pool, and a health probe.
        Correct Answer: BCD
        Section: [none]
        Explanation
        Explanation/Reference:
        Explanation:
        A standard load balancer is required for the HA ports.
        Two backend pools are needed as there are two services with different IP addresses. Floating IP rule is used where backend ports are reused.
        Incorrect Answers:
        F: HA Ports are not available for the basic load balancer.
        References: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-standard-overview https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-multivip-overview
        QUESTION 15
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 1
        Your on-premises network uses an IP address range of 131.107.2.0 to 131.107.2.255.
        You need to ensure that only device from the on-premises network can connect to the rg1lod9172796n1 storage account.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Navigate to the rg1lod9172796n1 storage account.
        Step 2: Click on the settings menu called Firewalls and virtual networks.
        Step 3: Ensure that you have elected to allow access from 'Selected networks'.
        Step 4: To grant access to an internet IP range, enter the address range of 131.107.2.0 to 131.107.2.255 (in CIDR format) under Firewall, Address Ranges.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-network-security
        QUESTION 16
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 4
        Another administrator attempts to establish connectivity between two virtual networks named VNET1 and VNET2.
        The administrator reports that connections across the virtual networks fail.
        You need to ensure that network connections can be established successfully between VNET1 and VNET2 as quickly as possible.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can connect one VNet to another VNet using either a Virtual network peering, or an Azure VPN Gateway.
        To create a virtual network gateway
        Step 1: In the portal, on the left side, click +Create a resource and type 'virtual network gateway' in search. Locate Virtual network gateway in the search return and click the entry. On the Virtual network gateway page, click Create at the bottom of the page to open the Create virtual network gateway page.
        Step 2: On the Create virtual network gateway page, fill in the values for your virtual network gateway.
        Name: Name your gateway. This is not the same as naming a gateway subnet. It's the name of the gateway object you are creating.
        Gateway type: Select VPN. VPN gateways use the virtual network gateway type VPN.
        Virtual network: Choose the virtual network to which you want to add this gateway. Click Virtual network to open the 'Choose a virtual network' page. Select the VNet. If you don't see your VNet, make sure the Location field is pointing to the region in which your virtual network is located.
        Gateway subnet address range: You will only see this setting if you did not previously create a gateway subnet for your virtual network. If you previously created a valid gateway subnet, this setting will not appear.
        Step 4: Select Create New to create a Gateway subnet.
        Step 5: Click Create to begin creating the VPN gateway. The settings are validated and you'll see the "Deploying Virtual network gateway" tile on the dashboard. Creating a gateway can take up to 45 minutes. You may need to refresh your portal page to see the completed status.
        References: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager- portal?
        QUESTION 17
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 5
        You plan to configure VM1 to be accessible from the Internet.
        You need to add a public IP address to the network interface used by VM1. What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can add private and public IP addresses to an Azure network interface by completing the steps that follow.
        Step 1: In Azure portal, click More services > type virtual machines in the filter box, and then click Virtual machines.
        Step 2: In the Virtual machines pane, click the VM you want to add IP addresses to. Click Network interfaces in the virtual machine pane that appears, and then select the network interface you want to add the IP addresses to. In the example shown in the following picture, the NIC named myNIC from the VM named myVM is selected:
        Step 3: In the pane that appears for the NIC you selected, click IP configurations. Step 4: Click Create public IP address.
        Step 5: In the Create public IP address pane that appears, enter a Name, select an IP address assignment type, a Subscription, a Resource group, and a Location, then click Create, as shown in the following picture:
        References: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-multiple-ip-addresses-portal
        QUESTION 18
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 6
        You need to allow RDP connections over TCP port 3389 to VM1 from the Internet. The solution must prevent connections from the Internet over all other TCP ports.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Create a new network security group Step 2: Select your new network security group.
        Step 3: Select Inbound security rules. Under Add inbound security rule, enter the following Destination: Select Network security group, and then select the security group you created previously. Destination port ranges: 3389
        Protocol: Select TCP
        References: https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-filter-network-traffic
        QUESTION 19
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        Task 5
        You plan to create 100 Azure virtual machines on each of the following three virtual networks:
        VNET1005a VNET1005b VNET1005c
        All the network traffic between the three virtual networks will be routed through VNET1005a.
        You need to create the virtual networks, and then to ensure that all the Azure virtual machines can connect to other virtual machines by using their private IP address. The solution must NOT require any virtual network gateways and must minimize the number of peerings.
        What should you do from the Azure portal before you configure IP routing?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Click Create a resource in the portal.
        Step 2: Enter Virtual network in the Search the Marketplace box at the top of the New pane that appears. Click Virtual network when it appears in the search results.
        Step 3: Select Classic in the Select a deployment model box in the Virtual Network pane that appears, then click Create.
        Step 4: Enter the following values on the Create virtual network (classic) pane and then click Create: Name: VNET1005a
        Address space: 10.0.0.0/16 Subnet name: subnet0 Resource group: Create new
        Subnet address range: 10.0.0.0/24
        Subscription and location: Select your subscription and location.
        Step 5: Repeat steps 3-5 for VNET1005b (10.1.0.0/16, 10.1.0.0/24), and for VNET1005c 10.2.0.0/16, 10.2.0.0/24).
        References: https://docs.microsoft.com/en-us/azure/virtual-network/create-virtual-network-classic
        QUESTION 20
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to
        return to the lab.
        You may now click next to proceed to the lab.
        Task 6
        You plan to create several virtual machines in different availability zones, and then to configure the virtual machines for load balanced connections from the Internet.
        You need to create an IP address resource named ip1006 to support the planned load balancing solution. The solution must minimize costs.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        We should create a public IP address.
        Step 1: At the top, left corner of the portal, select + Create a resource.
        Step 2: Enter public ip address in the Search the Marketplace box. When Public IP address appears in the search results, select it.
        Step 3: Under Public IP address, select Create.
        Step 4: Enter, or select values for the following settings, under Create public IP address, then select Create:
        Name: ip1006 SKU: Basic SKU IP Version: IPv6
        IP address assignment: Dynamic Subscription: Select appropriate Resource group: Select appropriate
        References: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-public-ip-address
        QUESTION 21
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        Task 8
        You need to create a virtual network named VNET1008 that contains three subnets named subnet0, subnet1, and subnet2. The solution must meet the following requirements:
        Connections from any of the subnets to the Internet must be blocked. Connections from the Internet to any of the subnets must be blocked.
        The number of network security groups (NSGs) and NSG rules must be minimized.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Click Create a resource in the portal.
        Step 2: Enter Virtual network in the Search the Marketplace box at the top of the New pane that appears. Click Virtual network when it appears in the search results.
        Step 3: Select Classic in the Select a deployment model box in the Virtual Network pane that appears, then
        click Create.
        Step 4: Enter the following values on the Create virtual network (classic) pane and then click Create: Name: VNET1008
        Address space: 10.0.0.0/16 Subnet name: subnet0 Resource group: Create new
        Subnet address range: 10.0.0.0/24
        Subscription and location: Select your subscription and location.
        Step 5: In the portal, you can create only one subnet when you create a virtual network. Click Subnets (in the SETTINGS section) on the Create virtual network (classic) pane that appears.
        Click +Add on the VNET1008 - Subnets pane that appears.
        Step 6: Enter subnet1 for Name on the Add subnet pane. Enter 10.0.1.0/24 for Address range. Click OK.
        Step 7: Create the third subnet: Click +Add on the VNET1008 - Subnets pane that appears. Enter subnet2 for Name on the Add subnet pane. Enter 10.0.2.0/24 for Address range. Click OK.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/create-virtual-network-classic
        QUESTION 22
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You manage a virtual network named VNet1 that is hosted in the West US Azure region. VNet1 hosts two virtual machines named VM1 and VM2 that run Windows Server.
        You need to inspect all the network traffic from VM1 to VM2 for a period of three hours. Solution: From Azure Network Watcher, you create a connection monitor.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        References: https://azure.microsoft.com/en-us/updates/general-availability-azure-network-watcher-connection-monitor- in-all-public-regions/
        QUESTION 23
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You manage a virtual network named VNet1 that is hosted in the West US Azure region. VNet1 hosts two virtual machines named VM1 and VM2 that run Windows Server.
        You need to inspect all the network traffic from VM1 to VM2 for a period of three hours. Solution: From Azure Network Watcher, you create a packet capture.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Use the Connection Monitor feature of Azure Network Watcher.
        References: https://azure.microsoft.com/en-us/updates/general-availability-azure-network-watcher-connection-monitor- in-all-public-regions/
        QUESTION 24
        HOTSPOT
        Subscription1 contains the virtual machines in the following table.
        In Subscription1, you create a load balancer that has the following configurations: Name: LB1
        SKU: Basic Type: Internal
        Subnet: Subnet12 Virtual network: VNET1
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-standard-overview
        QUESTION 25
        You have an Azure subscription named Subscription1 that contains two Azure virtual networks named VNet1 and VNet2. VNet1 contains a VPN gateway named VPNGW1 that uses static routing. There is a site- to-site VPN connection between your on-premises network and VNet1.
        On a computer named Client1 that runs Windows 10, you configure a point-to-site VPN connection to VNet1.
        You configure virtual network peering between VNet1 and VNet2. You verify that you can connect to VNet2 from the on-premises network. Client1 is unable to connect to VNet2.
        You need to ensure that you can connect Client1 to VNet2. What should you do?
        A. Select Allow gateway transit on VNet2.
        B. Enable BGP on VPNGW1.
        C. Select Allow gateway transit on VNet1.
        D. Download and re-install the VPN client configuration package on Client1.
        Correct Answer: D
        Section: [none]
        Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-point-to-site-routing
        QUESTION 26
        Note: This question is part of a series of questions that present the same scenario. Each question in the series contains a unique solution that might meet the stated goals. Some question sets might have more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these questions will not appear in the review screen.
        You manage a virtual network named VNet1 that is hosted in the West US Azure region. VNet1 hosts two virtual machines named VM1 and VM2 that run Windows Server.
        You need to inspect all the network traffic from VM1 to VM2 for a period of three hours. Solution: From Performance Monitor, you create a Data Collector Set (DCS).
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Use the Connection Monitor feature of Azure Network Watcher.
        References: https://docs.microsoft.com/en-us/azure/network-watcher/network-watcher-monitoring-overview
        QUESTION 27
        HOTSPOT
        You have a virtual network named VNet1 that has the configuration shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: add an address space
        Your IaaS virtual machines (VMs) and PaaS role instances in a virtual network automatically receive a private IP address from a range that you specify, based on the address space of the subnet they are connected to. We need to add the 192.168.1.0/24 address space.
        Box 2: add a network interface
        The 10.2.1.0/24 network exists. We need to add a network interface.
        References: https://docs.microsoft.com/en-us/office365/enterprise/designing-networking-for-microsoft-azure-iaas https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-static-private-ip-arm-pportal
        QUESTION 28
        HOTSPOT
        You have an Azure subscription named Subscription1. Subscription1 contains the virtual machines in the following table.
        Subscription1 contains a virtual network named VNet1 that has the subnets in the following table.
        VM3 has multiple network adapters, including a network adapter named NIC3. IP forwarding is enabled on NIC3. Routing is enabled on VM3.
        You create a route table named RT1 that contains the routes in the following table.
        You apply RT1 to Subnet1 and Subnet2.
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        IP forwarding enables the virtual machine a network interface is attached to:
        Receive network traffic not destined for one of the IP addresses assigned to any of the IP configurations assigned to the network interface.
        Send network traffic with a different source IP address than the one assigned to one of a network interface's IP configurations.
        The setting must be enabled for every network interface that is attached to the virtual machine that receives traffic that the virtual machine needs to forward. A virtual machine can forward traffic whether it has multiple network interfaces or a single network interface attached to it.
        Box 1: Yes
        The routing table allows connections from VM3 to VM1 and VM2. And as IP forwarding is enabled on VM3, VM3 can connect to VM1.
        Box 2: No
        VM3, which has IP forwarding, must be turned on, in order for VM2 to connect to VM1.
        Box 3: Yes
        The routing table allows connections from VM1 and VM2 to VM3. IP forwarding on VM3 allows VM1 to connect to VM2 via VM3.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-udr-overview https://www.quora.com/What-is-IP-forwarding
        QUESTION 29
        You have an Azure subscription that contains the resources in the following table.
        VM1 and VM2 are deployed from the same template and host line-of-business applications accessed by using Remote Desktop.
        You configure the network security group (NSG) shown in the exhibit. (Click the Exhibit tab.)
        You need to prevent users of VM2 and VM2 from accessing websites on the Internet over TCP port 80. What should you do?
        A. Change the DenyWebSites outbound security rule.
        B. Change the Port_80 inbound security rule.
        C. Disassociate the NSG from a network interface.
        D. Associate the NSG to Subnet1.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can associate or dissociate a network security group from a network interface or subnet.
        The NSG has the appropriate rule to block users from accessing the Internet. We just need to associate it with Subnet1.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/manage-network-security-group
        QUESTION 30
        HOTSPOT
        You are creating an Azure load balancer.
        You need to add an IPv6 load balancing rule to the load balancer.
        How should you complete the Azure PowerShell script? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-ipv6-internet-ps
        QUESTION 31
        HOTSPOT
        You have an Azure subscription named Subscription1 that contains a resource group named RG1. In RG1, you create an internal load balancer named LB1 and a public load balancer named LB2.
        You need to ensure that an administrator named Admin1 can manage LB1 and LB2. The solution must follow the principle of least privilege.
        Which role should you assign to Admin1 for each task? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        QUESTION 32
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 7
        You plan to allow connections between the VNET01-USEA2 and VNET01-USWE2 virtual networks.
        You need to ensure that virtual machines can communicate across both virtual networks by using their private IP address. The solution must NOT require any virtual network gateways.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Virtual network peering enables you to seamlessly connect two Azure virtual networks. Once peered, the virtual networks appear as one, for connectivity purposes.
        Peer virtual networks
        Step 1. In the Search box at the top of the Azure portal, begin typing VNET01-USEA2. When VNET01- USEA2 appears in the search results, select it.
        Step 2. Select Peerings, under SETTINGS, and then select + Add, as shown in the following picture:
        Step 3. Enter, or select, the following information, accept the defaults for the remaining settings, and then select OK.
        Name: myVirtualNetwork1-myVirtualNetwork2 (for example) Subscription: elect your subscription.
        Virtual network: VNET01-USWE2 - To select the VNET01-USWE2 virtual network, select Virtual network, then select VNET01-USWE2. You can select a virtual network in the same region or in a different region.
        Now we need to repeat steps 1-3 for the other network VNET01-USWE2:
        Step 4. In the Search box at the top of the Azure portal, begin typing VNET01- USEA2. When VNET01-
        USEA2 appears in the search results, select it.
        Step 5. Select Peerings, under SETTINGS, and then select + Add. References: https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-connect-virtual-networks-portal
        QUESTION 33
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 8
        You plan to host several secured websites on Web01.
        You need to allow HTTPS over TCP port 443 to Web01 and to prevent HTTP over TCP port 80 to Web01. What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You can filter network traffic to and from Azure resources in an Azure virtual network with a network security group. A network security group contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources.
        A network security group contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources.
        Step A: Create a network security group
        A1. Search for and select the resource group for the VM, choose Add, then search for and select Network security group.
        A2. Select Create.
        The Create network security group window opens. A3. Create a network security group
        Enter a name for your network security group.
        Select or create a resource group, then select a location. A4. Select Create to create the network security group.
        Step B: Create an inbound security rule to allows HTTPS over TCP port 443 B1. Select your new network security group.
        B2. Select Inbound security rules, then select Add. B3. Add inbound rule
        B4. Select Advanced.
        From the drop-down menu, select HTTPS.
        You can also verify by clicking Custom and selecting TCP port, and 443. B5. Select Add to create the rule.
        Repeat step B2-B5 to deny TCP port 80
        B6. Select Inbound security rules, then select Add. B7. Add inbound rule
        B8. Select Advanced.
        Clicking Custom and selecting TCP port, and 80. B9. Select Deny.
        Step C: Associate your network security group with a subnet
        Your final step is to associate your network security group with a subnet or a specific network interface.
        C1. In the Search resources, services, and docs box at the top of the portal, begin typing Web01. When the Web01 VM appears in the search results, select it.
        C2. Under SETTINGS, select Networking. Select Configure the application security groups, select the Security Group you created in Step A, and then select Save, as shown in the following picture:
        References: https://docs.microsoft.com/en-us/azure/virtual-network/tutorial-filter-network-traffic
        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message: "Licenses not assigned. License assignment failed for one user."
        You verify that the Azure subscription has the available licenses.
        Requirements Planned Changes
        Humongous Insurance plans to open a new office in Paris. The Paris office will contain 1,000 users who will
        be hired during the next 12 months. All the resources used by the Paris office users will be hosted in Azure.
        Planned Azure AD Infrastructure
        The on-premises Active Directory domain will be synchronized to Azure AD.
        All client computers in the Paris office will be joined to an Azure AD domain.
        Planned Azure Networking Infrastructure
        You plan to create the following networking resources in a resource group named All_Resources:
        Default Azure system routes that will be the only routes used to route traffic
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a separate resource group. The initial configuration of the web apps will be identical. The web administrators have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO) when accessing resources in Azure.
        QUESTION 1
        HOTSPOT
        You are evaluating the name resolution for the virtual machines after the planned implementation of the Azure networking infrastructure.
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Yes
        All client computers in the Paris office will be joined to an Azure AD domain.
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2
        Box 2: Yes
        A virtual network named ClientResources-VNet that will contain one subnet named ClientSubnet
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to the ClientResources-VNet virtual network.
        Box 3: No
        Only VMs in the registration network, here the ClientResources-VNet, will be able to register hostname records.
        References: https://docs.microsoft.com/en-us/azure/dns/private-dns-overview
        Testlet 3 Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Contoso, Ltd. is a consulting company that has a main office in Montreal and two branch offices in Seattle and New York.
        The Montreal office has 2,000 employees. The Seattle office has 1,000 employees. The New York office has 200 employees.
        All the resources used by Contoso are hosted on-premises.
        Contoso creates a new Azure subscription. The Azure Active Directory (Azure AD) tenant uses a domain named contoso.onmicrosoft.com. The tenant uses the P1 pricing tier.
        Existing Environment
        The network contains an Active Directory forest named contoso.com. All domain controllers are configured as DNS servers and host the contoso.com DNS zone.
        Contoso has finance, human resources, sales, research, and information technology departments. Each department has an organizational unit (OU) that contains all the accounts of that respective department. All the user accounts have the department attribute set to their respective department. New users are added frequently.
        Contoso.com contains a user named User1. All the offices connect by using private links.
        Contoso has data centers in the Montreal and Seattle offices. Each data center has a firewall that can be configured as a VPN device.
        All infrastructure servers are virtualized. The virtualization environment contains the servers in the following table.
        Contoso uses two web applications named App1 and App2. Each instance on each web application requires 1GB of memory.
        The Azure subscription contains the resources in the following table.
        The network security team implements several network security groups (NSGs).
        Planned Changes
        Contoso plans to implement the following changes: Deploy Azure ExpressRoute to the Montreal office.
        Migrate the virtual machines hosted on Server1 and Server2 to Azure. Synchronize on-premises Active Directory to Azure Active Directory (Azure AD). Migrate App1 and App2 to two Azure web apps named WebApp1 and WebApp2.
        Technical requirements
        Contoso must meet the following technical requirements:
        Ensure that WebApp1 can adjust the number of instances automatically based on the load and can scale up to five instances.
        Ensure that VM3 can establish outbound connections over TCP port 8080 to the applications servers in the Montreal office.
        Ensure that routing information is exchanged automatically between Azure and the routers in the Montreal office.
        Ensure Azure Multi-Factor Authentication (MFA) for the users in the finance department only. Ensure that webapp2.azurewebsites.net can be accessed by using the name app2.contoso.com Connect the New York office to VNet1 over the Internet by using an encrypted connection.
        Create a workflow to send an email message when the settings of VM4 are modified. Create a custom Azure role named Role1 that is based on the Reader role.
        Minimize costs whenever possible.
        QUESTION 1
        HOTSPOT
        You need to meet the connection requirements for the New York office.
        What should you do? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Create a virtual network gateway and a local network gateway.
        Azure VPN gateway. The VPN gateway service enables you to connect the VNet to the on-premises network through a VPN appliance. For more information, see Connect an on-premises network to a Microsoft Azure virtual network. The VPN gateway includes the following elements:
        Virtual network gateway. A resource that provides a virtual VPN appliance for the VNet. It is responsible for routing traffic from the on-premises network to the VNet.
        Local network gateway. An abstraction of the on-premises VPN appliance. Network traffic from the cloud application to the on-premises network is routed through this gateway.
        Connection. The connection has properties that specify the connection type (IPSec) and the key shared with the on-premises VPN appliance to encrypt traffic.
        Gateway subnet. The virtual network gateway is held in its own subnet, which is subject to various requirements, described in the Recommendations section below.
        Box 2: Configure a site-to-site VPN connection
        On premises create a site-to-site connection for the virtual network gateway and the local network gateway.
        Scenario: Connect the New York office to VNet1 over the Internet by using an encrypted connection. Incorrect Answers:
        Azure ExpressRoute: Established between your network and Azure, through an ExpressRoute partner. This connection is private. Traffic does not go over the internet.
        References: https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/vpn
        Question Set 1
        QUESTION 1
        You have an Azure Active Directory (Azure AD) tenant named contoso.onmicrosoft.com. The User administrator role is assigned to a user named Admin1.
        An external partner has a Microsoft account that uses the user1@outlook.com sign in.
        Admin1 attempts to invite the external partner to sign in to the Azure AD tenant and receives the following error message: “Unable to invite user user1@outlook.com – Generic authorization exception.”
        You need to ensure that Admin1 can invite the external partner to sign in to the Azure AD tenant. What should you do?
        A. From the Roles and administrators blade, assign the Security administrator role to Admin1.
        B. From the Organizational relationships blade, add an identity provider.
        C. From the Custom domain names blade, add a custom domain.
        D. From the Users blade, modify the External collaboration settings.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        References: https://techcommunity.microsoft.com/t5/Azure-Active-Directory/Generic-authorization-exception-inviting- Azure-AD-gests/td-p/274742
        QUESTION 2
        Your company has an Azure Active Directory (Azure AD) tenant named contoso.com that is configured for hybrid coexistence with the on-premises Active Directory domain. The tenant contains the users shown in the following table.
        Whenever possible, you need to enable Azure Multi-Factor Authentication (MFA) for the users in contoso.com.
        Which users should you enable for Azure MFA?
        A. User1 only
        B. User1, User2, and User3 only
        C. User1 and User2 only
        D. User1, User2, User3, and User4
        E. User2 only
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        QUESTION 3
        You have two Azure Active Directory (Azure AD) tenants named contoso.com and fabrikam.com. You have a Microsoft account that you use to sign in to both tenants.
        You need to configure the default sign-in tenant for the Azure portal. What should you do?
        A. From Azure Cloud Shell, run Set-AzureRmSubscription.
        B. From Azure Cloud Shell, run Set-AzureRmContext.
        C. From the Azure portal, configure the portal settings.
        D. From the Azure portal, change the directory.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session. The context includes tenant, subscription, and environment information.
        References: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermcontext
        QUESTION 4
        You have an Azure Active Directory (Azure AD) tenant.
        All administrators must enter a verification code to access the Azure portal.
        You need to ensure that the administrators can access the Azure portal only from your on-premises network.
        What should you configure?
        A. an Azure AD Identity Protection user risk policy.
        B. the multi-factor authentication service settings.
        C. the default for all the roles in Azure AD Privileged Identity Management
        D. an Azure AD Identity Protection sign-in risk policy
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        QUESTION 5
        You have an Active Directory forest named contoso.com.
        You install and configure Azure AD Connect to use password hash synchronization as the single sign-on (SSO) method. Staging mode is enabled.
        You review the synchronization results and discover that the Synchronization Service Manager does not display any sync jobs.
        You need to ensure that the synchronization completes successfully. What should you do?
        A. Run Azure AD Connect and set the SSO method to Pass-through Authentication.
        B. From Synchronization Service Manager, run a full import.
        C. From Azure PowerShell, run Start-AdSyncSyncCycle –PolicyType Initial.
        D. Run Azure AD Connect and disable staging mode.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Staging mode must be disabled. If the Azure AD Connect server is in staging mode, password hash synchronization is temporarily disabled.
        References: https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync- troubleshoot-password-hash-synchronization#no-passwords-are-synchronized-troubleshoot-by-using-the- troubleshooting-task
        QUESTION 6
        You have an Azure Active Directory (Azure AD) tenant named contoso.onmicrosoft.com.
        You hire a temporary vendor. The vendor uses a Microsoft account that has a sign-in of user1@outlook.com.
        You need to ensure that the vendor can authenticate to the tenant by using user1@outlook.com. What should you do?
        A. From the Azure portal, add a custom domain name, create a new Azure AD user, and then specify user1@outlook.com as the username.
        B. From Azure Cloud Shell, run the New-AzureADUser cmdlet and specify the
        –UserPrincipalName user1@outlook.com parameter.
        C. From the Azure portal, add a new guest user, and then specify user1@outlook.com as the email address.
        D. From Windows PowerShell, run the New-AzureADUser cmdlet and specify the
        –UserPrincipalName user1@outlook.com parameter.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        UserPrincipalName - contains the UserPrincipalName (UPN) of this user. The UPN is what the user will use when they sign in into Azure AD. The common structure is @, so for Abby Brown in Contoso.com, the UPN would be AbbyB@contoso.com
        Example:
        To create the user, call the New-AzureADUser cmdlet with the parameter values:
        powershell New-AzureADUser -AccountEnabled $True -DisplayName "Abby Brown" -PasswordProfile
        $PasswordProfile -MailNickName "AbbyB" -UserPrincipalName "AbbyB@contoso.com"
        References: https://docs.microsoft.com/bs-cyrl-ba/powershell/azure/active-directory/new-user-sample?view=azureadps- 2.0
        QUESTION 7
        You have an Azure Active Directory (Azure AD) tenant named contosocloud.onmicrosoft.com. Your company has a public DNS zone for contoso.com.
        You add contoso.com as a custom domain name to Azure AD. You need to ensure that Azure can verify the domain name.
        Which type of DNS record should you create?
        A. MX
        B. SRV
        C. DNSKEY
        D. NSEC
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/dns/dns-web-sites-custom-domain
        QUESTION 8
        You set the multi-factor authentication status for a user named admin1@contoso.com to Enabled. Admin1 accesses the Azure portal by using a web browser.
        Which additional security verifications can Admin1 use when accessing the Azure portal?
        A. a phone call, a text message that contains a verification code, and a notification or a verification code sent from the Microsoft Authenticator app
        B. an app password, a text message that contains a verification code, and a notification sent from the Microsoft Authenticator app
        C. an app password, a text message that contains a verification code, and a verification code sent from the Microsoft Authenticator app
        D. a phone call, an email message that contains a verification code, and a text message that contains an app password
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        QUESTION 9
        DRAG DROP
        You have an Azure Active Directory (Azure AD) tenant that has the initial domain name. You have a domain name of contoso.com registered at a third-party registrar.
        You need to ensure that you can create Azure AD users that have names containing a suffix of @contoso.com.
        Which three actions should you perform in sequence? To answer, move the appropriate cmdlets from the list of cmdlets to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        References: https://docs.microsoft.com/en-us/azure/dns/dns-web-sites-custom-domain
        QUESTION 10
        Your company has a main office in London that contains 100 client computers. Three years ago, you migrated to Azure Active Directory (Azure AD).
        The company’s security policy states that all personal devices and corporate-owned devices must be registered or joined to Azure AD.
        A remote user named User1 is unable to join a personal device to Azure AD from a home network. You verify that other users can join their devices to Azure AD.
        You need to ensure that User1 can join the device to Azure AD. What should you do?
        A. From the Device settings blade, modify the Users may join devices to Azure AD setting.
        B. From the Device settings blade, modify the Maximum number of devices per user setting.
        C. Create a point-to-site VPN from the home network of User1 to Azure.
        D. Assign the User administrator role to User1.
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        The Maximum number of devices setting enables you to select the maximum number of devices that a user can have in Azure AD. If a user reaches this quota, they will not be able to add additional devices until one or more of the existing devices are removed.
        Incorrect Answers:
        A: The Users may join devices to Azure AD setting enables you to select the users who can join devices to Azure AD. Options are All, Selected and None. The default is All.
        C: Azure AD Join enables users to join their devices to Active Directory from anywhere as long as they have connectivity with the Internet.
        References: https://docs.microsoft.com/en-us/azure/active-directory/devices/device-management-azure-portal http://techgenix.com/pros-and-cons-azure-ad-join/
        QUESTION 11
        You have an Azure DNS zone named adatum.com.
        You need to delegate a subdomain named research.adatum.com to a different DNS server in Azure. What should you do?
        A. Create an A record named *.research in the adatum.com zone.
        B. Create a PTR record named research in the adatum.com zone.
        C. Modify the SOA record of adatum.com.
        D. Create an NS record named research in the adatum.com zone.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        You need to create a name server (NS) record for the zone.
        References: https://docs.microsoft.com/en-us/azure/dns/delegate-subdomain
        QUESTION 12
        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform a set of tasks in a live environment. While most functionality will be available to you as it would be in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites) will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can use as much time as you would like to complete each lab. But, you should manage your time appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able to return to the lab.
        You may now click next to proceed to the lab.
        Task 7
        You plan to deploy several Azure virtual machines and to connect them to a virtual network named VNET1007.
        You need to ensure that future virtual machines on VNET1007 can register their name in an internal DNS zone named corp9172795.com. The zone must NOT be hosted on a virtual machine.
        What should you do from Azure Cloud Shell?
        To complete this task, start Azure Cloud Shell and select PowerShell (Linux). Click Show Advanced Settings, and then enter corp9172795n1 in the Storage account text box and File1 in the File share text box. Click Create storage, and then complete the task.
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: New-AzureRMResourceGroup -name MyResourceGroup
        Before you create the DNS zone, create a resource group to contain the DNS zone.
        Step 2: New-AzureRmDnsZone -Name corp9172795.com -ResourceGroupName MyResourceGroup
        A DNS zone is created by using the New-AzureRmDnsZone cmdlet. This creates a DNS zone called corp9172795.com in the resource group called MyResourceGroup.
        References: https://docs.microsoft.com/en-us/azure/dns/dns-getstarted-powershell
        QUESTION 13
        HOTSPOT
        You have an Azure Active Directory (Azure AD) tenant named adatum.com. Adatum.com contains the groups in the following table:
        You create two user accounts that are configured as shown in the following table.
        To which groups do User1 and User2 belong? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Group 1 only First rule applies
        Box 2: Group1 and Group2 only Both membership rules apply.
        References: https://docs.microsoft.com/en-us/sccm/core/clients/manage/collections/create-collections
        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Contoso, Ltd. is a manufacturing company that has offices worldwide. Contoso works with partner organizations to bring products to market.
        Contoso products are manufactured by using blueprint files that the company authors and maintains.
        Existing Environment
        Currently, Contoso uses multiple types of servers for business operations, including the following: File servers
        Domain controllers
        Microsoft SQL Server servers
        Your network contains an Active Directory forest named contoso.com. All servers and client computers are joined to Active Directory.
        You have a public-facing application named App1. App1 is comprised of the following three tiers: A SQL database
        A web front end
        A processing middle tier
        Each tier is comprised of five virtual machines. Users access the web front end by using HTTPS only.
        Requirements Planned Changes
        Contoso plans to implement the following changes to the infrastructure:
        Move all the tiers of App1 to Azure.
        Move the existing product blueprint files to Azure Blob storage.
        Create a hybrid directory to support an upcoming Microsoft Office 365 migration project.
        Technical Requirements
        Contoso must meet the following technical requirements:
        Move all the virtual machines for App1 to Azure.
        Minimize the number of open ports between the App1 tiers.
        Ensure that all the virtual machines for App1 are protected by backups. Copy the blueprint files to Azure over the Internet.
        Ensure that the blueprint files are stored in the archive storage tier. Ensure that partner access to the blueprint files is secured and temporary.
        Prevent user passwords or hashes of passwprds from being stored in Azure. Use unmanaged standard storage for the hard disks of the virtual machines.
        Ensure that when users join devices to Azure Active Directory (Azure AD), the users use a mobile phone to verify their identity
        Minimize administrative effort whenever possible
        User Requirements
        Contoso identifies the following requirements for users:
        Ensure that only users who are part of a group named Pilot can join devices to Azure AD. Designate a new user named Admin1 as the service admin for the Azure subscription.
        Admin1 must receive email alerts regarding service outages.
        Ensure that a new user named User3 can create network objects for the Azure subscription.
        QUESTION 1
        HOTSPOT
        You need to configure the Device settings to meet the technical requirements and the user requirements. Which two settings should you modify? To answer, select the appropriate settings in the answer area.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: Selected
        Only selected users should be able to join devices
        Box 2: Yes
        Require Multi-Factor Auth to join devices.
        From scenario:
        Ensure that only users who are part of a group named Pilot can join devices to Azure AD
        Ensure that when users join devices to Azure Active Directory (Azure AD), the users use a mobile phone to verify their identity.
        QUESTION 2
        You need to recommend a solution to automate the configuration for the finance department users. The solution must meet the technical requirements.
        What should you include in the recommendation?
        A. Azure AD B2C
        B. Azure AD Identity Protection
        C. an Azure logic app and the Microsoft Identity Management (MIM) client
        D. dynamic groups and conditional access policies
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Scenario: Ensure Azure Multi-Factor Authentication (MFA) for the users in the finance department only.
        The recommendation is to use conditional access policies that can then be targeted to groups of users, specific applications, or other conditions.
        References: https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-userstates
        QUESTION 3
        HOTSPOT
        You need to implement Role1.
        Which command should you run before you create Role1? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Testlet 3 Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would like to complete each case. However, there may be additional case studies and sections on this exam. You must manage your time to ensure that you are able to complete all questions included on this exam in the time provided.
        To answer the questions included in a case study, you will need to reference information that is provided in the case study. Case studies might contain exhibits and other resources that provide more information about the scenario that is described in the case study. Each question is independent of the other questions in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers and to make changes before you move to the next section of the exam. After you begin a new section, you cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane to explore the content of the case study before you answer the questions. Clicking these buttons displays information such as business requirements, existing environment, and problem statements. If the case study has an All Information tab, note that the information displayed is identical to the information displayed on the subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message: "Licenses not assigned. License assignment failed for one user."
        You verify that the Azure subscription has the available licenses.
        Requirements Planned Changes
        Humongous Insurance plans to open a new office in Paris. The Paris office will contain 1,000 users who will be hired during the next 12 months. All the resources used by the Paris office users will be hosted in Azure.
        Planned Azure AD Infrastructure
        The on-premises Active Directory domain will be synchronized to Azure AD. All client computers in the Paris office will be joined to an Azure AD domain. Planned Azure Networking Infrastructure
        You plan to create the following networking resources in a resource group named All_Resources:
        Default Azure system routes that will be the only routes used to route traffic
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a separate resource group. The initial configuration of the web apps will be identical. The web administrators have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO) when accessing resources in Azure.
        QUESTION 1
        You need to prepare the environment to meet the authentication requirements.
        Which two actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Install the Active Directory Federation Services (AD FS) role on a domain controller in the Miami office.
        B. Allow inbound TCP port 8080 to the domain controllers in the Miami office.
        C. Join the client computers in the Miami office to Azure AD.
        D. Add http://autologon.microsoftazuread-sso.com to the intranet zone of each client computer in the Miami office.
        E. Install Azure AD Connect on a server in the Miami office and enable Pass-through Authentication.
        Correct Answer: DE Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        D: You can gradually roll out Seamless SSO to your users. You start by adding the following Azure AD URL to all or selected users' Intranet zone settings by using Group Policy in Active Directory: https:// autologon.microsoftazuread-sso.com
        E: Seamless SSO works with any method of cloud authentication - Password Hash Synchronization or Pass-through Authentication, and can be enabled via Azure AD Connect.
        Incorrect Answers:
        A: Seamless SSO is not applicable to Active Directory Federation Services (ADFS). B: Azure AD connect does not port 8080. It uses port 443.
        C: Seamless SSO needs the user's device to be domain-joined, but doesn't need for the device to be Azure AD Joined.
        Scenario: Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO) when accessing resources in Azure.
        Planned Azure AD Infrastructure include: The on-premises Active Directory domain will be synchronized to Azure AD.
        References: https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect-sso-quick-start
