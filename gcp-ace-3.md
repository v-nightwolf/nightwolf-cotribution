# Google Cloud Associate Cloud Engineer Practice Exam - 3:
---
These are top 50 GCP ACE(Google Cloud Platform Associate Cloud Engineer) certification practice questions/cheatsheet (GCP ACE exam dumps) for professionals who are aspired to be GCP ACE certified. You will find these GCP ACE questions and answers very helpful in your GCP-ACE certification and interviews. Prepare well and All the very best.
<br>

  All the [feedbacks and suggestions](https://nightwolf.in/contribute/) are most welocome.

---
 {!inpage-ads.md!}
---

1. You deployed a Python application to GCP App Engine Standard service in the us-central
region. Most of your customers are based in Japan and are experiencing slowness due to
the latency. You want to transfer the application from us-central region to asia-northeast1
region to minimize latency. What should you do?

        a). Create a new GCP project. Create a new App Engine Application in the new GCP project and
            set its region to asia-northeast-1. Delete the old App Engine application.
        b). Update the region property to asia-northeast1 on the App Engine application.
        c). Update the default region property to asia-northeast1 on the App Engine Service.
        d). Deploy a new app engine application in the same GCP project and set the region to asianortheast1.
            Delete the old App Engine application.

        Correct: a

        Explanation:
            App Engine is regional, and you cannot change an app's region after you set it. You can deploy
            additional services in the App Engine, but they will all be targeted to the same region.
    Reference: <a target="_blank" href=https://cloud.google.com/appengine/docs/locations>https://cloud.google.com/appengine/docs/locations</a>

    ---

2. You deployed a java application in a single Google Cloud Compute Engine VM. During
peak usage, the application CPU is maxed out and results in stuck threads which ultimately
make the system unresponsive, and requires a reboot. Your operations team want to
receive an email alert when the CPU utilization is greater than 95% for more than 10
minutes so they can manually change the instance type to another instance that offers more
CPU. What should you do?

        a). In Cloud Logging, create logs based metric for CPU usage and store it as a custom metric in
            Cloud Monitoring. Create an Alerting policy based on CPU utilization in Cloud Monitoring
            and trigger an email notification when the utilization exceeds the threshold.
        b). Link the GCP project to a Cloud Monitoring workspace. Configure an Alerting policy based
            on CPU utilization in Cloud Monitoring and trigger an email notification when the utilization
            exceeds the threshold.
        c). Write a custom script to monitor CPU usage and send an email notification when the usage
            exceeds the threshold.
        d). Link the project to a Cloud Monitoring workspace. Write a custom script that captures CPU
            utilization every minute and sends to Cloud Monitoring as a custom metric. Add an uptime
            check based on the CPU utilization

        Correct: b 

        Explanation:
            A Workspace is a tool for monitoring resources contained in one or more Google Cloud projects
            or AWS accounts. In our case, we create a Stackdriver workspace and link our project to this workspace.
    Reference: <a target="_blank" href=https://cloud.google.com/monitoring/workspaces>https://cloud.google.com/monitoring/workspaces</a>

    ---

3. Your company installs and manages several types of IoT devices all over the world. Events range
from 50,000 to 500,000 messages a second. You want to identify the best solution for ingesting,
transforming, storing and analyzing this data in GCP platform. What GCP services should you use?

    ![!image](../img/3-question.png)

        a). Cloud Pub/Sub for ingesting, Cloud Dataflow for transforming, Cloud Datastore for storing
            and BigQuery for analyzing the time-series data.
        b). Firebase Messages for ingesting, Cloud Pub/Sub for transforming, Cloud Spanner for storing
            and BigQuery for analyzing the time-series data.
        c). Cloud Pub/Sub for ingesting, Cloud Dataflow for transforming, Cloud Bigtable for storing
            and BigQuery for analyzing the time-series data.
        d). Cloud Pub/Sub for ingesting, Cloud Storage for transforming, BigQuery for storing and
            Cloud Bigtable for analyzing the time-series data.

        Coorect: c

        Explanation:
            For ingesting time series data, your best bet is Cloud Pub/Sub. For processing the data in
            pipelines, your best bet is Cloud Dataflow.
            That leaves us with two remaining options; both have BigQuery for analyzing the data. For
            storage, it is a choice between Bigtable and Datastore. Bigtable provides out of the box support
            for time series data. So using Bigtable for Storage is the right answer.
    ![!image](../img/3-solution.png)

    Reference: <a target="_blank" href=https://cloud.google.com/bigtable/docs/schema-design-time-series>https://cloud.google.com/bigtable/docs/schema-design-time-series</a>

    ---

4. You migrated an internal HR system from an on-premises database to Google Cloud
Compute Engine Managed Instance Group (MIG). The networks team at your company
has asked you to associate the internal DNS records of the VMs with a custom DNS zone.
You want to follow Google recommended practices. What should you do?

        a). 1. Provision the VMs with custom hostnames.
        b). 1. Create a new Cloud DNS zone and set its visibility to private. 2. When provisioning the
            VMs, associate the DNS records with the new DNS zone.
        c). 1. Install a new BIND DNS server on Google Compute Engine, using the BIND name server
            software (BIND9). 2. Configure a Cloud DNS forwarding zone to direct all requests to the
            Internal BIND DNS server. 3. When provisioning the VMs, associate the DNS records with
            the Internal BIND DNS server.
        d). 1. Create a new Cloud DNS zone and a new VPC and associate the DNS zone with the VPC.
            2. When provisioning the VMs, associate the DNS records with the new DNS zone.
            3. Configure firewall rules to block all external (public) traffic. 4. Finally, configure
            the DNS zone associated with the default VPC to direct all requests to the new DNS zone.

        Correct: b

        Explanation: 
            Our requirements here are Internal and Custom Zone. 
            You should do when you want internal DNS records in a custom zone. Cloud DNS gives you the
            option of private zones and internal DNS names.
    Reference: <a target="_blank" href=https://cloud.google.com/dns/docs/overview#concepts>https://cloud.google.com/dns/docs/overview#concepts</a>

    ---

5. An application that you are migrating to Google Cloud relies on overnight batch jobs that
take between 2 to 3 hours to complete. You want to do this at a minimal cost. Where should
you run these batch jobs?

        a). Run the batch jobs in a GKE cluster on a node pool with four instances of type f1-micro.
        b). Run the batch jobs in a GKE cluster on a node pool with a single instance of type e2-small.
        c). Run the batch jobs in a preemptible compute engine instance of appropriate machine type.
        d). Run the batch jobs in a non-preemptible shared core compute engine instance that supports
            short periods of bursting.

        Correct: c

        Explanation:
            Requirements - achieve end goal while minimizing service costs. 
            We minimize the cost by selecting a preemptible instance of the appropriate type. If the
            preemptible instance is terminated, the next nightly run picks up the unprocessed volume.

6. 
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>
    Reference: <a target="_blank" href=></a>

---
<br>
{!footer.md!}
