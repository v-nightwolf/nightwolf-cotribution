# Google Cloud Associate Cloud Engineer Practice Exam - 2: 
---
These are top 100 GCP ACE(Google Cloud Platform Associate Cloud Engineer) certification practice questions/cheatsheet (GCP ACE exam dumps) for professionals who are aspired to be GCP ACE certified. You will find these GCP ACE questions and answers very helpful in your GCP-ACE certification and interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---
{!inpage-ads.md!}
---

1. A team of developers would like to have a standard work environment in Compute Engine.
You would like to be able to create multiple instances with identical configurations. The
configurations should be easy to change. What feature of Compute Engine would you use to specify the configuration?

        a). snapshot
        b). managed instance groups
        c). instance template
        d). unmanaged instance groups

        Correct: c

        Explanation:
            Instance templates specify the configuration of virtual machines and managed instance groups.
            Unmanaged instance groups may be heterogeneous and do not use instance templates. Snapshots
            are copies of disks at a point in time. They are useful for backups and copying disks but are not
            used for specifying configurations. 
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/images/image-families-best-practices>https://cloud.google.com/compute/docs/images/image-families-best-practices</a>

    ---

2. An IoT startup is uploading 2 TB of historical data to Cloud Storage. The data is in files
with one file per day per sensor. There are thousands of files. The file names are the date
followed by sensor ID, such as 20210101sensorABCD for a file with data from a sensor
called ABCD on January 1, 2021. The loads are not proceeding as quickly as expected.
What might be the cause of the slower than expected upload?

        a). The files are in gzip format instead of Avro format.
        b). The file names use the date as the first part of the filename so they may be creating hotspots 
            when writing data to Cloud Storage.
        c). The files are in CSV instead of Avro format.
        d). The data in files is being encrypted before being persisted to storage.

        Correct: b 

        Explanation:
            Files are written to servers within the Cloud Storage system based on filenames. Lexically close
            file names are written to the same server. This can lead to hotspotting, which is an imbalance in
            workload that has a small number of servers doing more work than other servers. Data is always
            encrypted before being persisted to storage so there should be no unexpected overhead for
            encrypting data. The size of the file not the format is the primary determiner of how long a file
            will take to load. tspots in which a few servers have heavy loads while other servers have little or
            no load. Load times should not vary based on the file format, such as CSV vs. Avro vs gzip. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/best-practices>https://cloud.google.com/storage/docs/best-practices</a>

    ---

3. Your use of GCP has grown significantly and you now have many resources to manage.
Some resources are in different environments and some are for different teams. You would
like to easily group resources so you can manage them more effectively. What feature of GCP would you use?

        a). Managed instance groups
        b). Snapshots
        c). Images
        d). Labels

        Correct: d

        Explanation:
            Labels allow you to specify key-value pairs for grouping resources, for example, a VM cloud be
            labeled with the key value pair 'envior:production.' Images are copies of operating systems, boot
            loaders, and related data that can be used to create boot disks. Snapshots are copies of persistent
            volumes made at a specific point in time. Managed instance groups are used to create sets of
            identically configured VMs that can autoscale. 
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/labeling-resources>https://cloud.google.com/compute/docs/labeling-resources</a>

    ---

4. You would like to display information about a dataset named primarydata in a project called analytics1. What command would you use?

        a). bq ls --format=prettyjson analytics1:primarydata
        b). bq show --format=prettyjson analytics1:primarydata
        c). bq ls --format=prettyjson analytics1//primarydata
        d). bq metadata --format=prettyjson analytics1:primarydata

        Correct: b

        Explanation:
            The correct answer is bq show --format=prettyjson analytics1:primarydata. The bq command is
            used with BigQuery and the show command displays information about a data set. Projects and
            datasets are specified as [project name]:[dataset name]. The option bq ls --format=prettyjson
            analytics1:primarydata is incorrect because it specifies ls instead of show. The option bq
            metadata --format=prettyjson analytics1:primarydata is incorrect because it specifies metadata
            instead of show. The option bq ls --format=prettyjson analytics1//primarydata is incorrect
            because it specifies ls instead of show and has the wrong syntax for specifying the project and
            dataset names. For more information, see https://cloud.google.com/bigquery/docs/reference/bqcli-reference
    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/reference/bqcli-reference>https://cloud.google.com/bigquery/docs/reference/bqcli-reference</a>

    ---

5. A DevOps engineer has just joined your team and needs to review audit logs. Which of the
following roles could you use to grant the needed permissions without granting more permissions than needed to read logs?

        a). roles/logging.configWriter
        b). roles/logging.bucketWriter
        c). roles/logging.admin
        d). roles/logging.privateLogsViewer

        Correct: d

        Explanation:
            roles/logging.privateLogsViewer provides provides read-only access to log entries in logs,
            including private logs. roles/logging.admin would give permission to review logs but would also
            grant other permissions that are not needed. roles/logging.configWriter grants permissions to
            read and write the configurations of logs-based metrics and sinks for exporting logs.
            roles/logging.bucketWriter provides permission to write to a Cloud Storage bucket. 
    Reference: <a target="_blank" href=https://cloud.google.com/logging/docs/audit>https://cloud.google.com/logging/docs/audit</a>

    ---

6. You have been given the responsibility to manage projects in GCP. What set of permissions will you need to manage projects?

        a). resourcemanager.projects.getIamPolicy and resourcemanager.projects.setIamPolicy only
        b). resourcemanager.projects.get and resourcemanager.projects.setIamPolicy only
        c). resourcemanager.projects.get only
        d). resourcemanager.projects.get, resourcemanager.projects.getIamPolicy, and
            resourcemanager.projects.setIamPolicy only

        Correct: d

        Explanation:
            The permissions, resourcemanager.projects.get, for retrieving projects identified by a project ID,
            resourcemanager.projects.getIamPolicy, for getting IAM access control policy for the specified
            Project, and resourcemanager.projects.setIamPolicy, for setting IAM access control policy for
            the specified project, are all required. 
    Reference: <a target="_blank" href=https://cloud.google.com/resource-manager/docs/access-control-proj>https://cloud.google.com/resource-manager/docs/access-control-proj</a>

    ---

7. Your team has created a set of Docker images. You want to be able to better manage
groups of containers. What could you do to images to enable grouping by environment, installed component, etc?

        a). Set the billing account parameter when creating the image.
        b). Add tags with the gcloud container images add-tag command.
        c). Set the account parameter when creating the images.
        d). Add configurations with the gcloud container images add-configuration command.

        Correct: b

        Explanation:
            Tags are used to group resources in GCP. They are added to images using the gcloud container
            images add-tag command. add-tag is not a valid command. Setting the billing account when
            creating an image is not a valid option. The add-configuration command is not a valid option.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/container/images>https://cloud.google.com/sdk/gcloud/reference/container/images</a>

    ---

8. A game developer is using App Engine to run several services. One of the services queries a
Datastore database for user information. Queries over a single property work correctly but
queries that reference two or more properties are not returning any data. You have been
asked to help diagnose the problem. Which file in the application would you look to first to diagnose the problem?

        a). dispatch.yaml
        b). index.yaml
        c). cron.yaml
        d). app.yaml

        Correct: b

        Explanation:
            Index.yaml files contain indexes for complex queries that reference more than one attribute.
            Datastore automatically creates indexes for single attributes. All queries must have a supporting
            index. App.yaml is for application specifications. Cron.yaml is for scheduled jobs.
            Dispatch.yaml is for overriding routing rules.
    Reference: <a target="_blank" href=https://cloud.google.com/appengine/docs/flexible/go/configuring-datastore-indexes-with-indexyaml>https://cloud.google.com/appengine/docs/flexible/go/configuring-datastore-indexes-with-indexyaml</a>

    ---

9. You would like to grant a role to an identity so that it can access a resource. Which of the
resource's subcommands would you use to grant a role on a resource?

        a). add-iam-policy-binding with --member and --role flags
        b). add-iam-policy-binding with no flags
        c). set-iam-policy with no flags
        d). set-iam-policy with --member and --role flags

        Correct: a

        Explanation:
            The correct subcommand is add-iam-policy-binding with --member and --role flags. The
            subcommand is available for several resource types, including: disk, images, instances, and
            snapshots among others.

    ---

10. A developer has to work with several clients all using Google Cloud. They would like to
easily switch between clients when working on the command line. What would you recommend they do?

        a). Create a configuration for each client and use the gcloud auth command to activate the
            appropriate configuration for each client.
        b). Create a policy for each client and use the gcloud policy command to activate the appropriate
            policy for each client.
        c). Create a configuration for each client and use the gcloud config configurations activate
            command to activate the appropriate configuration for each client.
        d). Create a policy for each client and use the gcloud auth-policy command to activate the
            appropriate policy for each client.

        Correct: c

        Explanation:
            The gcloud config configurations activate command allows for rapid changes to the
            configuration for the Cloud SDK and could be used for that purpose in this use case. gcloud auth
            is not used to activate a configuration. Policies are not used to specify command line
            configurations. 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/config>https://cloud.google.com/sdk/gcloud/reference/config</a>

    ---

11. You have created a new set of service accounts and want them to be used by existing VMs
running in Compute Engine. What command would you use to assign one of the service accounts to a VM instance?

        a). gcloud compute instances assign
        b). gcloud compute instances set-service-account
        c). gcloud instances set-service-account
        d). gcloud compute service-accounts assign

        Correct: b 

        Explanation:
            The command gcloud compute instances set-service-account assigns a service account to a VM
            instance. The other options are not valid gcloud commands. 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/instances>https://cloud.google.com/sdk/gcloud/reference/compute/instances</a>

    ---

12. You have been given the responsibility to manage several projects in GCP. You want to list
roles defined in a particular project. What Cloud SDK command would you use? (Note:
[PROJECT-ID] is a placeholder for a project identifier.)

        a). gcloud iam roles list --project=[PROJECT-ID]
        b). gcloud iam list roles --project=[PROJECT-ID]
        c). gsutil list iam roles [PROJECT-ID]
        d). gsutil iam list roles --project=[PROJECT-ID]

        Correct: a

        Explanation:
            gcloud iam roles list --project=[PROJECT-ID] is the correct command. Gsutil is the command
            line for managing Cloud Storage, not IAM so the two options that use gsutil are incorrect. 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/iam/roles/list>https://cloud.google.com/sdk/gcloud/reference/iam/roles/list</a>

    ---

13. As an administrator of a Kubernetes Engine cluster with many users from several teams
and departments, you would like to easily analyze resource usage by team and department.
What mechanisms could you use to differentiate resource usage?

        a). instance attributes
        b). Namespaces
        c). key-value pairs
        d). Guest attributes
        e). Labels

        Correct: e

        Explanation:
            Labels are key/value pairs that are attached to objects to specify identifying attributes of objects
            that are useful for users and admins. Namespaces are virtual clusters designed for environments
            like the one described, with many users, team, or other organization group structures 

    ---

14. A developer would like to create an image from a snapshot. What command should they
use to create an image named devimage1 from a snapshot called devsnapshot1?

        a). gcloud compute images create devimage1 --source-snapshot devsnapshot1
        b). gcloud disk images create devimage1 --source-snapshot devsnapshot1
        c). gcloud disk create devimage1 --source-snapshot devsnapshot1
        d). gcloud images create devimage1 --source-snapshot devsnapshot1

        Correct: a

        Explanation:
            Images are Compute Engine resources so they use gcloud compute commands. Images are the
            resource that is being created so the command is gcloud compute images create followed by the
            image name and the source-snapshot parameter. gcloud disk and gcloud image are not valid
            gcloud commands.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/disks/create>https://cloud.google.com/sdk/gcloud/reference/compute/disks/create</a>

    ---

15. You have determined that an application using a service account is not functioning
correctly. You think it may be an access control problem. You would like to view audit logs
to determine if this is the case. What audit log would you review?

        a). Policy Denied Audit Log
        b). Identity Access Audit Log
        c). Admin Activity Log
        d). Data Access Audit Log

        Correct: a

        Explanation:
            The Policy Denied Audit Log captures details when a user or service account is denied access
            because of a security policy violation. The Admin Activity Log tracks administrative actions
            including changes to configurations and metadata. The Data Access Audit Log tracks changes or
            reads of resource data or metadata. There is no Identity Access Audit Log in GCP. 
    Reference: <a target="_blank" href=https://cloud.google.com/logging/docs/audit>https://cloud.google.com/logging/docs/audit</a>

    ---

16. You have several buckets using Nearline storage class that you would like to change to
Coldline storage. What command would you use?

        a). gsutil rewrite -s STORAGE_CLASS gs://PATH_TO_OBJECT
        b). gcloud storage rewrite -s STORAGE_CLASS gs://PATH_TO_OBJECT
        c). gsutil newclass -s STORAGE_CLASS gs://PATH_TO_OBJECT
        d). gcloud storage newclass -s STORAGE_CLASS gs://PATH_TO_OBJECT

        Correct: a

        Explanation:
            Gsutil is the command line utility for Cloud Storage. The rewrite command with the -s parameter
            is used to change storage classes. gcloud storage rewrite -s STORAGE_CLASS
            gs://PATH_TO_OBJECT and gcloud storage newclass -s STORAGE_CLASS
            gs://PATH_TO_OBJECT are incorrect options because they use gcloud instead of gsutil. gsutil
            newclass -s STORAGE_CLASS gs://PATH_TO_OBJECT is incorrect, gsutil newclass is not a
            valid Cloud Storage command. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/gsutil/commands/rewrite>https://cloud.google.com/storage/docs/gsutil/commands/rewrite</a>

    ---

17. As a consultant to a global logistics company, you have been asked to advise on the
migration from an on premises inventory system to Google Cloud. The inventory system
uses a relational database. Your client wants to use a managed database service that
supports users in multiple regions. Inventory data needs to be consistent at all times. What
service would you recommend?

        a). Cloud Bigtable
        b). Cloud BigQuery
        c). Cloud Spanner
        d). Cloud SQL

        Correct: c

        Explanation:
            Cloud Spanner is a globally scalable, managed relational database that supports consistency.
            Cloud Bigtable is a NoSQL database. BigQuery is an analytical database. Cloud SQL is a
            relational database but it is designed for regional use cases. 
    Reference: <a target="_blank" href=https://cloud.google.com/spanner/docs/concepts>https://cloud.google.com/spanner/docs/concepts</a>

    ---

18. A client has asked you to help implement a cluster of servers that can scale up and down as
needed and will be resilient to a failure in a zone. What feature of Compute Engine would you use?

        a). snapshot
        b). unmanaged instance groups
        c). managed instance groups
        d). instance templates

        Correct: c

        Explanation:
            Managed instance groups are used to create sets of identically configured VMs that can autoscale
            an can be configure for regional deployment, which would address the need to be resilient to a
            failure in a single zone. 

    ---

19. A distributed application uses Cloud Pub/Sub to send messages to a service that analyzes
the data. Each message should only be sent once but for some reason, messages are sent
repeatedly. What configuration parameter would you investigate in order to correct this problem?

        a). --max-retry-delay
        b). --ack-deadline
        c). --dead-letter-topic
        d). min-retry-delay

        Correct: b

        Explanation:
            The problem may be caused by the consuming application not acknowledging the message has
            been successfully processed within the time required. The --ack-deadline may be set too low and
            the consuming application may not send the acknowledgement within that time. Increasing the
            --ack-deadline would give the consuming application more time to acknowledge successful
            processing of the message. Dead-letter-topics are specified to receive messages that cannot be
            acknowledged. --max-retry-delay is the maximum delay between consecutive deliveries of a
            given message. The min-retry-delay is the minimum delay between consecutive deliveries of a
            given message. Changing either the max or min retry delay will not affect acknowledging a
            message, which is the root cause of the problem. 
    Reference: <a target="_blank" href=https://cloud.google.com/pubsub/docs/publisher>https://cloud.google.com/pubsub/docs/publisher</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/pubsub/docs/subscriber>https://cloud.google.com/pubsub/docs/subscriber</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/pubsub/subscriptions/create>https://cloud.google.com/sdk/gcloud/reference/pubsub/subscriptions/create</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/pubsub/docs/dead-letter-topics>https://cloud.google.com/pubsub/docs/dead-letter-topics</a>

    ---

20. You are working in Cloud Shell to diagnose a problem with a Cloud SQL server running
MySQL. You would like to connect to the MySQL instance from the command line. What
command would you use to connect to the database as root using the built-in client?
[INSTANCE-ID] is the database instance identifier.

        a). gcloud sql connect [INSTANCE-ID] --user=root
        b). gcloud mysql connect [INSTANCE-IP] --user=root
        c). gcloud mysql --host=[INSTANCE -D] --user=root
        d). gsutil sql connect [INSTANCE-ID] --user=root

        Correct: a

        Explanation:
            To use the client built into Cloud Shell, the correct command is gcloud sql connect followed by
            the instance ID of the database you want to connect to along with the --user parameter to specify
            the username. The option mysql --host=[INSTANCE -D] --user=root. Both of the options,
            gcloud mysql --host=[INSTANCE -D] --user=root and gcloud mysql connect [INSTANCE-IP] --
            user=root, use gcloud mysql instead of gcloud sql and so are incorrect. Also gcloud mysql
            connect [INSTANCE-IP] --user=root specifies an IP address instead of an instance identifier.
            gsutil sql connect [INSTANCE-ID] --user=root is incorrect because gcloud is used with Cloud
            SQL and gsutil is command line utility used with Cloud Storage. 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/sql/connect>https://cloud.google.com/sdk/gcloud/reference/sql/connect</a>

    ---

21. You need to deploy a load balancer that will support internal TCP traffic within a single
region. What load balancer would you deploy?

        a). TCP Proxy
        b). Internal HTTP(S) Load Balancing
        c). SSL Proxy
        d). Network TCP/UDP Load Balancing

        Correct: d

        Explanation:
            The correct answer is Network TCP/UDP Load Balancing, which is used for internal TCP traffic.
            SSL Proxy is used for external TCP trafficand SSL processing is offloaded to the the proxy.
            Network TCP/UDP Load Balancing is used for internal TCP traffic. TCP Proxy Load Balancing
            is a reverse proxy load balancer that distributes TCP traffic coming from the internet to virtual
            machine (VM) instances in GCP. 
    Reference: <a target="_blank" href=https://cloud.google.com/loadbalancing/docs/load-balancing-overview>https://cloud.google.com/loadbalancing/docs/load-balancing-overview</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/loadbalancing/docs/choosing-load-balancer>https://cloud.google.com/loadbalancing/docs/choosing-load-balancer</a>

    ---

22. A group of epidemiologists is running a large number of simulations. They are using
several high CPU virtual machines. Each simulation takes approximately 10 minutes to
complete. If a simulation fails before completing, it is restarted on another VM. The
epidemiologists would like to minimize the GCP costs without increasing the time need to
complete a simulation. What would you recommend?

        a). Use preemptible virtual machine instances.
        b). Use more virtual machine instances.
        c). Use sole-tenant VMS.
        d). Use Shielded VM instances.

        Correct: a

        Explanation:
            Preemptible VMs cost significantly less then standard priced VMs. Preemptible VMs run up to
            24 hours before being shut down by Google. The epidemiologist can tolerate failures in some
            simulations since failed simulation are re-run.

    ---

23. A VM is mistakenly started in the wrong region and zone. You suspect the default region
and zone setting for your project is set incorrectly. What command would you use on the
command line to show the default region and zone? [PROJECT-ID] refers to the project identifier to be described.

        a). gcloud project-info describe --project [PROJECT-ID]
        b). gcloud project info describe
        c). gcloud project info list
        d). gcloud compute project-info describe --project [PROJECT-ID]

        Correct: d

        Explanation:
            This is a compute service setting so you would use gcloud compute and the resource is a project
            so project-info is required. The correct command is gcloud compute project-info describe --
            project [PROJECT ID]. The options gcloud project info describe, gcloud project-info describe --
            project [PROJECT ID], and gcloud project info list are not valid gcloud commands, they do not
            specify compute, which is the name of the service the gcloud command applies to.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/project-info>https://cloud.google.com/sdk/gcloud/reference/compute/project-info</a>

    ---

24. An app development team wants to develop a service written in C++ that can process a file
after it is uploaded to Cloud Storage. The processing time varies based on the size and
complexity of the content of the file. Almost all files can be processed in less than 1 minute
but some files can take up to 20 minutes to process. The developers are already using
containers and Cloud Pub/Sub for other services. They plan to use Cloud Storage's trigger
mechanism to send a message to Pub/Sub on upload. You want to minimize operational
overhead while ensuring all files are processed correctly. What GCP compute service would you use?

        a). Anthos
        b). Compute Engine
        c). App Engine Standard
        d). Cloud Run

        Correct: d

        Explanation:
            Cloud Run can execute container images with custom applications written in any programming
            language. It is a managed service so operational overhead is minimized. Cloud Pub/Sub
            configured with a push subscription could invoke a service running in Cloud Run. Compute
            Engine is not a managed service and would have more operational overhead. App Engine
            Standard does not support C++ applications. Anthos is a platform for managing multiple
            Kubernetes clusters in multiple environments and while it could be used to run the service, it is
            more than required by the specifications.

    ---

25. A startup is deploying analytical services for Internet of Things (IoT) applications. The
service will need to ingest large volumes of time series data in short periods of time. Users
will query the data is a few different ways but those ways are known and fixed. What
managed GCP database service would you recommend?

        a). Bigtable
        b). Cloud Spanner
        c). Cloud SQL
        d). BigQuery

        Correct: a

        Explanation:
            Bigtable is a NoSQL wide-column database well suited to low latency writes. Since only a few,
            well defined query patterns are needed, you can design the data model to support those patterns.
            BigQuery does not support large volumes of low latency writes. Cloud SQL and Cloud Spanner
            are relational databases designed for transaction processing systems but this use case does not
            require a transaction processing system. 
    Reference: <a target="_blank" href=https://cloud.google.com/bigtable/docs/overview>https://cloud.google.com/bigtable/docs/overview</a>

    ---

26. A colleague has asked you to help them better managed multiple files in Cloud Storage.
They would like to automate as much of the management as possible. You recommend
using lifecycle management policies. What operations can be automatically performed
using lifecycle policy management?

        a). Move files
        b). Delete
        c). Set storage class
        d). Enable versioning
        e). Copy files

        Correct: b, c

        Explanation:
            The two operations that can be performed using Cloud Storage lifecycle management are
            deleting objects and setting the storage class. Moving files and enabling versioning are not
            available in lifecycle management policies.
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/lifecycle>https://cloud.google.com/storage/docs/lifecycle</a>

    ---

27. The CFO of your company is concerned that BigQuery costs are growing too large. They
ask for recommendations on how to reduce the cost of querying without reducing the utility
of the service. Most of the queries are based on the time the data arrived. What would you
recommend as one way to reduce the amount of data scanned?

        a). Use the LIMIT option in SELECT statements to prevent more than a fixed number of rows from being
            returned.
        b). Use covering indexes to respond to queries using only the index without needing to seek additional
            blocks of data.
        c). Use ingestion time partitioned tables and specify _PARTITIONTIME filters when querying.
        d). Use read replicas and query only the read replica not the primary, which is where data is written.

        Correct: c

        Explanation:
            Ingestion time partitioned tables creates partitions by ingestion time. The pseudo column
            _PARTITIONTIME is added to the table and can be used to restrict the amount of data scanned.
            BigQuery does not provide for read replicas like some databases. BigQuery does not use indexes.
            The LIMIT option does not reduce the amount of data scanned, it only limits the number of rows 
            returned.

    ---

28. Your most recent GCP bill is higher than expected because of a significant increase in
storage charges. Your department recently enabled an audit log that is off by default for
most services. You think that audit logging may be responsible for the increased storage
charges. Which type of audit log would you think could be responsible?

        a). Policy Denied Audit Log
        b). System Event Audit Log
        c). Data Access Audit Log
        d). Admin Activity audit logs

        Correct: c

        Explanation:
            Data Access Audit logs generate large amounts of data and are disabled by default for most
            services; it is enabled by default for BigQuery. The other audit logs are not likely to generate the
            same volume of data as the Data Access Audit logs. 
    Reference: <a target="_blank" href=https://cloud.google.com/logging/docs/audit>https://cloud.google.com/logging/docs/audit</a>

    ---

29. You are setting up a service in Kubernetes Engine. You would like to have all internal
clients send request to a stable internal IP address. What type of service would you create?

        a). LoadBalancer
        b). ClusterIP
        c). Headless
        d). NodePort

        Correct: b

        Explanation:
            ClusterIP service is the default type of service and is used to enable internal clients to send
            requests to a stable internal IP address. Headless service type is used when a stable IP address is
            not needed. NodePort is used to enable clients to send requests to the IP address of a node on one
            or more nodePort values specified by the service. LoadBalancer clients send request to the IP
            address of a network load balancer. 
    Reference: <a target="_blank" href=https://cloud.google.com/kubernetes-engine/docs/concepts/service>https://cloud.google.com/kubernetes-engine/docs/concepts/service</a>

    ---

30. A data scientist is running several large queries against BigQuery. They would like to know
how much the query will cost before running the query. How would recommend they do that?

        a). Use the bq query command with the --dry_run flag
        b). Use the bq query command with the --cost flag
        c). Use the bq query command with the --limit parameter and the --scan parameter
        d). Use the bq query command with the --estimate-cost flag

        Correct: a

        Explanation:
            The --dry_run flag is used with the bq query command to estimate the cost of running a query.
            bq does not have --estimate-cost or --cost flags. There is --scan parameter in bq. Limit can be
            used with SQL queries to limit the number of rows returned but it does not limit the amount of
            data scanned. Since it is the amount of data scanned, not returned, that determines cost, using a
            limit statement will not help reduce cost.
    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/best-practices-costs>https://cloud.google.com/bigquery/docs/best-practices-costs</a>

    ---

31. You are administering a project that uses BigQuery. You would like to list all the datasets
in the project. What command would you use?

        a). bq ls
        b). gsutil ls
        c). gsutil dir
        d). bq dir

        Correct: a

        Explanation:
            BigQuery uses the bq command line and the command to list datasets is bq ls. bq dir is not a
            valid bq command. Gsutil is the command line utility used with Cloud Storage not BigQuery.
    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/reference/bq-cli-reference>https://cloud.google.com/bigquery/docs/reference/bq-cli-reference</a>

    ---

32. You believe you may have over provisioned several VMs. You would like to get data on the
CPU load at 15 minute intervals from all Linux servers. How would you do this with the least amount of work?

        a). Install the Prometheus agent on each server and monitor the load_15m metric.
        b). Install a bash script that uses the sar -u command to get CPU utilization and write the value to sysout.
        c). Install the Cloud Monitoring agent on each server and monitor the load_15m metric.
        d). Install a bash script that uses the sar -u command to get CPU utilization and write the value to syslog.

        Correct: c

        Explanation:
            The Cloud Monitoring agent collects data on CPU utilization and other metrics. Installing the
            agent and then view the collected data with Cloud Monitoring requires the least amount of work.
            Installing a bash script that uses the sar -u command to get CPU utilization and write the value to
            syslog or sysout would work but would require you to write and maintain the script. Prometheus
            is an open source monitoring tool that could be used but you would need to install, configure,
            and maintain it.
    Reference: <a target="_blank" href=https://cloud.google.com/monitoring/agent/installation>https://cloud.google.com/monitoring/agent/installation</a>

    ---

33. You have deployed a service using App Engine that requires a batch job run every hour.
You notice that the batch job is running every two hours instead of every hour. You'd like
to change the job specification to correct the problem. What file would you edit to correct the problem?

        a). app.yaml
        b). batch.yaml
        c). job.yaml
        d). cron.yaml

        Correct: d 

        Explanation:
            Cron.yaml files contain specifications for running scheduled jobs in App Engine. App.yaml has
            overall application specifications. Batch.yaml and job.yaml are not specified as part of App
            Engine services. 
    Reference: <a target="_blank" href=https://cloud.google.com/appengine/docs/flexible/python/scheduling-jobs-with-cron-yaml>https://cloud.google.com/appengine/docs/flexible/python/scheduling-jobs-with-cron-yaml</a>

    ---

34. You want to create an autoscaling Kubernetes cluster in Kubernetes Engine. Which of the
following commands would you specify?

        a). kubectl containers create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.
        b). gcloud container clusters create with --enable-autoscaling flag and --min-nodes and maxnodes parameters.
        c). gcloud kubernetes clusters create with --enable-autoscaling flag and --min-nodes and maxnodes parameters.
        d). kubectl clusters create with --enable-autoscaling flag and --min-nodes and max-nodes parameters.

        Correct: b

        Explanation:
            The correct command is gcloud container clusters create with --enable-autoscaling flag and --min-nodes
            and max-nodes parameters. Kubectl is a command line for managing resources, such as pods, within a
            Kubernetes cluster so the options kubectl clusters create with --enableautoscaling flag and
            --min-nodes and max-nodes parameters and kubectl containers create with --enable-autoscaling flag and
            --min-nodes and max-nodes parameters are incorrect. The option gcloud kubernetes clusters create with
            --enable-autoscaling flag and --min-nodes and max-nodes parameters is incorrect because it specifies
            gcloud kubernetes instead of gcloud containers.
            (Kubernetes Engine was originally named Container Engine. When the service name was changed, the gcloud
            command was not changed to reflect the new service name). 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/container/clusters/create>https://cloud.google.com/sdk/gcloud/reference/container/clusters/create</a>

    ---

35. You need to deploy a load balancer that will support external clients using TCP traffic,
including SSL. You want to offload SSL processing. What load balancer would you deploy?

        a). SSL Proxy
        b). The explanation was pasted here. Was "Internal HTTP(S) Load Balancing" supposed to go here, like
            the question below?
        c). TCP Proxy
        d). Network TCP/UDP Load Balancing

        Correct: a

        Explanation:
            The correct answer is the SSL Proxy, which should be used for external TCP traffic with the SSL
            processing offloaded to the the proxy. Network TCP/UDP Load Balancing is used for internal TCP traffic.
            A network load balancer distributes TCP or UDP traffic among virtual machine (VM) instances in the same
            region.
    Reference: <a target="_blank" href=https://cloud.google.com/loadbalancing/docs/load-balancing-overview>https://cloud.google.com/loadbalancing/docs/load-balancing-overview</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/loadbalancing/docs/choosing-load-balancer>https://cloud.google.com/loadbalancing/docs/choosing-load-balancer</a>

    ---

36. You have created a virtual private cloud (VPC) in auto mode, which automatically creates
a subnet in each region. How is the CIDR block determined for each region?

        a). Each region will automatically be assigned a set of predefined IP ranges that fit within the
            10.128.0.0/9 CIDR block.
        b). You will specify non-overlapping CIDR blocks for each region.
        c). You will specify non-overlapping CIDR ranges for the set of regions you want a subnet created for.
        d). Each region will be automatically assigned a range of external IP addresses.

        Correct: a

        Explanation:
            When using auto mode VPC creation, a subnet is created in each region and each subnet is assigned a
            range of IP addresses that fit within the 10.128.0.0/9 CIDR block. You do not have to specify CIDR
            blocks in auto mode so both of the options, You will specify non-overlapping CIDR blocks for each
            region and You will specify non-overlapping CIDR ranges for the set of regions you want a subnet
            created for, are incorrect. External addresses are not assigned in auto mode, so the option each
            region will be automatically assigned a range of external IP addresses is incorrect. 
    Reference: <a target="_blank" href=https://cloud.google.com/vpc/docs/using-vpc>https://cloud.google.com/vpc/docs/using-vpc</a>

    ---

37. A colleague who is new to GCP has asked for your help with understanding predefined
roles. They would like to know details about several predefined roles. What command
would you suggest they use? [ROLE-ID] indicates where to specify the role identifier in the command.

        a). gcloud iam roles describe [ROLE-ID]
        b). gcloud roles predefined describe [ROLE-ID]
        c). gcloud iam roles list [ROLE-ID]
        d). gcloud roles predefined describe [ROLE-ID]

        Correct: a 

        Explanation:
            gcloud iam roles describe [ROLE-ID] is the correct command for displaying information about a role.
            The options gcloud roles predefined describe [ROLE-ID] and gcloud roles predefined describe [ROLE-ID]
            are missing the term iam, which is needed to indicate the gcloud command is for the Identity and
            Access Management service. The option gcloud iam roles list [ROLE-ID] uses list instead of describe.
            List is typically used to see short descriptions of multiple resources while describe is typically
            used to see more detailed information about a resource. 
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/iam/roles/describe>https://cloud.google.com/sdk/gcloud/reference/iam/roles/describe</a>

    ---

38. Your team uses a number of custom images. You want to be able to release new versions of
each image while still maintaining the ability to rollback to a previous version if needed.
What feature of Compute Engine would you use for this purpose?

        a). community supported images
        b). managed instance groups
        c). image families
        d). unmanaged instance groups

        Correct: c

        Explanation:
            Image families are used to group related images together so you can roll forward or back
            between specific images versions. Image families always point to the latest version of an image
            that is not deprecated. Managed and unmanaged instance groups are types of clusters, not an
            image management feature. Community supported images not directly supported by Compute
            Engine and are maintained by community members. 

    ---

39. You are hosting a large amount of image and video content for an educational service.
Learners from around the world use the service. You currently host content on servers in
your own data center in North America. Learners in Asia, Africa, and Europe experience
long latencies loading content. What GCP service could you use to ensure that all learners
experience the same level of latency and the latency is kept low, especially for frequently
accessed content?

        a). Persistent disks
        b). Cloud CDN
        c). Cloud Storage Nearline Storage Class
        d). Cloud VPN

        Correct: b

        Explanation:
            Cloud CDN is a content distribution network for global content delivery. It caches data at
            distributed points around the world so users requests for content are routed to the closest content
            location. Cloud Storage Nearline Storage Class is appropriate for content that is only accessed
            once or less per month. Cloud VPNs are used to link Google Cloud network to external networks,
            such as an on premises data center network. Persistent disks are used to store data on virtual
            machines and could be used if you were to deploy and manage VMs across multiple regions but that
            would be less efficient than using Cloud CDN. 
    Reference: <a target="_blank" href=https://cloud.google.com/cdn/docs/overview>https://cloud.google.com/cdn/docs/overview</a>

    ----

40. Due to security concerns, you want to ensure all data written to your Cloud Storage
buckets are encrypted. What do you need to do to ensure data is encrypted when stored in Cloud Storage?

        a). Set up customer managed encryption keys and use those keys to encrypt data before saving to Cloud Storage.
        b). Set a lifecycle policy that specifies encryption is on.
        c). Use the --encrypt flag with gsutil
        d). Nothing, this is the default behavior.

        Correct: d

        Explanation:
            All data stored in Google Cloud is encrypted before it is persisted. You do not have to do
            anything to ensure your data is encrypted at rest in GCP. You may set up customer managed
            encryption keys if you want to control how keys are managed but it is not necessary. There is no
            --encrypt flag with gsutil. There is no encryption option with lifecycle management policies. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/encryption>https://cloud.google.com/storage/docs/encryption</a>

    ---

41. A startup is developing an Internet of Things (IoT) service. When data is first ingested,
some basic data quality checks are performed that ensure the format is correct. The checks
are simple Python functions that apply regular expression checks. The data will be ingested
using Pub/Sub. When new data arrives, it should be automatically have the quality checks
applied. The checks will always run for less than one second. What compute service would
you use to apply the data quality checks?

        a). App Engine Standard
        b). Compute Engine
        c). Cloud Functions
        d). App Engine Flexible

        Correct: c

        Explanation:
            Cloud Functions are the best option since it is a managed service that can be invoked on events,
            such as when a message is ingested by Cloud Pub/Sub. Cloud Functions support Python. Also
            the code to execute runs for short periods of time. Compute Engine could be used but you would
            be charged for time the VM is running even if it were not processing data and would require
            more management than Cloud Functions, which is serverless. App Engine Standard and App
            Engine Flexible could be used but they provide more functionality than is needed to run simple
            Python functions applying regular expression checks and require more configuration than Cloud Functions.
    Reference: <a target="_blank" href=https://cloud.google.com/functions/docs/concepts/overview>https://cloud.google.com/functions/docs/concepts/overview</a> <br>
    Reference: <a target="_blank" href=https://cloud.google.com/functions/docs/tutorials/pubsub>https://cloud.google.com/functions/docs/tutorials/pubsub</a>

    ---

42. A team providing business intelligence solutions to your company is migrating to GCP.
They make extensive use of SQL and want to continue to use SQL. They currently use
relational databases to store data. Data is loaded every night. When data is older than 3
years, it is no longer needed. They expect the database to grow to 100 GB within six
months. Most of the operations on the database query a few columns but scan many rows.
They also want to minimize database management overhead. What GCP service would you
recommend they use?

        a). Bigtable
        b). BigQuery
        c). Cloud Firestore
        d). Cloud SQL

        Correct: b

        Explanation:
            BigQuery is the best option. BigQuery is a managed analytical database that supports SQL. It is
            optimized for write once/read many operations. It can easily store 100 GB or more of data. It is a
            managed service designed to support data warehouses. Bigtable and Cloud Firestore are NoSQL
            databases and do not support SQL. Cloud SQL does support SQL but it is designed for
            transaction processing and does not support up to 100 GB in a single database. 
    Reference: <a target="_blank" href=https://cloud.google.com/solutions/migration/dw2bq/dw-bq-migrationoverview>https://cloud.google.com/solutions/migration/dw2bq/dw-bq-migrationoverview</a>

    ---

43. To improve security of your applications, you want to create several custom roles with
limited permissions. What role would give you sufficient permission to create custom roles?

        a). roles/iam.roles.create.custom
        b). roles/iam.serviceAccountUser
        c). roles/iam.roles.create
        d). roles/iam.serviceAccountUser.create

        Correct: c

        Explanation:
            The role roles/iam.roles.create will provide the permissions required to create custom roles.
            roles/iam.roles.create.custom is not a valid option. roles/iam.serviceAccountUser is used to grant
            an identity access to a service account. roles/iam.serviceAccountUser.create is not a valid option.
    Reference: <a target="_blank" href=https://cloud.google.com/iam/docs/creating-custom-roles>https://cloud.google.com/iam/docs/creating-custom-roles</a>
    Reference: <a target="_blank" href=https://cloud.google.com/iam/docs/understanding-custom-roles>https://cloud.google.com/iam/docs/understanding-custom-roles</a>

    ---

44. A system admin needs to be able to create an instance that runs as a service account,
attaches a persistent disk to an instance that runs as a service account, and set instance
metadata on an instance that runs as a service account. Which of the following roles are
required to meet those requirements?

        a). roles/compute.instanceAdmin.v1
        b). roles/compute.imageUser
        c). roles/compute.storageAdmin
        d). roles/iam.serviceAccountCreator
        e). roles/iam.serviceAccountUser

        Correct: a, e

        Explanation:
            2 roles are required: roles/compute.instanceAdmin.v1 and roles/iam.serviceAccountUser. The
            roles/compute.instanceAdmin.v1 role gives full control of Compute Engine instances, instance
            groups, disks, snapshots, and images. The roles/iam.serviceAccountUser role gives permission to
            run operations as the service account. roles/compute.storageAdmin gives only permissions to
            create, modify, and delete disks, images, and snapshots, which are available by
            roles/compute.instanceAdmin.v1. roles/iam.serviceAccountCreator gives permission to create
            service accounts. 
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/access/iam>https://cloud.google.com/compute/docs/access/iam</a>

    ---

45. You are considering running a Windows server in GCP. You would like to review a list of
Windows Server images available. What command would you use?

        a). gcloud compute list windows-cloud
        b). gcloud compute images list --project windows-cloud --no-standard-images
        c). gcloud compute images describe --project windows-cloud --no-standard-images
        d). gcloud compute instances describe windows-cloud

        Correct: b

        Explanation:
            The command gcloud compute images list --project windows-cloud --no-standard-images will
            list Windows Server images. List provides a list of images with minimal information. Describe is
            used to show more detailed information. The options gcloud compute list windows-cloud, gcloud
            compute images describe --project windows-cloud --no-standard-images, and gcloud compute instances
            describe windows-cloud are not a valid gcloud command, the term windows-cloud is not used in gcloud
            compute commands.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/images/list>https://cloud.google.com/sdk/gcloud/reference/compute/images/list</a>

    ---

46. You have just taken over responsibility to manage a large number of objects in Cloud
Storage. You are reviewing a random sample of objects and want to know the creation time
and content type for those objects. You plan to write a shell script to display this data.
What command would you use in your script to retrieve that metadata?

        a). gsutil stat gs://BUCKET_NAME/OBJECT_NAME
        b). gsutil list gs://BUCKET_NAME/OBJECT_NAME
        c). gsutil metadata gs://BUCKET_NAME/OBJECT_NAME
        d). gsutil describe gs://BUCKET_NAME/OBJECT_NAME

        Correct: a

        Explanation:
            The correct command to list that metadata is gsutil stat gs://BUCKET_NAME/OBJECT_NAME.
            gsutil metadata is not a valid gsutil command. gsutil list is not a valid command, instead gsutil ls
            is used to list bucket information. gsutil describe is not a valid command. Describe is often used
            with gcloud commands, but not gsutil. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/gsutil/commands/stat>https://cloud.google.com/storage/docs/gsutil/commands/stat</a>

    ---

47. A client of yours needs to be sure that only applications from the same project run on a
physical server. For example, two applications from Project A may run on VMs deployed
to a single physical server but an application from Project A and Project B will not be
deployed to VMs that are running the same physical server. What feature of Compute
Engine would you recommend?

        a). Preemptible VMs
        b). Sole-tenant nodes
        c). Managed instance groups
        d). Shielded VMs

        Correct: b 

        Explanation:
            Sole-tenant nodes provide for exclusive access to a physical server. Shielded VMs provide
            additional security protections but do not guarantee sole-tenancy. Managed instance groups is a
            set of identically configured VMs. Preemptible VMs are low cost VMs that may be shutdown at
            any time by Google. 
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes>https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes</a>

    ---

48. A team of data scientists wants to migrate an on premises Spark cluster to Google Cloud.
They would like to use a managed service. What GCP service would you recommend?

        a). Cloud Dataproc
        b). Cloud Dataflow
        c). Cloud Bigtable
        d). Cloud Data Studio

        Correct: a

        Explanation:
            Cloud Dataproc is a managed Spark/Hadoop cluster service. Cloud Data Studio is a reporting
            and analytics tool. Cloud Dataflow is a batch and stream processing platform. Cloud Bigtable is
            a NoSQL database.
    Reference: <a target="_blank" href=https://cloud.google.com/dataproc/docs/concepts/overview>https://cloud.google.com/dataproc/docs/concepts/overview</a>

    ---

49. You would like to use SSH host keys on your VMs to improve security. What feature of
Compute Engine VMs do you need to enable to store SSH host keys?

        a). Shielded VMs
        b). labels
        c). Sole-tenant nodes
        d). guest attributes

        Correct: d

        Explanation:
            The correct answer is guest attributes. When guest attributes are enabled, Compute Engine will
            store your generated host keys as guest attributes. Sole-tenant nodes provides for exclusive
            access to a physical server. Shielded VMs provide additional security protections but do not
            guarantee sole-tenancy. Labels allow you to specify key-value pairs for grouping resources, for
            example, a VM cloud be labeled with the key value pair 'envior:production.'
    Reference: <a target="_blank" href=https://cloud.google.com/solutions/connecting-securely>https://cloud.google.com/solutions/connecting-securely</a>

    ---

50. You are running several services in Cloud Run. You will need to programmatically
determine the name of the configuration that created the container. Where would you find this?

        a). In the container startup script
        b). In the service startup script
        c). In the K_Configuration environment variable
        d). In the VM instance metadata

        Correct: c

        Explanation:
            When Cloud Run starts a container, it creates environment variables: K_Configuration,
            K_Revision, K_Service, and Port. K_Configuration specifies the configuration that created the
            container. When using Docker containers, you specify a command to execute on startup using
            the CMD command in a Dockerfile configuration. Container startup or service startup scripts do
            not necessarily set a standard environment variable for storing metadata, such as the name of the
            configuration used with Cloud Run. VM instance data is incorrect because Cloud Run is
            serverless and we do not have access to underlying VMs. 
    Reference: <a target="_blank" href=https://cloud.google.com/run/docs/reference/container-contract>https://cloud.google.com/run/docs/reference/container-contract</a>

---     
[<h3 style="text-align: center;font-family: cursive;">Next Page</h3>](gcp-ace-3.md) 

---         
<br>
{!footer.md!}

