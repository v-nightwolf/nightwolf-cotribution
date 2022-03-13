# DevOps Interview Question
---

 We have consolidated a list of frequently asked DevOps interview questions for Freshers and Experianced. This will help DevOps Engineers in their preparations for Interview. 
  You will find these questions very helpful in your DevOps interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

1. What is Source Code Management?

        It is a process through which we can store and manage any code. Developers write code, Testers write test
        cases and DevOps engineers write scripts. This code, we can store and manage in Source Code Management.
        Different teams can store code simultaneously. It saves all changes separately. We can retrieve this code
        at any point of time.

2. What are the Advantages of Source Code Management ? 

        - Helps in Achieving teamwork.
        - Can work on different features simultaneously.
        - Acts like pipeline b/w offshore & onshore teams.
        - Track changes (Minute level).
        - Different people from the same team, as well as different teams, can store code simultaneously.

3. Available Source Code Management tools in the market? 
        
        There are so many Source Code Management tools available in the market. Those are 
         - Git
         - SVN
         - Perforce 
         - Clear case
        Out of all these tools, Git is the most advanced tool in the market where we are getting so many
        advantages compared to other Source Code Management tools.

4. What is Git?

        Git is one of the Source Code Management tools where we can store any type of code. Git is the most advanced 
        tool in the market now. We also call Git is version control system because every update stored as a new
        version. At any point of time, we can get any previous version. We can go back to previous versions. Every
        version will have a unique number. That number we call commit-ID. By using this commit ID, we can track each
        change i.e. who did what at what time. For every version, it takes incremental backup instead of taking 
        the whole backup. That’s why Git occupies less space. Since it is occupying less space, it is very fast.

5. What are the advantages of Git? 

        Speed:- Git stores every update in the form of versions. For every version, it takes incremental backup
                instead of taking the whole backup. Since it is taking less space, Git is very fast. That
                incremental backup we call “Snapshot”.

        Parallel branching:- We can create any number of branches as per our requirement. No need to take prior
                permission from any one, unlike other Source Code Management tools. Branching is for parallel
                development. Git branches allow us to work simultaneously on multiple features. 

        Fully Distributed:- A backup copy is available in multiple locations in each and everyone’s server instead
                of keeping in one central location, unlike other Source Code Management tools. So even if we lose
                data from one server, we can recover it easily. That’s why we call GIT as DVCS (Distributed 
                Version Control System)

6. What are the stages in Git? 

        There are total of 4 stages in Git 

        1. Workspace:- It is the place where we can create files physically and modify. Being a Git user, we work
                in this work space.
        2. Staging area/Indexing area:- In this area, Git takes a snapshot for every version. It is a buffer zone
                between workspace and local repository. We can’t see this region because it is virtual.
        3. Local repository:- It is the place where Git stores all commit locally. It is a hidden directory so
                that no one can delete it accidentally. Every commit will have unique commit ID.
        4. Central repository:- It is the place where Git stores all commit centrally. It belongs to everyone who
                is working in your project. Git Hub is one of the central repositories. Used for storing the code
                and sharing the code to others in the team.

7. What is the common branching strategy in Git?

        - Product is the same, so one repo. But different features.
        - Each feature has one separate branch
        - Finally, merge (code) all branches
        - For Parallel development
        - Can create any no of branches
        - Can create one branch on the basis of another branch
        - Changes are personal to that particular branch
        - Can put files only in branches (not in repo directly)
        - The default branch is “Master”
        - Files created in a workspace will be visible in any of the branch workspaces until you commit. Once you
          commit, then that file belongs to that particular branch.

8. How many types of repositories available in Git?

        There are two types of repositories available in Git

        Bare Repositories (Central)
            These repositories are only for Storing & Sharing the code
            All central repositories are bare repositories

        Non – Bare Repositories (Local)
            In these repositories, we can modify the files
            All local /user repositories are Bare Repositories

9. Can you elaborate commit in Git?

        - Storing file permanently in the local repository we call commit.
        - For every commit, we get one commit ID.
        - It contains 40 long Alpha-numeric characters.
        - It uses the concept “Check some” (It’s a tool in Linux, generates binary value equal to the data present in file)
        - Even if you change one dot, Commit-ID will get changed.
        - Helps in tracking the changes

10. What do you mean by “Snapshot” in Git?

        - It is a backup copy for each version git stores in a repository.
        - Snapshot is an incremental backup copy (only backup for new changes)
        - Snapshot represents some data of particular time so that, we can get data of particular time by taking
          that particular snapshot
        - This snapshot will be taken in Staging area in Git which is present between Git workspace and Git local
          repository.

11. What is GitHub?

        Git hub is central git repository where we can store code centrally. Git hub belongs to Microsoft Company.
        We can create any number of repositories in Git hub. All public repositories are free and can be accessible
        by everyone. Private repositories are not free and can restrict public access for security. We can copy the
        repository from one account to other accounts also. This process we call as “Fork”. In this repository also
        we can create branches. The default branch is “Master”.

12. What is Git merge?

        By default, we get one branch in git local repository called “Master”. We can create any no of branches for
        parallel development. We write code for each feature in each branch so that development happens separately.
        Finally, we merge code off all branches in to Master and push to central repository. We can merge code to
        any other branch as well. But merging code into master is standard practice that being followed widely.

        Sometimes, while merging, conflict occurs. When same file is in different branches with different code,
        when try to merge those branches, conflict occurs. We need to resolve that conflict manually by rearranging
        the code.

13. What is Git stash?

        We create multiple branches to work simultaneously on multiple features. But to work on multiple tasks
        simultaneously in one branch (i.e. on one feature), we use git stash. Stash is a temporary repository 
        where we can store our content and bring it back whenever we want to continue with our work with that
        stored content. 
        It removes content inside file from working directory and puts in stashing store and gives clean working
        directory so that we can start new work freshly. Later on you can bring back that stashed items to working
        directory and can resume your work on that file. Git stash applicable to modified files. Not new files.
        Once we finish our work, we can remove all stashed items form stash repository.

14. What is Git Reset?

        Git Reset command is used to remove changes form staging area. This is bringing back file form staging area
        to work directory. We use this command before commit. Often we go with git add accidentally. In this case
        if we commit, that file will be committed. Once you commit, commit ID will be generated and it will be in
        the knowledge of everyone. So to avoid this one, we use Git reset.

        If you add “–hard” flag to git reset command, in one go, file will be removed from staging area as well as
        working directory. We generally go with this one if we fell that something wrong in the file itself.

15. What is Git Revert?

        Git Revert command is used to remove changes from all 3 stages (work directory, staging area and local
        repository). We use this command after commit. Sometimes, we commit accidentally and later on we realize
        that we shouldn’t have done that. For this we use Git revert. This operation will generate new commit ID
        with some meaningful message to ignore previous commit where mistake is there. But, here we can’t
        completely eliminate the commit where mistake is there. Because Git tracks each and every change.

16. Difference between Git pull and Git clone?

        We use these two commands to get changes from central repository. For the first time if you want whole 
        central repository in your local server, we use git clone. It brings entire repository to your local server.
        Next time onwards you might want only changes instead of whole repository. In this case, we use Git pull.

        - Git clone is to get whole copy of central repository
        - Git pull is to get only new changes from central repository (Incremental data)

17. What is the difference between Git pull and Fetch?

        We use Git pull command to get changes from central repository. In this operation, internally two commands
        will get executed. One is Git fetch and another one is Git merge.
        Git fetch means, only bringing changes from central repo to local repo. But these changes will not be
        integrated to local repo which is there in your server. Git merge means, merging changes to your local
        repository which is there in your server. Then only you can see these changes. So Git pull is the
        combination of Git pull and Git merge.

18. What is the difference between Git merge and rebase? 

        We often use these commands to merge code in multiple branches. Both are almost same but few differences.
        When you run Git merge, one new merge commit will be generated which is having the history of both
        development branches. It preserves the history of both branches. By seeing this merge commit, everyone
        will come to know that we merged two branches. If you do Git rebase, commits in new branch will be applied
        on top of base branch tip. There won’t be any merge commit here. It appears that you started working in one
        single branch form the beginning. This operation will not preserves the history of new branch.

19. What is Git Bisect?

        Git Bisect we use to pick bad commit out of all good commits. Often developers do some mistakes. For them
        it is very difficult to pick that commit where mistake is there. They go with building all commits one by
        one to pick bad commit. But Git bisect made their lives easy. Git bisect divides all commits equally in to
        two parts (bisecting equally). Now instead of building each commit, they go with building both parts. Where
        ever bad commit is there, that part build will be failed. We do operation many times till we get bad commit.
        So Git bisect allows you to find a bad commit out of good commits. You don’t have to trace down the bad
        commit by hand; git-bisect will do that for you.

20. What is Git squash?

        To move multiple commits into its parent so that you end up with one commit. If you repeat this process
        multiple times, you can reduce “n” number of commits to a single one. Finally we will end up with only one
        parent commit. We use this operation just to reduce number of commits.

21. What is Git hooks?
  
        We often call this as web hooks as well. By default we get some configuration files when you install git.
        These files we use to set some permissions and notification purpose. We have different types of hooks
        (pre commit hooks & post commit hooks) Pre-commit hooks:- Sometimes you would want every member in your
        team to follow certain pattern while giving commit message. Then only it should allow them to commit.
        These type of restrictions we call pre-commit hooks.
 
        Post-commit hooks:- Sometimes, being a manager you would want an email notification regarding every commit
        occurs in a central repository. This kind of things we call post-commit hooks.
        In simple terms, hooks are nothing but scripts to put some restrictions.

22. What is Git cherry-pick?

        When you go with git merge, all commits which are there in new development branch will be merged into
        current branch where you are. But sometimes, requirement will be in such that you would want to get
        only one commit form development branch instead of merging all commits. In this case we go with git
        cherry-pick. Git cherry-pick will pick only one commit whatever you select and merges with commits which
        are there in your current branch. So picking particular commit and merging into your current branch we
        call git cherry-pick.

23. What is the difference between Git and SVN?

        SVN:- It is centralized version control system (CVCS) where back up copy will be placed in only one central
           repository. There is no branching strategy in SVN. You can’t create branches. So no parallel development.
           There is no local repository. So can’t save anything locally. Every time after writing code you need to
           push that code to central repository immediately to save changes.

        Git:- It is a Distributed version control system where back up copy is available in everyone’s machine’s
           local repository as well as a central repository. We can create any no of branches as we want. So we
           can go in parallel development simultaneously. Every Git repository will have its own local repository.
           So we can save changes locally. At the end of our work finally, we can push code to a central repository.

24. What is the commit message in Git?

        Every time we commit, while committing, we have to give commit message just to identify each commit. We
        can’t remember to commit numbers because they contain 40 long alphanumeric characters. So, to remember
        commits easily, we give commit message. The format of commit message differs from company to company and
        individual to individual. We have one more way to identify commits. That is giving “Tags”. Tag is a kind
        of meaningful name to a particular commit. Instead of referring to commit ID, we can refer to tags.
        Internally tag will refer to respective commit ID. These are the ways to get a particular commit easily.

25. What is Configuration Management?

        It is a method through we automate admin tasks. Each and every minute details of a system, we call
        configuration details. If we do any change here means we are changing the configuration of a machine.
        That means we are managing the configuration of the machine. System administrators used to manage the
        configuration of machine through manually. DevOps engineers are managing this configuration through
        automated way by using some tools which are available in the market. That’s why we call these tools
        as configuration management tools.

26. What is IAC?

        IAC means Infrastructure As Code. It is the process through which we automate all admin tasks. Here we
        write code in Ruby script in chef. When you apply this code, automatically code will be converted into
        Infrastructure. So here we are getting so many advantages in writing the code. Those are: 

          1. Code is Testable (Testing code is easy compare to Infrastructure)
          2. Code is Repeatable (Can re-use the same code again and again)
          3. Code is Versionable (Can store in versions so that can get any previous versions at any time)

27. What do you mean by IT Infrastructure??

        IT Infrastructure is a composite of the following things

         1. Software
         2. Network
         3. People
         4. Process

28. What are the problems that system admins used to face earlier when there were no configuration management tools?
  
        1. Managing users & Groups is big hectic thing (create users and groups, delete, edit……)
        2. Dealing with packages (Installing, Upgrading & Uninstalling) 
        3. Taking backups on regular basis manually 
        4. Deploying all kinds of applications in servers
        5. Configure services (Starting, stopping and restarting services) These are some problems that system 
           administrators used to face earlier in their manual process of managing configuration of any machine.

29. Why should we go with Configuration Management Tool?
 
        1. By using the Configuration Management Tool, we can automate almost each and every admin task.
        2. We can increase uptime so that can provide maximum user satisfaction. 
        3. Improve the performance of systems. 
        4. Ensure compliance
        5. Prevent errors as tools won’t do any errors
        6. Reduce cost (Buy tool once and use 24/7)

30. How this Configuration Management Tool works?

        Whatever system admins (Linux/windows) used to do manually, now we are automating all those tasks by
        using any Configuration Management Tool. We can use this tool whether your servers are in on-premises
        or in the cloud. It turns your code into infrastructure. So your code is versionable, repeatable and 
        testable. You only need to tell what the desired configuration should be, not how to achieve it. Through 
        automation, we get our desired state of server. This is unique feature of Configuration Management Tool.

31. What is the architecture of Chef? 

        Chef is an administration tool. In this we have total 3 stages: 

         1. Chef Workstation (It is the place where we write code) 
         2. Chef Server (It is the place where we store code) 
         3. Chef Node (It is the place where we apply code) We need to establish communication among workstation,
            server and nodes. You can have any no of nodes. There is no limit. Chef can manage any no of nodes 
            effectively.

32. Components of Chef? 

        1. Chef Workstation: Where you write the code 
        2. Chef Server: Where you upload the code
        3. Chef Node: Where you apply the code 
        4. Knife: Tool to establish communication among workstation, server & node. 
        5. Chef-client: Tool runs on every chef node to pull code from chef server 
        6. Ohai: Maintains current state information of chef node (System Discovery Tool) 
        7. Idempotency: Tracking the state of system resources to ensure that the changes should not re-apply
                        repeatedly. 
        8. Chef Supermarket: Where you get custom code

33. How does Chef Works? 
   
        We need to install chef package in workstation, server and nodes. We create cookbook in workstation. Inside
        cookbook, there will be a default recipe where you write code in ruby script. You can create any no of
        recipes. There is no limit. After writing code in recipe, we upload whole cookbook to chef server. Chef 
        server acts as central hub storing code. Then, we need to add this cookbook’s recipe to nodes run-list.
        Chef-client tool will be there in each and every chef node. It runs frequently. Chef-client comes to chef
        server and take that code and applies that code in node. This is how code will be converted into infrastructure.

34. What is Idempotency? 

        It is unique feature in all configuration management tools. It ensures that changes should not re-apply
        repeatedly. Once chef-client converted code into Infrastructure, then even chef-client runs again, it will
        not take any action. It won’t do the same task again and again. If any new changes are there in that code,
        then only chef-client is going to take action. So it doesn’t make any difference ever if you run
        chef-client any no of times. So tracking the system details to not to reapply changes again and again,
        we call Idempotency.

35. What is Ohai and how does it works?? 

        Ohai we call “System Discovery Tool”. It stores system information. It captures each and every minute 
        details of system and updates it then and there if any new changes are there. Whenever chef-client converts
        code in infrastructure in node, immediately Ohai store will be updated. Next time onwards, before 
        chef-client runs, it verifies in Ohai store to know about current state of information. So chef-client 
        will come to know the current state of server. Then chef-client acts accordingly. If new changes are there,
        then only it will take action. If there are no new changes, then it won’t take any action. Ohai tool helps 
        in achieving this.

36. How many types of chef server?

        Total there are 3 ways through which we can manage chef server.

          1. Directly we can take chef server from Chef Company itself. In this case, everything will be managed 
             by Chef Company. You will get support from chef. This type of server we call Managed/Hosted chef.
             This is completely Graphical User Interface (GUI). It’s not free. We need to pay to Chef Company 
             after exceeding free tier limit. 

          2. We can launch one server and we need to install chef server package. It is completely free package. 
             It’s GUI (Graphical User interface) 

          3. We can launch one server and we need to install chef server package. It is completely free package. 
             It’s CLI (Command Line Interface).

37. What is there inside cookbook?
  
        Below mentioned files and folders will be there inside cookbook when you first create it:

           Chefignore: like .gitignore (to ignore files and folders)
           Kitchen.yml: for testing of cookbook 
           Metadata.rb: name, author, version…. etc of cookbook
           Readme.md: information about usage of cookbook 
           Recipe: It is a file where you write code
           Spec: for unit test 
           Test: for integration test

38. What is Attributes concept in chef? 

        Sometimes we might need to deploy web applications to in nodes and for that we need to know some host 
        specific details of each server like IP Address, Hostname etc. Because we need to mention that in
        configuration files of each server. These files we call as Configuration files. This information will
        be vary from system to system. These host specific details that we mention in Configuration files,we 
        call “Attributes”. Chef-client tool gathers these Attributes from Ohai store and puts in configuration 
        files. Instead of hard coding these attributes, we mention as variables so that every time, file will 
        be updated with latest details of their respective nodes.

39. What is Run-list in Chef?

        This is an ordered list of recipes that we are going to apply to nodes. We mention all recipes in 
        cookbook and then we upload that cookbook to chef server. Then, we attach all recipes to nodes 
        run-list in sequence order. When chef-client runs, it applies all recipes to nodes in the same 
        order whatever the order you mention in run-list. Because sometimes order is important especially 
        when we deal with dependent recipes.

40. What is bootstrap? 

        It is the process of adding chef node to chef server or we can call, bringing any machine into chef 
        environment. In this bootstrapping process total three action will be performed automatically.

          1. Node gets connected to chef server.
          2. Chef server will install chef package in chef node.
          3. Cookbooks will be applied to chef node.

        It is only one time effort. As and when we purchase any new machine in company, immediately we add that
        server to chef server. At a time, we can only bootstrap one machine, not  multiple machines.

41. What is the workflow of Chef? 

        We connect chef workstation, chef server and chef node with each other. After that, we create cookbook
        in chef workstation and inside that cookbook, we write code in recipe w.r.t. the infrastructure to be
        created. Then we upload entire cookbook to chef server and attach that cookbook’s recipe to nodes run-list.
        Now we automate chef-client which will be there in all chef nodes. Chef-client runs frequently towards chef
        server for new code. So chef-client will get that code from server and finally applies to chef node. 
        This is how, code is converted into infrastructure. If no changes are there in code, even if chef-client
        runs any no of time, it won’t take any action until it finds some changes in code. This is what we call
        Idempotency.

42. How does we connect Chef Workstation to Chef Server? 

        First we download started kit from chef server. This will be downloaded in the form of zip file. If we 
        extract this zip file, we will get chef-repo folder. This chef-repo folder we need to place in chef
        workstation. Inside chef-repo folder, we can see total three folders. They are .chef, cookbooks and roles.
        Out of these three, .chef folder is responsible to establish communication between chef server and chef
        workstation. Because, inside .chef folder, we can see two files. They are knife.rb and organization.pem.
        Inside kinfe.rb, there will be the url (address) of chef server. Because of this url, communication will
        be established between chef server and chef workstation. This is how we connect Chef Workstation to Chef
        Server.

43. How does the chef-client runs automatically? 

        By default, chef-client runs manually. So we need to automate this manually. For this, we use “cron tool”
        which is the default tool in all Linux machines use to schedule tasks to be executed automatically at
        frequent intervals. So in this “crontab” file, we give chef-client command and we need to set the timing
        as per our requirement. Then onwards chef-client runs automatically after every frequent intervals. It is
        only one time effort. When we purchase any new server in company, along with bootstrap, we automate 
        chef-client then and there.

44. What is chef supermarket?

        Chef supermarket is the place where we get custom cookbooks. Every time we need not to create cookbooks and
        need not to write code from scratch. We can go with custom cookbooks which are available in chef supermarket
        being provided by chef organization and community. We can download these cookbooks and modify as per our 
        needs. We get almost each and every cookbook from chef supermarket. They are safe to use.

45. What is wrapper cookbook?

        Either we can download those chef supermarket cookbooks or without downloading, we can call these 
        supermarket cookbooks during run time so that every time we get updates automatically for that cookbook if
        any new updates are there. Here, we use our own cookbook to call chef supermarket cookbook. This process
        of calling cookbook by using another cookbook, we call wrapper cookbook. Especially, we use this concept
        to automate chef-client.

46. What is “roles” in chef? 

        Roles are nothing but a Custom run-list. We create role & upload to chef server & assign them to nodes.
        If we have so many nodes, need to add cookbook to run-list of all those nodes, it is very difficult to
        attach to all nodes run-list. So, we create role & attach that role to all those nodes once. Next time
        onwards, add cookbook to that role. Automatically, that cookbook will be attached to all those nodes.
        So role is one time effort. Instead of adding cookbooks to each & every node’s run-list always, just 
        create a role & attach that role to nodes. When we add cookbook to that role, it will be automatically
        applied to all nodes those assigned with that role.

47. What is include_recipe in chef? 

        By default, we can call one recipe at a time in one cookbook. But if you want to call multiple recipes
        from same cookbook, we use include_recipe concept. Here, we take default recipe and we mention all recipes
        to be called in this default recipe in an order. If we call default recipe, automatically default recipe
        will call all other recipes which are there inside default recipe. By using one recipe, we can call any
        number of recipes. This process of calling one recipe by using other recipe, we call as include_recipe.
        Here condition is we can call recipes from same cookbook, but not from different cookbooks.

48. How to deploy a web server by using chef?

        package ‘httpd’ do
          action :install
        end 

        file ‘/var/www/html/index.html’ do
         content ‘Hello nightwolf Students!!’ 
         action :create
        end

        service ‘httpd’ do
          action [ :enable, :start ]
        end

49. How to write ruby code to create file, directory?

        file ‘/myfile’ do 
          content ‘This is my second file’ 
          action :create
          owner ‘root’
          group ‘root’
        end

        directory ‘/mydir’ do
          action :create
          owner ‘root’
          group ‘root’
        end

50. How to write ruby code to create user, group and install package?

        user ‘user1’ do
          action: create
        end

        group ‘group1’ do
          action :create
          members ‘user1’
          append true
        end

        package ‘httpd’ do
          action: install
        end

51. What is container?

        The container is like a virtual machine in which we can deploy any type of applications, softwares and 
        libraries. It’s a light weight virtual machine which uses OS in the form of image, which is having less
        in size compare to traditional VMware and oracle virtual box OS images. Container word has been taken
        from shipping containers. It has everything to run an application.

52. What is virtualization?

        Logically dividing big machine into multiple virtual machines so that each virtual machine acts as new
        server and we can deploy any kind of applications in it. For this first we install any virtualization
        software on top of base OS. This virtualization software will divide base machine resources in to logical
        components. In a simple terms, logically dividing one machine into multiple machines we call virtualization.

53. What is Docker? 

        Docker is a tool by using which, we create containers in less time. Docker uses light weight OS in the form
        of docker images that we will get from docker hub. Docker is open source now. It became so popular because
        of its unique virtualization concept called “Containerization” which is not there in other tools. We can
        use docker in both windows and Linux machines.

54. What do you mean by docker image?

        Docker image is light weight OS provided by docker company. We can get any type of docker image form docker
        hub. We use these docker images to create docker containers. This docker images may contain only OS or OS +
        other softwares as well. Each software in docker image, will be stored in the form of layer. Advantage of 
        using docker images is, we can replicate the same environment any no of times.

55. What are the ways through which we can create docker images?
 
        There are three ways through which we can create docker images.

          1. We can take any type of docker image directly from docker hub being provided by docker company and 
             docker community.
          2. We can create our own docker images form our own docker containers i.e. first we create container form
             base docker image taken form docker hub and then by going inside container, we install all required
             soft wares and then create docker image from our own docker container.
          3. We can create docker image form docker file. It is the most preferred way of creating docker images.

56. What is docker file and why do we use it?

        It is a just normal text file with instructions in it to build docker image. It is the automated way of 
        creating docker images. Once you build docker image, automatically docker file will be created. In this
        file, we mention required OS image and all required soft wares in the form of instructions. Once we build
        docker file, back end, docker container will be created and then docker image will be crated from that
        container and that container will be destroyed automatically.

57. Difference between docker and VM Ware?

        VM Ware uses complete OS which contains GBs in size. But docker image size is MBs only. So it takes less
        size. That’s why it takes less base machine resources. This docker image is compressed version of OS.
        The second advantage of docker is, there is no pre-allocation of RAM. During run time, it takes RAM as
        pre requirement from base machine and one’s job is done, it release RAM. But in VM Ware, pre-allocation
        of RAM is there and it blocked whether it uses or not. So need more RAM for base machine if you want to
        use VM Ware unlike Docker.

58. What is OS-Lever Virtualization?

        It is the unique feature of Docker which is not available in other virtualization soft wares. Docker takes
        most of UNIX features form host machine OS and it only takes extra layers of required OS in the form of
        docker image. So docker image contains only extra layers of required OS. For core UNIX kernel, it depends
        upon host OS, why because UNIX kernel is same in any of the UNIX and Linux flavors. In a simple terms,
        docker takes host OS virtually. That’s why we call this concept as OS-Lever Virtualization.

59. What is Layered file system/Union file system?

        Inside docker container, wheat ever we do, that forms as a new layer. For instance, creating files,
        directories, installing packages etc. This is what we call as layered file system. Each layer takes less
        space. We can create docker image form this container. In that docker image also we get all these layers
        and forms unity. That’s why we also call Union File System. If we create container out of docker image,
        you can able to see all those files, directories and packages. This is what replication of same environment.

60. What are the benefits of Docker?

          1. Containerization (OS level virtualization) (No need guest OS)   
          2. No pre-allocation of RAM
          3. Can replicate same environment   
          4. Less cost   
          5. Less weight (MB’s in size)  
          6. Fast to fire up  
          7. Can run on physical/virtual/cloud  
          8. Can re-use (same image)   
          9. Can create containers in less time


[<h3 style="text-align: center;font-family: cursive;"> Next Page </h3>](devops_interview_questions-2.md)



You may also refer to:

* [Linux Interview Questions for Freshers](linux_basic.md)
* [Linux Interview Questions for Freshers-2](linux_interview_questions_for_freshers.md)
* [Linux Interview Questions for Freshers and Experianced - L1](linux_L1.md)
* [Linux Interview Questions for Experianced Linux Admins - L2](linux_L2.md)
* [Advanced Linux Interview Questions for Experianced Admins - L3](linux_L3.md)
* [OS Network Interview Questions](network.md)
* [AWS interview questions for experianced professionals](aws.md)
* [DevOps Interview Questions for Freshers and Experianced-2](devops_interview_questions-2.md)
* [GIT Interview Questions for DevOps Roles](git.md)
* [Jenkins Interview Questions for Experianced DevOps Engineer](jenkins.md)
* [Interview materials](reference.md)
