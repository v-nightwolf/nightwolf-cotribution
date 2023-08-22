## Microsoft Azure Administrator AZ-103
---

These are Microsoft Azure Administrator AZ-103 certification questions for experienced professionals.  You will find these questions very helpful in your Microsoft Azure Administrator AZ-103 certification exam. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

 {!inpage-ads.md!}

---

QUESTION 1


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

        Solution: On Subscription1, you assign the Logic App Operator role to the Developers group. Does this meet
                  the goal?

        A. Yes
        B. No

        Correct Answer: B

        Explanation:
        You would need the Logic App Contributor role.
   References:<br>
    - <a href="https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles"
    target="_blank">https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles</a>
    <br>- <a href="https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app"
    target="_blank">https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app</a>



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

   References:<br>
    - <a href="https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles"
    target="_blank">https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles</a>
    <br>- <a href="https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app"
    target="_blank">https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app</a>





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

   References:<br>
    - <a href="https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/search-queries"
    target="_blank">https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/search-queries</a>
    <br>- <a href="https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-portal"
    target="_blank">https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-portal</a>





QUESTION 5




        You have an Azure subscription named Subscription1. Subscription1 contains the resource groups in the
        following table.
        RG1 has a web app named WebApp1. WebApp1 is located in West Europe. You move WebApp1 to RG2.
        What is the effect of the move?

        A. The App Service plan for WebApp1 moves to North Europe. Policy2 applies to WebApp1.
        B. The App Service plan for WebApp1 remains in West Europe. Policy2 applies to WebApp1.
        C. The App Service plan for WebApp1 moves to North Europe. Policy1 applies to WebApp1.
        D. The App Service plan for WebApp1 remains in West Europe. Policy1 applies to WebApp1.

        Correct Answer: B Section: [none] Explanation

        Explanation:
        You can move an app to another App Service plan, as long as the source plan and the target plan are in
        the same resource group and geographical region.
        The region in which your app runs is the region of the App Service plan it's in. However, you cannot change
        an App Service plan's region.

   References:<br>
    - <a href="https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage"
    target="_blank">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage</a>



QUESTION 6




        You have an Azure subscription that contains a resource group named RG1. RG1 contains 100 virtual machines.
        Your company has three cost centers named Manufacturing, Sales, and Finance. You need to associate each
        virtual machine to a specific cost center.
        What should you do?

        A. Configure locks for the virtual machine.
        B. Add an extension to the virtual machines.
        C. Assign tags to the virtual machines.
        D. Modify the inventory settings of the virtual machine.

        Correct Answer: C Section: [none] Explanation

        Explanation/Reference:
        References:
        https://docs.microsoft.com/en-us/azure/billing/billing-getting-started
        https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-using-tags


QUESTION 7



        Note: This question is part of a series of questions that present the same scenario. Each question in the
        series contains a unique solution that might meet the stated goals. Some question sets might have more
        than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these
        questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1
        contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1.
        Solution: From the Subscriptions blade, you select the subscription, and then click Programmatic deployment.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:


QUESTION 8



        Note: This question is part of a series of questions that present the same scenario. Each question in the
        series contains a unique solution that might meet the stated goals. Some question sets might have more
        than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these
        questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1
        contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1.
        Solution: From the Subscriptions blade, you select the subscription, and then click Resource providers. Does
        this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:


QUESTION 9



        Note: This question is part of a series of questions that present the same scenario. Each question
        in the series contains a unique solution that might meet the stated goals. Some question sets might have
        more than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these
        questions will not appear in the review screen.
        You have an Azure subscription named Subscription1. Subscription1 contains a resource group named RG1. RG1
        contains resources that were deployed by using templates.
        You need to view the date and time when the resources were created in RG1. Solution: From the RG1 blade,
        you click Automation script.
        Does this meet the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:


QUESTION 10



        HOTSPOT
        You have an Azure subscription.
        You plan to use Azure Resource Manager templates to deploy 50 Azure virtual machines that will be part of
        the same availability set.
        You need to ensure that as many virtual machines as possible are available if the fabric fails or during
        servicing.
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
        Increasing the update domain (platformUpdateDomainCount) helps with capacity and availability planning
        when the platform reboots nodes. A higher number for the pool (20 is max) means that fewer of their nodes
        in any given availability set would be rebooted at once.
        References:
        https://www.itprotoday.com/microsoft-azure/check-if-azure-region-supports-2-or-3-fault-domains-managed- disks
        https://github.com/Azure/acs-engine/issues/1030


QUESTION 11



        HOTSPOT
        You have an Azure subscription named Subscription1 that has a subscription ID of c276fc76-9cd4-44c9-
        99a7-4fd71546436e.
        You need to create a custom RBAC role named CR1 that meets the following requirements: Can be assigned
        only to the resource groups in Subscription1
        Prevents the management of the access permissions for the resource groups
        Allows the viewing, creating, modifying, and deleting of resource within the resource groups
        What should you specify in the assignable scopes and the permission elements of the definition of CR1? To
        answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        References:
        https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles
        https://docs.microsoft.com/en-us/azure/role-based-access-control/resource-provider-
        operations#microsoftresources


QUESTION 12



        HOTSPOT
        You have an Azure Active Directory (Azure AD) tenant that contains three global administrators named Admin1,
        Admin2, and Admin3.
        The tenant is associated to an Azure subscription. Access control for the subscription is configured as
        shown in the Access control exhibit. (Click the Exhibit tab.)
        You sign in to the Azure portal as Admin1 and configure the tenant as shown in the Tenant exhibit. (Click
        the Exhibit tab.)
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



        Note: This question is part of a series of questions that present the same scenario. Each question in the
        series contains a unique solution that might meet the stated goals. Some question sets might have more
        than one correct solution, while others might not have a correct solution.
        After you answer a question in this section, you will NOT be able to return to it. As a result, these
        questions will not appear in the review screen.
        You have an Azure Active Directory (Azure AD) tenant named Adatum and an Azure Subscription named
        Subscription1. Adatum contains a group named Developers. Subscription1 contains a resource group named Dev.
        You need to provide the Developers group with the ability to create Azure logic apps in the Dev resource group.
        Solution: On Subscription1, you assign the DevTest Labs User role to the Developers group. Does this meet
        the goal?
        A. Yes
        B. No
        Correct Answer: B Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        DevTest Labs User role only lets you connect, start, restart, and shutdown virtual machines in your Azure
        DevTest Labs.
        The Logic App Contributor role lets you manage logic app, but not access to them. It provides access to
        view, edit, and update a logic app.
        References: https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles
        https://docs.microsoft.com/en-us/azure/logic-apps/logic-apps-securing-a-logic-app


QUESTION 15



        You have an Azure Active Directory (Azure AD) tenant that contains 5,000 user accounts. You create a new
        user account named AdminUser1.
        You need to assign the User administrator administrative role to AdminUser1. What should you do from the
        user account properties?
        A. From the Directory role blade, modify the directory role.
        B. From the Licenses blade, assign a new license.
        C. From the Groups blade, invite the user account to a new group.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Assign a role to a user
        1. Sign in to the Azure portal with an account that's a global admin or privileged role admin for the
        directory.
        2. Select Azure Active Directory, select Users, and then select a specific user from the list.
        3. For the selected user, select Directory role, select Add role, and then pick the appropriate admin
        roles from the Directory roles list, such as Conditional access administrator.
        4. Press Select to save.
        References:
        https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-users-assign-role-
        azure-portal


QUESTION 16



        HOTSPOT
        You have an Azure subscription named Subscription1.
        You plan to deploy an Ubuntu Server virtual machine named VM1 to Subscription1.
        You need to perform a custom deployment of the virtual machine. A specific trusted root certification
        authority (CA) must be added during the deployment.
        What should you do? To answer, select the appropriate options in the answer area.
        NOTE: Each correct selection is worth one point.

        Explanation:
        Box 1: Cloud-init.txt
        Cloud-init.txt is used to customize a Linux VM on first boot up. It can be used to install packages and
        write files, or to configure users and security. No additional steps or agents are required to apply your
        configuration.
        Box 2: The az vm create command
        Once Cloud-init.txt has been created, you can deploy the VM with az vm create cmdlet, sing the --custom-
        data parameter to provide the full path to the cloud-init.txt file.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-automate-vm-deployment


QUESTION 17



        You have an Azure subscription named Subscription1. In Subscription1, you create an alert rule named Alert1.
        The Alert1 action group is configured as shown in the following exhibit.
        Alert1 alert criteria is triggered every minute.
        Use the drop-down menus to select the answer choice that completes each statement based on the information
        presented in the graphic.
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
        Note: Rate limiting is a suspension of notifications that occurs when too many are sent to a particular
        phone number, email address or device. Rate limiting ensures that alerts are manageable and actionable.
        The rate limit thresholds are:
        SMS: No more than 1 SMS every 5 minutes. Voice: No more than 1 Voice call every 5 minutes. Email: No more
        than 100 emails in an hour.
        Other actions are not rate limited.
        References:
        https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/monitoring-and-diagnostics/monitoring-
        overview-alerts.md


        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would
        like to complete each case. However, there may be additional case studies and sections on this exam. You
        must manage your time to ensure that you are able to complete all questions included on this exam in the
        time provided.
        To answer the questions included in a case study, you will need to reference information that is provided
        in the case study. Case studies might contain exhibits and other resources that provide more information
        about the scenario that is described in the case study. Each question is independent of the other questions
        in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers
        and to make changes before you move to the next section of the exam. After you begin a new section, you
        cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane
        to explore the content of the case study before you answer the questions. Clicking these buttons displays
        information such as business requirements, existing environment, and problem statements. If the case study has
        an All Information tab, note that the information displayed is identical to the information displayed on the
        subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office
        has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional
        level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a
        dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some
        of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message:
        "Licenses not assigned. License assignment failed for one user."
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
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual
        network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways
        setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to
        the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows
        Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a
        separate resource group. The initial configuration of the web apps will be identical. The web administrators
        have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from
        the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO)
        when accessing resources in Azure.


QUESTION 18



        You need to resolve the licensing issue before you attempt to assign the license again. What should you do?
        A. From the Groups blade, invite the user accounts to a new group.
        B. From the Profile blade, modify the usage location.
        C. From the Directory role blade, modify the directory role.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        License cannot be assigned to a user without a usage location specified.
        Scenario: Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message:
        "Licenses not assigned. License agreement failed for one user."
        You verify that the Azure subscription has the available licenses.


QUESTION 19



        You need to resolve the Active Directory issue. What should you do?
        A. Run the IdFix tool then use the Update actions.
        B. From Active Directory Domains and Trusts, modify the list of UPN suffixes.
        C. From Azure AD Connect, modify the outbound synchronization rule.
        D. From Active Directory Users and Computers, select the user accounts and then modify the UPN suffix value.
        Correct Answer: A Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        IdFix is used to perform discovery and remediation of identity objects and their attributes in an on-premises
        Active Directory environment in preparation for migration to Azure Active Directory. IdFix is intended
        for the Active Directory administrators responsible for directory synchronization with Azure Active Directory.
        Scenario: Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some
        of the characters are unsupported in Azure AD.
        References: https://www.microsoft.com/en-us/download/details.aspx?id=36832


QUESTION 20



        You need to define a custom domain name for Azure AD to support the planned infrastructure. Which domain
        name should you use?
        A. ad.humongousinsurance.com
        B. humingousinsurance.onmicrosoft.com
        C. humongousinsurance.com
        D. humongousinsurance.local
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Every Azure AD directory comes with an initial domain name in the form of domainname.onmicrosoft.com. The
        initial domain name cannot be changed or deleted, but you can add your corporate domain name to Azure
        AD as well. For example, your organization probably has other domain names used to do business and users
        who sign in using your corporate domain name. Adding custom domain names to Azure AD allows you to assign
        user names in the directory that are familiar to your users, such as ‘alice@contoso.com.’ instead of
        'alice@domain name.onmicrosoft.com'.
        Scenario:
        Network Infrastructure: Each office has a local data center that contains all the servers for that
        office. Each office has a dedicated connection to the Internet.
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com
        Planned Azure AD Infrastructure: The on-premises Active Directory domain will be synchronized to Azure AD.
        References: https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/add-custom-domain
        Question Set 1


QUESTION 21



        You plan to use the Azure Import/Export service to copy files to a storage account.
        Which two files should you create before you prepare the drives for the import job? Each correct answer
        presents part of the solution.
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
        E: Modify the dataset.csv file in the root folder where the tool resides. Depending on whether you want
        to import a file or folder or both, add entries in the dataset.csv file
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-import-export-data-to-files


QUESTION 22



        DRAG DROP
        You have an on-premises file server named Server1 that runs Windows Server 2016. You have an Azure
        subscription that contains an Azure file share.
        You deploy an Azure File Sync Storage Sync Service, and you create a sync group. You need to synchronize
        files from Server1 to Azure.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the list
        of actions to the answer area and arrange them in the correct order.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Install the Azure File Sync agent on Server1
        The Azure File Sync agent is a downloadable package that enables Windows Server to be synced with an Azure
        file share
        Step 2: Register Server1.
        Register Windows Server with Storage Sync Service
        Registering your Windows Server with a Storage Sync Service establishes a trust relationship between your
        server (or cluster) and the Storage Sync Service.
        Step 3: Add a server endpoint
        Create a sync group and a cloud endpoint.
        A sync group defines the sync topology for a set of files. Endpoints within a sync group are kept in sync
        with each other. A sync group must contain one cloud endpoint, which represents an Azure file share and
        one or more server endpoints. A server endpoint represents a path on registered server.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-deployment-guide


QUESTION 23



        You create an Azure Storage account named contosostorage. You plan to create a file share named data.
        Users need to map a drive to the data file share from home computers that run Windows 10. Which outbound
        port should you open between the home computers and the data file share?
        A. 80
        B. 443
        C. 445
        D. 3389
        Correct Answer: C Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Ensure port 445 is open: The SMB protocol requires TCP port 445 to be open; connections will fail if port
        445 is blocked.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows


QUESTION 24



        HOTSPOT
        You have several Azure virtual machines on a virtual network named VNet1. You configure an Azure Storage
        account as shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information
        presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: always
        Endpoint status is enabled.
        Box 2: Never
        After you configure firewall and virtual network settings for your storage account, select Allow trusted
        Microsoft services to access this storage account as an exception to enable Azure Backup service to access
        the network restricted storage account.
        Reference: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-windows
        https://azure.microsoft.com/en-us/blog/azure-backup-now-supports-storage-accounts-secured-with-azure-
        storage-firewalls-and-virtual-networks/


QUESTION 25



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


QUESTION 26



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed: Azure Username:
        XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796


        Task 2
        You plan to store media files in the rg1lod9172796 storage account.
        You need to configure the storage account to store the media files. The solution must ensure that only
        users who have access keys can download the media files and that the files are accessible only over HTTPS.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        We should create an Azure file share.
        Step 1: In the Azure portal, select All services. In the list of resources, type Storage Accounts. As you
        begin typing, the list filters based on your input. Select Storage Accounts.
        On the Storage Accounts window that appears. Step 2: Locate the rg1lod9172796 storage account.
        Step 3: On the storage account page, in the Services section, select Files.
        Step 4: On the menu at the top of the File service page, click + File share. The New file share page
        drops down.
        Step 5: In Name type myshare. Click OK to create the Azure file share. References:
        https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-use-files-portal


QUESTION 27



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab.

        Task 1
        You plan to migrate a large amount of corporate data to Azure Storage and to back up files stored on old
        hardware to Azure Storage.
        You need to create a storage account named corpdata9172795n1 in the corpdatalod9172795 resource group. The
        solution must meet the following requirements:
        Corpdata9172795n1 must be able to host the virtual disk files for Azure virtual machines. The cost of
        accessing the files must be minimized.
        Replication costs must be minimized.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: In the Azure portal, click All services. In the list of resources, type Storage Accounts. As you
        begin typing, the list filters based on your input. Select Storage Accounts.
        Step 2: On the Storage Accounts window that appears, choose Add. Step 3: Select the subscription in which
        to create the storage account. Step 4: Under the Resource group field, select corpdatalod9172795.
        Step 5: Enter a name for your storage account: corpdata9172795n1
        Step 6: For Account kind select: General-purpose v2 accounts (recommended for most scenarios) General-purpose
        v2 accounts is recommended for most scenarios. . General-purpose v2 accounts deliver the lowest per-gigabyte
        capacity prices for Azure Storage, as well as industry-competitive transaction
        prices.
        Step 7: For replication select: Read-access geo-redundant storage (RA-GRS)
        Read-access geo-redundant storage (RA-GRS) maximizes availability for your storage account. RA-GRS provides
        read-only access to the data in the secondary location, in addition to geo-replication across two regions.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account
        https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview


QUESTION 28



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab.
        Task 2
        You plan to move backup files and documents from an on-premises Windows file server to Azure Storage. The
        backup files will be stored as blobs.
        You need to create a storage account named corpdata9172795n2. The solution must meet the following
        requirements:
        Ensure that the documents are accessible via drive mappings from Azure virtual machines that run Windows
        Server 2016.
        Provide the highest possible redundancy for the documents. Minimize storage access costs.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: In the Azure portal, click All services. In the list of resources, type Storage Accounts. As you
        begin typing, the list filters based on your input. Select Storage Accounts.
        Step 2: On the Storage Accounts window that appears, choose Add.
        Step 3: Select the subscription in which to create the storage account.
        Step 4: Under the Resource group field, select Create New. Create a new Resource
        Step 5: Enter a name for your storage account: corpdata9172795n2
        Step 6: For Account kind select: General-purpose v2 accounts (recommended for most scenarios) General-purpose
        v2 accounts is recommended for most scenarios. General-purpose v2 accounts deliver the lowest per-gigabyte
        capacity prices for Azure Storage, as well as industry-competitive transaction prices.
        Step 7: For replication select: Read-access geo-redundant storage (RA-GRS)
        Read-access geo-redundant storage (RA-GRS) maximizes availability for your storage account. RA-GRS provides
        read-only access to the data in the secondary location, in addition to geo-replication across two regions.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account
        https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview


QUESTION 29



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
        The Azure File Sync agent is a downloadable package that enables Windows Server to be synced with an Azure
        file share
        Step 2 (B): Register Server1.
        Register Windows Server with Storage Sync Service
        Registering your Windows Server with a Storage Sync Service establishes a trust relationship between your
        server (or cluster) and the Storage Sync Service.
        Step 3 (C): Create a sync group and a cloud endpoint.
        A sync group defines the sync topology for a set of files. Endpoints within a sync group are kept in sync
        with each other. A sync group must contain one cloud endpoint, which represents an Azure file share and
        one or more server endpoints. A server endpoint represents a path on registered server.
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-deployment-guide


QUESTION 30



        DRAG DROP
        You have an Azure subscription named Subscription1.
        You create an Azure Storage account named contosostorage, and then you create a file share named data.
        Which UNC path should you include in a script that references files from the data file share? To answer,
        drag the appropriate values to the correct targets. Each value may be used once, more than once, or not
        at all. You may need to drag the split bar between panes or scroll to view content.
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


QUESTION 31



        DRAG DROP
        You have an Azure subscription that contains a storage account.
        You have an on-premises server named Server1 that runs Windows Server 2016. Server1 has 2 TB of data.
        You need to transfer the data to the storage account by using the Azure Import/Export service.
        In which order should you perform the actions? To answer, move all actions from the list of actions to
        the answer area and arrange them in the correct order.
        NOTE: More than one order of answer choices is correct. You will receive credit for any of the correct
        orders you select.
        Select and Place:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        At a high level, an import job involves the following steps:
        Step 1: Attach an external disk to Server1 and then run waimportexport.exe
        Determine data to be imported, number of drives you need, destination blob location for your data in
        Azure storage.
        Use the WAImportExport tool to copy data to disk drives. Encrypt the disk drives with BitLocker.
        Step 2: From the Azure portal, create an import job.
        Create an import job in your target storage account in Azure portal. Upload the drive journal files.
        Step 3: Detach the external disks from Server1 and ship the disks to an Azure data center. Provide the
        return address and carrier account number for shipping the drives back to you. Ship the disk drives to
        the shipping address provided during job creation.
        Step 4: From the Azure portal, update the import job
        Update the delivery tracking number in the import job details and submit the import job. The drives are
        received and processed at the Azure data center.
        The drives are shipped using your carrier account to the return address provided in the import job.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-import-export-service


QUESTION 32



        You have the Azure virtual machines shown in the following table.
        You have a Recovery Services vault that protects VM1 and VM2. You need to protect VM3 and VM4 by using
        Recovery Services. What should you do first?
        A. Create a new backup policy.
        B. Configure the extensions for VM3 and VM4.
        C. Create a storage account.
        D. Create a new Recovery Services vault.
        Correct Answer: D Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        A Recovery Services vault is a storage entity in Azure that houses data. The data is typically copies of
        data, or configuration information for virtual machines (VMs), workloads, servers, or workstations. You
        can use Recovery Services vaults to hold backup data for various Azure services
        References: https://docs.microsoft.com/en-us/azure/site-recovery/azure-to-azure-tutorial-enable-replication


QUESTION 33



        HOTSPOT
        You have an Azure subscription named Subscription1 that is associated to an Azure Active Directory (Azure
        AD) tenant named AAD1.
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
        With the latest update to Azure Backup, customers can retain their data for up to 99 years in Azure. Note: A
        backup policy defines a matrix of when the data snapshots are taken, and how long those snapshots are retained.
        The backup policy interface looks like this:
        References: https://docs.microsoft.com/en-us/azure/backup/backup-azure-files
        https://docs.microsoft.com/en-us/azure/backup/backup-azure-vms-first-look-arm#defining-a-backup-policy
        https://blogs.microsoft.com/firehose/2015/02/16/february-update-to-azure-backup-includes-data-retention-
        up-to-99-years-offline-backup-and-more/


QUESTION 34



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


QUESTION 35



        HOTSPOT
        You have Azure Storage accounts as shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information
        presented in the graphic.
        NOTE: Each correct selection is worth one point.
        Hot Area:
        Correct Answer:
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Box 1: storageaccount1 and storageaccount2 only Box 2: All the storage accounts
        Note: The three different storage account options are: General-purpose v2 (GPv2) accounts, General-
        purpose v1 (GPv1) accounts, and Blob storage accounts.
        General-purpose v2 (GPv2) accounts are storage accounts that support all of the latest features for blobs,
        files, queues, and tables.
        Blob storage accounts support all the same block blob features as GPv2, but are limited to supporting only
        block blobs.
        General-purpose v1 (GPv1) accounts provide access to all Azure Storage services, but may not have the
        latest features or the lowest per gigabyte pricing.
        References: https://docs.microsoft.com/en-us/azure/storage/common/storage-account-options


QUESTION 36



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796


        Task 1

        You plan to prevent users from accidentally deleting blob data from Azure.
        You need to ensure that administrators can recover any blob data that is deleted accidentally from the
        storagelod9272261 storage account for 14 days after the deletion occurred.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Task A: Create a Recovery Services vault (if a vault already exists skip this task, go to Task B below)
        A1. From Azure Portal, On the Hub menu, click All services and in the list of resources, type Recovery
        Services and click Recovery Services vaults.
        If there are recovery services vaults in the subscription, the vaults are listed. A2. On the Recovery
        Services vaults menu, click Add.
        A3. The Recovery Services vault blade opens, prompting you to provide a Name, Subscription, Resource group,
        and Location
        Task B. Create a backup goal
        B1. On the Recovery Services vault blade (for the vault you just created), in the Getting Started section,
        click Backup, then on the Getting Started with Backup blade, select Backup goal.
        The Backup Goal blade opens. If the Recovery Services vault has been previously configured, then the Backup
        Goal blades opens when you click Backup on the Recovery Services vault blade.
        B2. From the Where is your workload running? drop-down menu, select Azure.
        B3. From the What do you want to backup? menu, select Blob Storage, and click OK. B4. Finish the Wizard.
        Task C. create a backup schedule
        C1. Open the Microsoft Azure Backup agent. You can find it by searching your machine for Microsoft Azure
        Backup.
        C2. In the Backup agent's Actions pane, click Schedule Backup to launch the Schedule Backup Wizard.
        C3. On the Getting started page of the Schedule Backup Wizard, click Next. C4. On the Select Items to
        Backup page, click Add Items.
        The Select Items dialog opens.
        C5. Select Blob Storage you want to protect, and then click OK. C6. In the Select Items to Backup page,
        click Next.
        On the Specify Backup Schedule page, specify Schedule a backup every day, and click Next.
        C7. On the Select Retention Policy page, set it to 14 days, and click Next.
        C8. Finish the Wizard.
        References: https://docs.microsoft.com/en-us/azure/backup/backup-configure-vault


QUESTION 37



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time
        appropriately to ensure that you are able to complete the lab(s) and all other sections of the exam in
        the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796
        Task 2
        Your company plans to store several documents on a public website.
        You need to create a container named bios that will host the documents in the storagelod9272261 storage
        account. The solution must ensure anonymous access and must ensure that users can browse folders in the
        container.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Azure portal create public container
        To create a container in the Azure portal, follow these steps:
        Step 1: Navigate to your new storage account in the Azure portal.
        Step 2: In the left menu for the storage account, scroll to the lob service section, then select Blobs. Select
        the + Container button.
        Type a name for your new container: bios
        Set the level of public access to the container: Select anonymous access.
        Step 3: Select OK to create the container. References:
        https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-portal


QUESTION 38



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796

        Task 3
        Your company plans to host in Azure the source files of several line-of-business applications.
        You need to create an Azure file share named corpsoftware in the storagelod9272261 storage account. The
        solution must ensure that corpsoftware can store only up to 250 GB of data.
        What should you do from the Azure portal?
        Correct Answer: See explanation below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Go to the Storage Account blade on the Azure portal:
        Step 2: Click on add File Share button:
        Step 3: Provide Name (storagelod9272261) and Quota (250 GB).
        References: https://docs.microsoft.com/en-us/azure/storage/files/storage-how-to-create-file-share


QUESTION 39



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796

        Task 6
        You recently created a virtual machine named Web01.
        You need to attach a new 80-GB standard data disk named Web01-Disk1 to Web01. What should you do from the
        Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Add a data disk
        Step 1: In the Azure portal, from the menu on the left, select Virtual machines. Step 2: Select the Web01
        virtual machine from the list.
        Step 3: On the Virtual machine page, , in Essentials, select Disks.
        Step 4: On the Disks page, select the Web01-Disk1 from the list of existing disks. Step 5: In the Disks
        pane, click + Add data disk.
        Step 6: Click the drop-down menu for Name to view a list of existing managed disks accessible to your
        Azure subscription. Select the managed disk Web01-Disk1 to attach:
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal

        Testlet 2
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would
        like to complete each case. However, there may be additional case studies and sections on this exam. You
        must manage your time to ensure that you are able to complete all questions included on this exam in the
        time provided.
        To answer the questions included in a case study, you will need to reference information that is provided
        in the case study. Case studies might contain exhibits and other resources that provide more information
        about the scenario that is described in the case study. Each question is independent of the other questions
        in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers
        and to make changes before you move to the next section of the exam. After you begin a new section, you
        cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane
        to explore the content of the case study before you answer the questions. Clicking these buttons displays
        information such as business requirements, existing environment, and problem statements. If the case study has
        an All Information tab, note that the information displayed is identical to the information displayed on the
        subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Contoso, Ltd. is a manufacturing company that has offices worldwide. Contoso works with partner organizations
        to bring products to market.
        Contoso products are manufactured by using blueprint files that the company authors and maintains.
        Existing Environment
        Currently, Contoso uses multiple types of servers for business operations, including the following:
        File servers
        Domain controllers
        Microsoft SQL Server servers
        Your network contains an Active Directory forest named contoso.com. All servers and client computers are
        joined to Active Directory.
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
        Ensure that all the virtual machines for App1 are protected by backups. Copy the blueprint files to Azure
        over the Internet.
        Ensure that the blueprint files are stored in the archive storage tier. Ensure that partner access to the
        blueprint files is secured and temporary.
        Prevent user passwords or hashes of passwprds from being stored in Azure. Use unmanaged standard storage
        for the hard disks of the virtual machines.
        Ensure that when users join devices to Azure Active Directory (Azure AD), the users use a mobile phone to
        verify their identity
        Minimize administrative effort whenever possible
        User Requirements
        Contoso identifies the following requirements for users:
        Ensure that only users who are part of a group named Pilot can join devices to Azure AD. Designate a new
        user named Admin1 as the service admin for the Azure subscription.
        Admin1 must receive email alerts regarding service outages.
        Ensure that a new user named User3 can create network objects for the Azure subscription.


QUESTION 40



        HOTSPOT
        You need to identify the storage requirements for Contoso.
        For each of the following statements, select Yes if the statement is true. Otherwise, select No.
        NOTE: Each correct selection is worth one point.

        Explanation:
        Box 1: Yes
        Contoso is moving the existing product blueprint files to Azure Blob storage.
        Use unmanaged standard storage for the hard disks of the virtual machines. We use Page Blobs for these. Box
        2: No
        Box 3: No


QUESTION 41



        You need to move the blueprint files to Azure. What should you do?
        A. Use Azure Storage Explorer to copy the files.
        B. Use the Azure Import/Export service.
        C. Generate a shared access signature (SAS). Map a drive, and then copy the files by using File Explorer.
        D. Generate an access key. Map a drive, and then copy the files by using File Explorer.

        Correct Answer: A 

        Azure Storage Explorer is a free tool from Microsoft that allows you to work with Azure Storage data on
        Windows, macOS, and Linux. You can use it to upload and download data from Azure blob storage.
        Scenario:
        Planned Changes include: move the existing product blueprint files to Azure Blob storage. Technical
        Requirements include: Copy the blueprint files to Azure over the Internet.
        References:
        https://docs.microsoft.com/en-us/azure/machine-learning/team-data-science-process/move-data-to-azure-
        blob-using-azure-storage-explorer


QUESTION 42



        You need to implement a backup solution for App1 after the application is moved. What should you create first?
        A. a recovery plan
        B. a Recovery Services vault
        C. an Azure Backup Server
        D. a backup policy

        Correct Answer: B 

        Explanation:
        A Recovery Services vault is a logical container that stores the backup data for each protected resource,
        such as Azure VMs. When the backup job for a protected resource runs, it creates a recovery point inside
        the Recovery Services vault.
        Scenario:
        There are three application tiers, each with five virtual machines. Move all the virtual machines for App1
        to Azure.
        Ensure that all the virtual machines for App1 are protected by backups.
        References: https://docs.microsoft.com/en-us/azure/backup/quick-backup-vm-portal
        Testlet 3
        Case study
        This is a case study. Case studies are not timed separately. You can use as much exam time as you would
        like to complete each case. However, there may be additional case studies and sections on this exam. You
        must manage your time to ensure that you are able to complete all questions included on this exam in the
        time provided.
        To answer the questions included in a case study, you will need to reference information that is provided
        in the case study. Case studies might contain exhibits and other resources that provide more information
        about the scenario that is described in the case study. Each question is independent of the other questions
        in this case study.
        At the end of this case study, a review screen will appear. This screen allows you to review your answers
        and to make changes before you move to the next section of the exam. After you begin a new section, you
        cannot return to this section.
        To start the case study
        To display the first question in this case study, click the Next button. Use the buttons in the left pane
        to explore the content of the case study before you answer the questions. Clicking these buttons displays
        information such as business requirements, existing environment, and problem statements. If the case study has
        an All Information tab, note that the information displayed is identical to the information displayed on the
        subsequent tabs. When you are ready to answer a question, click the Question button to return to the question.
        Overview
        Humongous Insurance is an insurance company that has three offices in Miami, Tokyo and Bangkok. Each office
        has 5.000 users.
        Existing Environment
        Active Directory Environment
        Humongous Insurance has a single-domain Active Directory forest named humongousinsurance.com. The functional
        level of the forest is Windows Server 2012.
        You recently provisioned an Azure Active Directory (Azure AD) tenant.
        Network Infrastructure
        Each office has a local data center that contains all the servers for that office. Each office has a
        dedicated connection to the Internet.
        Each office has several link load balancers that provide access to the servers.
        Active Directory Issue
        Several users in humongousinsurance.com have UPNs that contain special characters. You suspect that some
        of the characters are unsupported in Azure AD.
        Licensing Issue
        You attempt to assign a license in Azure to several users and receive the following error message:
        "Licenses not assigned. License assignment failed for one user."
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
        A virtual network named Paris-VNet that will contain two subnets named Subnet1 and Subnet2 A virtual
        network named ClientResources-VNet that will contain one subnet named ClientSubnet
        A virtual network named AllOffices-VNet that will contain two subnets named Subnet3 and Subnet4
        You plan to enable peering between Paris-VNet and AllOffices-VNet. You will enable the Use remote gateways
        setting for the Paris-VNet peerings.
        You plan to create a private DNS zone named humongousinsurance.local and set the registration network to
        the ClientResources-VNet virtual network.
        Planned Azure Computer Infrastructure
        Each subnet will contain several virtual machines that will run either Windows Server 2012 R2, Windows
        Server 2016, or Red Hat Linux.
        Department Requirements
        Humongous Insurance identifies the following requirements for the company's departments:
        Web administrators will deploy Azure web apps for the marketing department. Each web app will be added to a
        separate resource group. The initial configuration of the web apps will be identical. The web administrators
        have permission to deploy web apps to resource groups.
        During the testing phase, auditors in the finance department must be able to review all Azure costs from
        the past week.
        Authentication Requirements
        Users in the Miami office must use Azure Active Directory Seamless Single Sign-on (Azure AD Seamless SSO)
        when accessing resources in Azure.


QUESTION 43


        You need to prepare the environment to ensure that the web administrators can deploy the web apps as
        quickly as possible.
        Which three actions should you perform in sequence? To answer, move the appropriate actions from the list
        of actions to the answer area and arrange them in the correct order.

        Explanation:
        Step 1:
        First you create a storage account using the Azure portal.
        Step 2:
        Select Automation options at the bottom of the screen. The portal shows the template on the Template
        tab. Add the storage account to the library.
        Step 3:
        Share the template.
        Scenario: Web administrators will deploy Azure web apps for the marketing department. Each web app will
        be added to a separate resource group. The initial configuration of the web apps will be identical. The
        web administrators have permission to deploy web apps to resource groups.
        References: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-quickstart-create-
        templates-use-the-portal
        Question Set 1


QUESTION 44



        You plan to automate the deployment of a virtual machine scale set that uses the Windows Server 2016
        Datacenter image.
        You need to ensure that when the scale set virtual machines are provisioned, they have web server components
        installed.
        Which two actions should you perform? Each correct answer presents part of the solution.
        NOTE: Each correct selection is worth one point.
        A. Modify the extensionProfile section of the Azure Resource Manager template.
        B. Create an automation account.
        C. Upload a configuration script.
        D. Create a new virtual machine scale set in the Azure portal.
        E. Create an Azure policy.

        Correct Answer: A & D 

        Explanation:
        Virtual Machine Scale Sets can be used with the Azure Desired State Configuration (DSC) extension
        handler. Virtual machine scale sets provide a way to deploy and manage large numbers of virtual machines,
        and can elastically scale in and out in response to load. DSC is used to configure the VMs as they come
        online so they are running the production software.
        References: https://docs.microsoft.com/en-us/azure/virtual-machine-scale-sets/virtual-machine-scale-sets-dsc


QUESTION 45



        DRAG DROP
        You have two Azure virtual machines named VM1 and VM2. VM1 has a single data disk named Disk1. You need
        to attach Disk1 to VM2. The solution must minimize downtime for both virtual machines.
        Which four actions should you perform in sequence? To answer, move the appropriate actions from the list
        of actions to the answer area and arrange them in the correct order.

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
        5. In the Disks pane, to the far right of the data disk that you would like to detach, click the Detach
        button image detach button.
        6. After the disk has been removed, click Save on the top of the pane.
        7. In the virtual machine pane, click Overview and then click the Start button at the top of the pane to
        restart the VM.
        8. The disk stays in storage but is no longer attached to a virtual machine.
        References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/detach-disk
        https://docs.microsoft.com/en-us/azure/lab-services/devtest-lab-attach-detach-data-disk


QUESTION 46



        HOTSPOT
        You have an Azure subscription named Subscription1. Subscription1 contains a virtual machine named VM1.
        You install and configure a web server and a DNS server on VM1.
        VM1 has the effective network security rules shown in the following exhibit.
        Use the drop-down menus to select the answer choice that completes each statement based on the information
        presented.

        NOTE: Each correct selection is worth one point.

        Explanation:
        Box 1:
        Rule2 blocks ports 50-60, which includes port 53, the DNS port. Internet users can reach the Web server,
        since it uses port 80.
        Box 2:
        If Rule2 is removed internet users can reach the DNS server as well.
        Note: Rules are processed in priority order, with lower numbers processed before higher numbers, because
        lower numbers have higher priority. Once traffic matches a rule, processing stops. As a result, any rules
        that exist with lower priorities (higher numbers) that have the same attributes as rules with higher
        priorities are not processed.
        References: https://docs.microsoft.com/en-us/azure/virtual-network/security-overview


QUESTION 47



        DRAG DROP
        You have an Azure Linux virtual machine that is protected by Azure Backup. One week ago, two files were
        deleted from the virtual machine.
        You need to restore the deleted files to an on-premises computer as quickly as possible.
        Which four actions should you perform in sequence? To answer, move the appropriate actions from the list
        of actions to the answer area and arrange them in the correct order.

        Explanation:

        To restore files or folders from the recovery point, go to the virtual machine and choose the desired
        recovery point.
        Step 0. In the virtual machine's menu, click Backup to open the Backup dashboard. Step 1. In the Backup
        dashboard menu, click File Recovery.
        Step 2. From the Select recovery point drop-down menu, select the recovery point that holds the files you
        want. By default, the latest recovery point is already selected.
        Step 3: To download the software used to copy files from the recovery point, click Download Executable
        (for Windows Azure VM) or Download Script (for Linux Azure VM, a python script is generated).
        Step 4: Copy the files by using AzCopy
        AzCopy is a command-line utility designed for copying data to/from Microsoft Azure Blob, File, and Table
        storage, using simple commands designed for optimal performance. You can copy data between a file
        system and a storage account, or between storage accounts.
        References: https://docs.microsoft.com/en-us/azure/backup/backup-azure-restore-files-from-vm
        https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy


QUESTION 48



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab. Use the following login credentials as needed:
        Azure Username: XXXXXXX
        Azure Password: XXXXXXX
        The following information is for technical support purposes only:
        Lab Instance: 9172796

        Task 3
        You plan to protect on-premises virtual machines and Azure virtual machines by using Azure Backup.
        You need to prepare the backup infrastructure in Azure. The solution must minimize the cost of storing
        the backups in Azure.
        What should you do from the Azure portal?

        Correct Answer: See solution below.

        Explanation:
        First, create Recovery Services vault.
        Step 1: On the left-hand menu, select All services and in the services list, type Recovery Services. As
        you type, the list of resources filters. When you see Recovery Services vaults in the list, select it to
        open the Recovery Services vaults menu.
        Step 2: In the Recovery Services vaults menu, click Add to open the Recovery Services vault menu.
        Step 3: In the Recovery Services vault menu, for example, Type myRecoveryServicesVault in Name.
        The current subscription ID appears in Subscription. If you have additional subscriptions, you could choose
        another subscription for the new vault.
        For Resource group select Use existing and choose myResourceGroup. If myResourceGroup doesn't exist,
        select Create new and type myResourceGroup.
        From the Location drop-down menu, choose West Europe. Click Create to create your Recovery Services vault.
        References: https://docs.microsoft.com/en-us/azure/backup/tutorial-backup-vm-at-scale


QUESTION 49



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab.

        Task 3
        You need to deploy two Azure virtual machines named VM1003a and VM1003b based on an Ubuntu Server image. The
        deployment must meet the following requirements:
        Provide a Service Level Agreement (SLA) of 99.95 percent availability. Use managed disks.
        What should you do from the Azure portal?

        Correct Answer: See solution below.

        Explanation:
        Step 1: Open the Azure portal.
        Step 2: On the left menu, select All resources. You can sort the resources by Type to easily find your images.
        Step 3: Select the image you want to use from the list. The image Overview page opens. Step 4: Select
        Create VM from the menu.
        Step 5: Enter the virtual machine information.
        Select VM1003a as the name for the first Virtual machine.
        The user name and password entered here will be used to log in to the virtual machine. When complete,
        select OK. You can create the new VM in an existing resource group, or choose Create new to create a new
        resource group to store the VM.
        Step 6: Select a size for the VM. To see more sizes, select View all or change the Supported disk type
        filter. Step 7: Under Settings, make changes as necessary and select OK.
        Step 8: On the summary page, you should see your image name listed as a Private image. Select Ok to start
        the virtual machine deployment.
        Repeat the procedure for the second VM and name it VM1003b. References:
        https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-generalized-managed


QUESTION 50



        SIMULATION
        Please wait while the virtual machine loads. Once loaded, you may proceed to the lab section. This may
        take a few minutes, and the wait time will not be deducted from your overall test time.
        When the Next button is available, click it to access the lab section. In this section, you will perform
        a set of tasks in a live environment. While most functionality will be available to you as it would be
        in a live environment, some functionality (e.g, copy and paste, ability to navigate to external websites)
        will not be possible by design.
        Scoring is based on the outcome of performing the tasks stated in the lab. In other words, it doesn’t
        matter how you accomplish the task, if you successfully perform it, you will earn credit for that task.
        Labs are not timed separately, and this exam may have more than one lab that you must complete. You can
        use as much time as you would like to complete each lab. But, you should manage your time appropriately
        to ensure that you are able to complete the lab(s) and all other sections of the exam in the time provided.
        Please note that once you submit your work by clicking the Next button within a lab, you will NOT be able
        to return to the lab.
        You may now click next to proceed to the lab.

        Task 4
        You need to deploy an Azure virtual machine named VM1004a based on an Ubuntu Server image, and then
        configure VM1004a to meet the following requirements:
        The virtual machine must contain data disks that can store at least 15 TB of data. The data disks must be
        able to provide at least 2.000 IOPS.
        Storage costs must be minimized.
        What should you do from the Azure portal?
        Correct Answer: See solution below.
        Section: [none] Explanation
        Explanation/Reference:
        Explanation:
        Step 1: Open the Azure portal.
        Step 2: On the left menu, select All resources. You can sort the resources by Type to easily find your images.
        Step 3: Select the image you want to use from the list. The image Overview page opens. Step 4: Select
        Create VM from the menu.
        Step 5: Enter the virtual machine information.
        Select VM1004a as the name for the first Virtual machine.
        The user name and password entered here will be used to log in to the virtual machine. When complete,
        select OK. You can create the new VM in an existing resource group, or choose Create new to create a new
        resource group to store the VM.
        Step 6: Select a size for the VM. To see more sizes, select View all or change the Supported disk type
        filter. To support 15 TB of data you would need a Premium disk.
        Step 7: Under Settings, make changes as necessary and select OK.
        Step 8: On the summary page, you should see your image name listed as a Private image. Select Ok to start
        the virtual machine deployment.

  References: https://docs.microsoft.com/en-us/azure/virtual-machines/windows/create-vm-generalized-managed


<br>
<br>
<br>
<br>
{!footer.md!}
