# Google Cloud Associate Cloud Engineer Practice Exam 1 : 

<br>
These are GCP ACE(Google Cloud Platform Associate Cloud Engineer) certification practice questions for professionals who are aspired to be GCP ACE certified. You will find these questions very helpful in your GCP-ACE certification and interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---

1. You have a Cloud Datastore database that you would like to backup. You'd like to issue a
command and have it return immediately while the backup runs in the background. You
want the backup file to be stored in a Cloud Storage bucket named my-datastore-backup.
What command would you use?

        a). gcloud datastore backup gs://my-datastore-backup
        b). gsutil datastore export gs://my-datastore-backup --async
        c). gcloud datastore export gs://my-datastore-backup
        d). gcloud datastore export gs://my-datastore-backup --async

        Correct: d

        Explanation:
            The correct command is gcloud datastore export gs://my-datastore-backup --async. Export, not
            backup, is the datastore command to save data to a Cloud Storage bucket. Gsutil is used to
            manage Cloud Storage, not Cloud Datastore.
    Reference: <a target="_blank" href=https://cloud.google.com/datastore/docs/export-import-entities>https://cloud.google.com/datastore/docs/export-import-entities</a>

    ---

2. Your organization has created multiple folders, one for each department. In each folder,
departments have one or more projects. What would you expect resources within the folder
to share?

        a). Service accounts
        b). IAM policies
        c). IAM roles
        d). Permissions

        Correct: b

        Explanation:
            Folders are used to group resources that share common IAM policies. Service accounts are
            specific to a set of operating requirements within a project. Permissions are associated with roles
            but not directly with folders. IAM roles are granted to identities, not folders. 

      Reference: <a target="_blank" href=https://cloud.google.com/resource-manager/docs/creating-managing-folders>https://cloud.google.com/resource-manager/docs/creating-managing-folders</a>

    ---

3. As a consultant to a mid-sized retailer you have been asked to help choose a managed
database platform for the company's inventory management application. The retailer's
market is limited to the Northeast United States. What service would you recommend?

        a). Bigtable
        b). Cloud Dataproc
        c). Cloud Spanner
        d). Cloud SQL

        Correct: d

        Explanation:
            Cloud SQL is a managed relational database service suitable for regionally used applications.
            Cloud Spanner is also a managed relational database but it is designed for multi-region and
            global applications. BigQuery is not used for transaction processing systems. Cloud Dataproc is
            a managed Spark/Hadoop service, not a relational database. For more information, see
    Reference: <a target="_blank" href=https://cloud.google.com/sql/docs>https://cloud.google.com/sql/docs</a>

    ---

4. An auditor is reviewing your GCP use. They have asked for access to any audit logs
available in GCP. What audit logs are available for each project, folder, and organization?

        a). Admin Activity
        b). User Login
        c). Performance Metrics
        d). System Event
        e). Data Access
        f). Policy Access

        Correct: a, d, e

        Explanation:
            Cloud Audit Logs maintain three audit logs: Admin Activity logs, Data Access logs, and System
            Event logs. There is no such thing as a Policy Access log, a User Login log, or a Performance
            Metric log in GCP Audit Logs.
    Reference: <a target="_blank" href=https://cloud.google.com/logging/docs/audit>https://cloud.google.com/logging/docs/audit</a>

    ---

5. A developer is trying to upload files from their local device to a Compute Engine VM using
the gcloud scp command. The copy command is failing. What would you check to try to
correct the problem?

        a). Grant the identity the roles/compute.admin role
        b). Add the identity of the developer to the administrator group for the VM.
        c). Grant the identity compute.admin permission
        d). Ensure firewall rules allow traffic to port 22 to allow SSH connections. 

        Correct: d

        Explanation:
            To copy files to a VM, a firewall rule must be in place to allow traffic on port 22, the default
            SSH port. Administrator privileges are not needed to upload a file so the other three options are
            not correct. For more information, see https://cloud.google.com/compute/docs/instances/transferfiles.
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/instances/transferfiles>https://cloud.google.com/compute/docs/instances/transferfiles</a>

    ---

6. A group of data scientists need access to data stored in Cloud Bigtable. You want to follow
Google recommended best practices for security. What role would you assign to the data
scientist to allow them to read data from Bigtable?

        a). roles/bigtable.owner
        b). roles/bigtable.reader
        c). roles/bigtable.user
        e). roles/bigtable.admin

        Correct: b

        Explanation:
            The role/bigtable.reader gives the data scientist the ability to read data but not write data or
            modify the database. This follows the Principle of Least Privilege as recommended by Google.
            Roles/bigtable.admin gives permissions to administer all instances in a project, which is not
            needed by a data scientist. Roles/bigtable.user provides read and write permissions but data
            scientist do not need read permission. There is no predefined role called roles/bigtable.owner.
    Reference: <a target="_blank" href=https://cloud.google.com/bigtable/docs/access-control>https://cloud.google.com/bigtable/docs/access-control</a>

    ---

7. You want to load balance an application that receives traffic from other resources in the
same VPC. All traffic is TCP with IPv4 addresses. What load balancer would you
recommend?

        a). Internal TCP/UDP Load Balancing
        b). SSL Proxy Load Balancing
        c). TCP Proxy Load Balancing
        d). Network TCP/UDP Load Balancing 

        Correct: a

        Explanation:
            Internal TCP/UDP Load Balancing is used for internal traffic, that is not from the internet. SSL
            Proxy, TCP Proxy, and Network TCP/UDP load balancing are used with external traffic. 
    Reference: <a target="_blank" href=https://cloud.google.com/load-balancing/docs/choosing-load-balancer>https://cloud.google.com/load-balancing/docs/choosing-load-balancer</a>

    ---

8. You want to deploy an application to a Kubernetes Engine cluster using a manifest file
called my-app.yaml. What command would you use?

        a). gcloud containers deployment apply my-app.yaml
        b). kubectl apply -f my-app.yaml
        c). gcloud deployment apply my-app.yaml
        d). kubectl deployment apply my-app.yaml

        Correct: b

        Explanation:
            The correct answer is to use the "kubectl apply -f" with the name of the deployment file.
            Deployments are Kubernetes abstractions and are managed using kubectl, not gcloud. The other
            options are not valid commands.
    Reference: <a target="_blank" href=https://kubernetes.io/docs/reference/kubectl/overview/>https://kubernetes.io/docs/reference/kubectl/overview/</a>

    ---

9. A photographer wants to share images they have stored in a Cloud Storage bucket called
free-photos-on-gcp. What command would you use to allow all users to read these files?

        a). gsutil ch allUsers:Viewer gs://free-photos-on-gcp
        b). gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp
        c). gcloud ch allUsers:objectViewer gs://free-photos-on-gcp
        d). gcloud iam ch allUsers:Viewer gs://free-photos-on-gcp

        Correct: b

        Explanation:
            The correct command is gsutil iam ch allUsers:objectViewer gs://free-photos-on-gcp. Gsutil is
            used with Cloud Storage, not gcloud so the gcloud ch option is incorrect. The term objectViewer
            is the correct way to grant read access to objects in a bucket.
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/gsutil/commands/iam>https://cloud.google.com/storage/docs/gsutil/commands/iam</a>

    ---

10. Your department runs a legacy application on an on premises cluster. The nodes in the
cluster are heterogeneous. You want to migrate this cluster to Google Cloud. What
Compute Engine resource would you use?

        a). Autoscaler
        b). Managed instance groups (MIGs)
        c). Network load balancer
        d). Unmanaged instance group

        Correct: d 

        Explanation:
            Heterogeneous clusters can be run on unmanaged instance groups but not managed instance groups. 
            Network load balancer is used to distribute workload in a cluster but it is not an instance group 
            itself. Autoscaler adds and removes nodes in a managed instance group as needed.
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-unmanaged-instances>https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-unmanaged-instances</a>

    ---

11. You have created a Kubernetes Engine cluster that will run machine learning training
processes and machine learning prediction processes. The training processes require more
CPU and memory than the prediction processes. How would you configure the cluster to
support this?

        a). Increase the number of replica sets for the machine learning training process.
        b). Use two node pools, one configured with more CPU and memory than the other.
        d). Use multiple pods with some configured for more CPU and memory.
        c). Increase the number of deployments for the machine learning training process.

        Correct: b

        Explanation:
            Node pools are used to configure resources for particular workloads. All nodes in a node pool are
            configured the same. Replica sets and deployments do not control the number of CPUs or amount of memory.

    ---

12. You will be creating a GKE cluster and want to use Cloud Operations for GKE instead of
legacy monitoring and logging. If you create the cluster using a gcloud container clusters
create command, what parameter would you specify to explicitly enable Cloud Operations
for GKE?

        a). --enable-gke-monitor
        b). --disable-legacy-monitoring
        c). --enable-cloud-operations
        d). --enable-stackdriver-kubernetes

        Correct: d

        Explanation:
            The correct way to enable Cloud Operations for GKE is to use the parameter --enablestackdriver-kubernetes.
            The other options are not valid parameter names.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/container/clusters/create>https://cloud.google.com/sdk/gcloud/reference/container/clusters/create</a>

    ---

13. A client of yours has a Python 3 application that usually has very little load but sometimes
experiences sudden and extreme spikes in traffic. They want to run it in GCP but they
want to keep costs as low as possible. They also want to minimize management overhead.
What service would you recommend?

        a). Kubernetes Engine
        b). Compute Engine
        c). App Engine
        d). Cloud Functions

        Correct: c

        Explanation:
            App Engine is designed for applications written in supported languages, including Python 3, that
            need to run at low cost, and need to scale in response to rapid increases in load. App Engine is a
            managed service and as such minimizes operational overhead . Compute Engine and Kubernetes
            Engine both require more management overhead. Cloud Functions are used to respond to events
            in GCP, not to execute a continually running application. 
    Reference: <a target="_blank" href=https://cloud.google.com/appengine/docs/standard>https://cloud.google.com/appengine/docs/standard</a>

    ---

14. During an audit, auditors determined that there are insufficient access controls on Cloud
Storage buckets. The auditors recommend you use uniform bucket-level access. After
applying uniform bucket-level access some users that had access to objects in buckets no
longer have access. What could be the cause?

        a). Applying uniform bucket-level access removes all access privileges. No user will have access
            until permissions are reset.
        b). Users do not have permissions through ACLs that allow them access to objects in buckets.
            Prior to setting uniform bucket-level access, those users had access through IAM.
        c). Users do not have IAM permissions that allow them access to objects in buckets. Prior to
            setting uniform bucket-level access, those users had access through ACLs.
        d). ACLs are removed when uniform bucket-level access is applied. ACLs must be recreated.

        Correct: c

        Explanation:
            Access is granted to Cloud Storage objects using IAM or access control lists (ACLs). When
            uniform bucket-level access is applied, users only have access through IAM roles and
            permissions. A users that could access objects before uniform bucket-level access is applied but
            not after must have had access through ACLs. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/uniform-bucket-level-access>https://cloud.google.com/storage/docs/uniform-bucket-level-access</a>

    ---

15. A startup has an app that allows users to upload images to Cloud Storage. The images
should be analyzed as soon as possible once they are loaded. Processing takes
approximately 1 second for each image. There are periods when no images are uploaded
and other times when many images are upload in short periods of time. What compute
option would you use to process images?

        a). Compute Engine
        b). Kubernetes Engine
        c). App Engine Flexible
        d). Cloud Functions

        Correct: d

        Explanation:
            Cloud Functions is used to respond to events in GCP, including uploading of files in Cloud
            Storage. Processing can finish within the time limits Cloud Functions must run. Since there are
            periods when no images are uploaded, there is no need to have an application running
            continuously and checking for new image uploads so App Engine Flexible, Cloud Engine, and
            Kubernetes Engine are more than required.
    Reference: <a target="_blank" href=https://cloud.google.com/functions/docs/how-to>https://cloud.google.com/functions/docs/how-to</a>

    ---

16. A client has asked for your advice about building a data transformation pipeline. The
pipeline will read data from Cloud Storage and Cloud Spanner, merge data from the two
sources and write the data to a BigQuery data set. The client does not want to manage
servers or other infrastructure, if possible. What GCP service would you recommend?

        a). Cloud Dataprep
        b). Compute Engine
        c). Cloud Data Fusion
        d). Cloud Build

        Correct: c

        Explanation:
            Cloud Data Fusion is a managed service that is designed for building data transformation
            pipelines. Compute Engine is not a managed service. Cloud Dataprep is used to prepare data for
            analytics and machine learning. Cloud Build is a service for creating container images.
    Reference: <a target="_blank" href=https://cloud.google.com/data-fusion/docs/how-to>https://cloud.google.com/data-fusion/docs/how-to</a>

    ---

17. You want to clone a persistent disk. What characteristics of the source and cloned disk
must be the same?

        a). Zone
        b). disk type
        c). Region
        d). Size

        Correct: a, b, c 

        Explanation:
            The source and cloned disk must be in the same zone and region and must be of the same type.
            The size of the clone must be at least the size of the source disk but does not need to be the same.
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/disks/create-snapshots>https://cloud.google.com/compute/docs/disks/create-snapshots</a>

    ---

18. You have a set of snapshots that you keep as backups of several persistent disks. You want
to know the source disk for each snapshot. What command would you use to get that information?

        a). gcloud compute disk describe
        b). gcloud compute snapshots list
        c). gcloud compute snapshots describe
        d). gcloud snapshots describe

        Correct: c

        Explanation:
            The correct command is gcloud compute snapshots describe which shows information about the
            snapshot, including source disk, creation time, and size. The other options are not valid gcloud
            commands.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/snapshots/describe>https://cloud.google.com/sdk/gcloud/reference/compute/snapshots/describe</a>

    ---

19. The CFO of you company feels you are spending too much on BigQuery. You determine
that a few long running queries are costing more than they should. You would like to
experiment with different ways of writing these queries. You'd like to know the estimated
cost of running each query without actually running them. How could you do this?

        a). Use the --estimate-cost option with the bq command.
        b). Use the --dry-run option with a bq query command.
        c). Use the --estimate-cost with the gcloud command.
        d). Use the Pricing Calculator.

        Correct: b

        Explanation:
            The correct answer is to use the --dry-run option with the bq select command. The Pricing
            Calculator can give you an estimate of aggregate costs based on storage and amount of data
            queried but it does not provide estimates of a the cost of running a specific query. There is no
            --estimate-cost option with either the bq or gcloud command.
    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/estimate-costs>https://cloud.google.com/bigquery/docs/estimate-costs</a>

    ---

20. You are using HTTP(S) Load Balancing for a Web application that has several services.
Depending on the URL specified by a user, requests are routed to different backend
services. What would you use to specify how those request should be routed?

        a). URL maps
        b). Routes
        c). Traces
        d). Firewall rules

        Correct: a

        Explanation:
            URL maps specify direct requests to particular services. Routes are used to specify paths to
            destination IP addresses outside a subnet. Firewall rules control the flow of traffic on a network.
            Traces are used to understand performance characteristics of services in a distributed system. 
    Reference: <a target="_blank" href=https://cloud.google.com/load-balancing/docs/url-map>https://cloud.google.com/load-balancing/docs/url-map</a>

    ---

21. An application running in Compute Engine sometimes gets spikes in load. You want to add
instances automatically when load increases significantly and plan to use managed instance
groups. What would you need to create in order to automatically scale the cluster?

        a). Persistent Disk
        b). Snapshot
        c). Load balancer
        d). Instance template

        Correct: d

        Explanation:
            An instance template is needed to enable Compute Engine to automatically add instances to a
            managed instance group. Snapshots are not required to add instances to a managed instance
            group. Persistent disks are not needed to control the addition of nodes to a managed instance
            group. Load balancers are used with managed instance groups but are not the thing that
            automatically adds nodes to the managed instance group.
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances>https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances</a>

    ---

22. A new team member has just created a new project in GCP. What role is automatically granted to them when they create the project?

        a). roles/viewer
        b). roles/browser
        c). roles/editor
        d). roles/owner

        Correct: d

        Explanation:
            When you create a project, you are automatically granted the roles/owner role. The owner role
            includes permissions granted by roles/editor, roles/viewer, and roles/browser.
    Reference: <a target="_blank" href=https://cloud.google.com/resource-manager/docs/access-control-proj>https://cloud.google.com/resource-manager/docs/access-control-proj</a>

    ---

23. As a developer using GCP, you will need to set up a local development environment. You
will want to authorize the use of gcloud commands to access resources. What commands
could you use to authorize access?

        a). gcloud config login
        b). gcloud auth login
        c). gcloud login
        d). gcloud init

        Correct: b, d

        Explanation:
            Gcloud init will authorize access and perform other common setup steps. Gcloud auth login will
            authorize access only. Gcloud login and gcloud config login are not valid commands.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/docs/initializing>https://cloud.google.com/sdk/docs/initializing</a>

    ---

24. A data warehouse administrator is trying to load data from Cloud Storage to BigQuery.
What permissions will they need?

        a). bigquery.tables.create
        b). bigquery.jobs.create
        c). bigquery.tables.list
        d). bigquery.jobs.list
        e). bigquery.tables.updateData

        Correct: a, b, e

        Explanation:
            To load data, an identity must have bigquery.tables.create, bigquery.tables.updateData, and
            bigquery.jobs.create. bigquery.tables.list is needed to list tables and metadata on tables.
    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/batch-loading-data>https://cloud.google.com/bigquery/docs/batch-loading-data</a>

    Reference: <a target="_blank" href=https://cloud.google.com/bigquery/docs/access-control>https://cloud.google.com/bigquery/docs/access-control</a>

    ---

25. A startup has created an IoT application that analyzes data from sensors deployed on
vehicles. The application depends on a database that can write large volumes of data at low
latency. The startup has used HBase in the past but want to migrate to a managed database
service. What service would you recommend?

        a). Cloud Spanner
        b). Bigtable
        c). Cloud Dataproc
        d). BigQuery

        Correct: b

        Explanation:
            Bigtable is a wide column database with low latency writes that is well suited for IoT data
            storage. BigQuery is a data warehouse service. Cloud Dataproc is a managed Spark/Hadoop
            service. Cloud Spanner is a global-scale relational database designed for transaction processing.
    Reference: <a target="_blank" href=https://cloud.google.com/bigtable/docs/schema-design>https://cloud.google.com/bigtable/docs/schema-design</a>

    Reference: <a target="_blank" href=https://cloud.google.com/bigtable/docs/schema-design-steps>https://cloud.google.com/bigtable/docs/schema-design-steps</a>

    ---

26. You have created a set of firewall rules to control ingress and egress traffic to a network.
Traffic that you intended to allow to leave the network appears to be blocked. What could
you do to get information to help you diagnose the problem?

        a). Enable Cloud Monitoring of each firewall rule
        b). Use Cloud Debugger to debug the firewall rules
        c). Enable firewall rule logging for each of the firewall rules
        d). Enable Cloud Trace of each firewall rule

        Correct: c

        Explanation:
            Firewall rule logging can be enabled for each firewall rule. Each time the rule is applied to allow
            or deny traffic, a connection record is created. Connection records can be viewed in Cloud
            Logging. Cloud Monitoring is used for collecting and view metrics on resource performance.
            Cloud Trace is used to understand performance in distributed systems. Cloud Debugger is used
            by developers to identify and correct errors in code. 
    Reference: <a target="_blank" href=https://cloud.google.com/vpc/docs/firewall-rules-logging>https://cloud.google.com/vpc/docs/firewall-rules-logging</a>

    ---

27. A Cloud Storage user wants to rename several files in a bucket. What command should they use?

        a). gsutil mv
        b). gsutil cp
        c). gsutil rename
        d). gsutil rn

        Correct: a

        Explanation:
            To rename a file in cloud storage, use the move command gsutil mv. Gsutil cp will copy files,
            not rename them. Gsutil rewrite and gsutil rn are not a valid command. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/gsutil/commands/mv>https://cloud.google.com/storage/docs/gsutil/commands/mv</a>

    ---

28. Your organization has created multiple projects in several folders. You have been assigned
to manage them and want to get descriptive information about each project. What command would you use to get metadata about a project?

        a). gcloud describe projects <PROJECT_ID>
        b). gcloud projects describe <PROJECT_ID>
        c). gcloud describe projects <PROJECT_NAME>
        d). gcloud projects describe <PROJECT_NAME>

        Correct: b

        Explanation:
            The correct command is 'gcloud projects describe <PROJECT_ID'>. 'gcloud projects describe <PROJECT_NAME>'
            is incorrect because PROJECT_NAME is not used in this command.
            'gcloud describe projects' is wrong because 'describe' and 'projects' are in the wrong order in the
            command. 'gcloud describe project <PROJECT_NAME>' is incorrect because it uses PROJECT_NAME instead
            of PROJECT_ID.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/projects/describe>https://cloud.google.com/sdk/gcloud/reference/projects/describe</a>

    ---

29. A group of developers are creating a multi-tiered application. Each tier is in its own project.
The developer would like to work with a common VPC network. What would you use to implement this?

        a). Create routes between subnets of each project
        b). Create a VPN between projects
        c). Create firewall rules to load balance traffic between each project's subnets.
        d). Create a shared VPC

        Correct: d

        Explanation:
            A shared VPC allows projects to share a common VPC network. VPNs are used to link VPCs to
            on premises networks. Routes and firewall rules are not sufficient for implementing a common
            VPC. Firewall rules are not used to load balance, they are used to control the ingress and egress
            of traffic on a network. 
    Reference: <a target="_blank" href=https://cloud.google.com/vpc/docs/shared-vpc>https://cloud.google.com/vpc/docs/shared-vpc</a>

    Reference: <a target="_blank" href=https://cloud.google.com/composer/docs/how-to/managing/configuring-shared-vpc>https://cloud.google.com/composer/docs/how-to/managing/configuring-shared-vpc</a>

    ---

30. As a consultant to a new GCP customer, you are asked to help set up billing accounts.
What permission must an identity have in order to create a billing account?

        a). billing.create
        b). roles/billing.create
        c). roles/billing.accounts.create
        d). billing.accounts.create

        Correct: d

        Explanation:
            billing.accounts.create is the permission needed to create a billing account. billing.create is not a
            valid permission. Roles are sets of permissions but they are not permissions themselves so
            roles/billing.create and roles/billing.accounts.create are not correct answers. 
    Reference: <a target="_blank" href=https://cloud.google.com/billing/docs/how-to/manage-billing-account>https://cloud.google.com/billing/docs/how-to/manage-billing-account</a>

    ---

31. You have just created a custom mode network using the command: gcloud compute networks create.
You want to eventually deploy instances in multiple regions. What is the next thing you should do?

        a). Create subnets in regions where you plan to deploy instances
        b). Create firewall rules to load balance traffic
        c). Create subnets in all regions
        d). Create a VPN between the custom model network and other networks in the VPC.

        Correct: a

        Explanation:
            After creating a custom mode network, you will need to create subnets in regions where
            instances will be deployed. You do not have to create subnets in all regions but an instance
            cannot be deployed to a region without a subnet. Firewalls are used to control the ingress and
            egress of data, they are not used to load balance. VPNs are used to provide connectivity between
            Google Cloud and outside networks, such as an on premises network. 
    Reference: <a target="_blank" href=https://cloud.google.com/vpc/docs/using-vpc>https://cloud.google.com/vpc/docs/using-vpc</a>

    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/compute/networks/subnets/create>https://cloud.google.com/sdk/gcloud/reference/compute/networks/subnets/create</a>

    ---

32. A client of yours wants to deploy a stateless application to Kubernetes cluster. The
replication controller is named my-app-rc. The application should scale based on CPU utilization;
specifically when CPU utilization exceeds 80%. There should never be fewer than 2 pods or more
than 6. What command would you use to implement autoscaling with these parameters?

        a). kubectl apply rc my-app-rc --min=2 --max=6 --cpu-percent=80
        b). kubectl autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80
        c). gcloud containers apply rc my-app-rc --min=2 --max=6 --cpu-percent=80
        d). gcloud containers autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80

        Correct: b

        Explanation:
            The correct command is to use kubectl autoscale specifying the appropriate min, max, and cpu
            percent. Specifically: kubectl autoscale rc my-app-rc --min=2 --max=6 --cpu-percent=80. The
            other options are not valid commands. 
    Reference: <a target="_blank" href=https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale>https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale</a>

    ---

33. The contents of the a Cloud Storage bucket called free-photos-gcp are currently stored in
multiregional storage class. You want to change the storage class to nearline. What command would you use?

        a). gsutil rewrite -s nearline gs://free-photos-gcp
        b). gsutil migrate --from multiregional --to nearline gs://free-photos-gcp
        c). gsutil migrate -s nearline gs://free-photos-gcp
        d). gsutil rewrite -from multiregional --to nearline gs://free-photos-gcp

        Correct: a

        Explanation:
            The correct command for changing the storage class is gsutil rewrite with the target storage class
            and bucket specified. Gsutil migrate is not a valid command. There is no need to specify the
            parameters -from or -to.
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/gsutil/commands/rewrite>https://cloud.google.com/storage/docs/gsutil/commands/rewrite</a>

34. You have created a process that will run nightly. The process needs read and write access
to two Cloud Storage buckets. You do not want to use your identity to ensure the process has
sufficient privileges. How would you ensure the process can read and write to the Cloud Storage buckets?

        a). Create a service account and grant it a role that provides read and write permission.
        b). Create a federated identity and grant it permissions directly to enable read and write access.
        c). Create a service account and assign permissions directly to enable read and write access.
        d). Create a Cloud Identity and grant it a role that provides read and write permissions.

        Correct: a

        Explanation:
            Service accounts are used to provide applications and instances with an identity that can have
            roles that give the identity sufficient permission to execute operations it needs to perform.

35. You will be running an application that requires high levels of security. You want to ensure the 
application does not run on a server that has been compromised by a rootkit or other kernel-level malware.
What kind of virtual machine would you use?

        a). Hardened VM
        b). Shielded VM
        c). GPU-enabled VM
        d). Preemptible VM

        Correct: b

        Explanation:
            Shielded VMs are hardened virtual machines that use Secure Boot, virtual trusted platform
            module enabled Measured Boot, and integrity monitoring. Preemptible VMs can be taken back
            by Google at any time but cost significantly less than standard prices. Hardened VM is not a
            valid option in Compute Engine. GPU-enabled VMs can improve the performance of compute
            intensive applications, such as training machine learning models. 
    Reference: <a target="_blank" href=https://cloud.google.com/security/shielded-cloud/shielded-vm>https://cloud.google.com/security/shielded-cloud/shielded-vm</a>

    ---

36. Your company is migrating an on premises archive of files to Google Cloud. The archived files are
infrequently used but on average about once every 30 days. You would like to minimize the cost of storage.
What storage option would you recommend?

        a). Nearline Storage
        b). Coldline Storage
        c). Multi-regional storage
        d). Persistent Disks

        Correct: a

        Explanation:
            Nearline Storage is a class of Cloud Storage designed for objects that will be accessed at most
            once every 30 days. Coldline Storage is suitable for objects accessed at most once per year.
            Multi-regional storage is best suited for objects that should have low latency access from
            multiple regions. Persistent disks should not be used for archival storage. 
    Reference: <a target="_blank" href=https://cloud.google.com/storage/docs/storage-classes>https://cloud.google.com/storage/docs/storage-classes</a>

    ---

37. You want to use Cloud Identity to create identities. You have received a verification record
for your domain. Where would you add that record?

        a). In the billing account for your organization
        b). In the domain's DNS setting
        c). In the metadata of each resource created in your organization
        d). In IAM settings for each identity

        Correct: b

        Explanation:
            Cloud Identity provides domain verification records, which are added to DNS settings for the
            domain. IAM is used to control access granted to identities, it is not a place to manage domains.
            The billing account is used for payment tracking, it is not a place to manage domains. Resources
            do have metadata, but that metadata is not used to manage domains. 
    Reference: <a target="_blank" href=https://cloud.google.com/identity/docs/verify-domain>https://cloud.google.com/identity/docs/verify-domain</a>

    ---

38. Your company has an on premises Hadoop cluster that is to be migrated to Google Cloud.
The CFO wants to minimize operational overhead. What GCP service would you recommend?

        a). Bigtable
        b). Cloud Dataproc
        c). Cloud Pub/Sub
        d). Cloud Dataflow

        Correct: b

        Explanation:
            Cloud Dataproc is a managed Spark/Hadoop service that can be used to migrate Hadoop clusters
            GCP. Cloud Pub/Sub is a queuing service that is used to ingest data and store it until it can be
            processed. Bigtable is a NoSQL database, not a queueing service. Cloud Dataflow is a stream
            and batch processing service, not a queueing service.
    Reference: <a target="_blank" href=https://cloud.google.com/dataproc/docs/how-to>https://cloud.google.com/dataproc/docs/how-to</a>

    ---

39. Your company has a complicated billing structure for GCP projects. You would like to set up multiple
configurations for use with the command line interface. What command would you use to create those?

        a). gcloud config configurations create
        b). gcloud config configurations set
        c). gcloud configurations set
        d). gcloud configurations create

        Correct: a

        Explanation:
            The correct command is gcloud config configurations create. Gcloud configurations crae, gcloud
            config configurations set, and gcloud configurations set are not valid gcloud commands to create
            configurations.
    Reference: <a target="_blank" href=https://cloud.google.com/sdk/gcloud/reference/config/configurations/create>https://cloud.google.com/sdk/gcloud/reference/config/configurations/create</a>

    ---

40. You have deployed a sole tenant node in Compute Engine. How will this restrict what VMs run on that node.

        a). Only VMs using the same operating system will run on that node.
        b). Only VMs from the same organization will run on that node.
        c). Only one VM will run on that node.
        d). Only VMs from the same project will run on the node.

        Correct: d

        Explanation:
            On a sole tenant node, only VMs from the same project will run on that node. They do not need
            to use the same operating system. Sole tenant nodes are not restricted to a single VM. VMs from
            the same organization but different projects will not run on the same sole tenant instance.
    Reference: <a target="_blank" href=https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes>https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes</a>

    ---

41. You want to run a Kubernetes cluster for a high availability set of applications. What type of cluster would you use?

        a). Multi-regional
        b). Single zone
        c). Regional
        d). Multi-zonal

        Correct: c

        Explanation:
            Regional clusters have replicas of the control plane while single zone and multi-zonal clusters
            have only one control plane. There is no such thing as multi-regional cluster. 
    Reference: <a target="_blank" href=https://cloud.google.com/blog/products/containers-kubernetes/best-practicesfor-
creating-a-highly-available-gke-cluster>https://cloud.google.com/blog/products/containers-kubernetes/best-practicesfor-
creating-a-highly-available-gke-cluster</a>
