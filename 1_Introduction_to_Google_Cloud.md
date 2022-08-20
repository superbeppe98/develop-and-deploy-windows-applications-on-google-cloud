[Back to Syllabus](/README.md#course-syllabus)

## Learning Objectives
- Understand the services in Google Cloud
- Create Windows VMs in Google Cloud
<br>

## What is Google Cloud?
Hi I'm Eoin Carroll, a Technical
Curriculum Developer in Google Cloud. What exactly is Google Cloud? How is
it organized? And what makes it unique? In this module, we'll
orient you in the basics, in this module, we'll introduce Google
Cloud with a particular focus on how the platform is an excellent place
to render your Windows workloads. Google has huge expertise
in running software at scale. You'll be familiar with Google Search,
Maps, Gmail, Google workspace, YouTube and Photos. These, and many more applications, are part
of everyone's day to day life through Google Chrome Browser and
Android cell phones. And now Google has shared its high-quality
infrastructure with the rest of us with Google Cloud. You'll be able to provision your virtual
machines in Google's data centers and connect them over Google's
private global fiber network. Google Cloud is a great place for
people who rely on Microsoft Server, operating systems and applications. You'll see how you can provision
Google Compute Engine, virtual machines with Microsoft Windows
Server and SQL Server, and run web applications meant for the .NET
platform on Internet Information Services. The concept of cloud computing
began with colocation. Instead of operating your own data center, you rented space in
the colocation facility. This was the first wave of outsourcing. With colocation, the transfer
of ownership was minimal. You still owned the machines and
you maintained them. Traditionally, colocation was not
thought of as cloud computing, but to begin the process of transferring IT
infrastructure out of your organization. Today, cloud computing involves
virtualized data centers, virtual machines and APIs.
Virtualization provides elasticity. You automate infrastructure
procurement instead of purchasing hardware. With virtualization,
you still maintain the infrastructure, it's still a user-controlled
user-configured environment. This is the same as an on-
premises data center. But now the hardware is
in a different location. Virtualization does provide
a number of benefits. The development teams can move faster. And you can turn capital expenses
into operating expenses. The next wave of cloud computing is
a fully-automated elastic cloud. This involves a move from the user-
maintained infrastructure to automated services. In a fully automated environment, developers do not need to think
about individual machines. The service automatically provisions and configures the infrastructure
used to run your applications. Google is uniquely positioned to propel
organizations into the next wave of cloud computing. Google's first product In Google Cloud,
App Engine, showed in 2008 that anybody could develop and deploy scalable, highly available web applications
without provisioning web servers. And many key Google products
today are low or no operations. In Google Cloud, all resources are
organized by projects that provide a container for
all of the products on the platform. You'll provision resources within
a project. And the project serves as an important identifier for billing and
management of users in groups. Resources within a project
are either global, regional, or zonal. Regions are independent geographic areas
that consist of zones. Locations within regions tend to have a round-trip network
latency of under five milliseconds. A zone is a deployment area for
Google Cloud resources within a region. It might help to think of this zone has
being similar to a logical data center with an independent power network. So zones should be considered a single
failure domain within a region. In order to deploy fault tolerant
applications with high availability, you should deploy your applications across
multiple zones in a region to help protect against unexpected failures. To protect against the loss of an entire
region due to a natural disaster, you should have a disaster recovery plan.
And know how to bring up your application in the unlikely event that
your primary region is lost. Google Cloud services and
resources can also be zonal, regional or managed by Google across multiple regions. Zonal resources operate in a single
zone. If a zone becomes unavailable, all of the zonal resources in that zone
are unavailable until service is restored. An example of a zonal resource is a Google
Compute Engine instance that resides within a specific zone. Regional resources are deployed
with redundancy within a region. This gives them a higher availability
relative to zonal resources. An example of a regional resource
would be a regional bucket for storing data in Google Cloud Storage. A few Google Cloud services are managed
by Google to be redundant and distributed within and across regions. For example,
buckets in the United States region for Google Cloud Storage, keep data
at REST inside the United States. But at REST state can be stored in or
moved to any Cloud Storage region within the United States. Google Cloud's
products and services can be broadly categorized as compute storage,
big data and machine learning. Leveraging compute can include virtual
machines via Compute Engine, running Docker containers in a managed platform
using Google Kubernetes Engine, deploying applications in a managed
platform like App Engine, running event-based serverless
code using Cloud Functions, or running stateless containers as
a managed service like Cloud Run. Many Google cloud storage products operate
at petabyte scale including Bigtable, a NoSQL key-value datastore,
Cloud storage for storing blob data, and Cloud Spanner, a horizontally scalable
SQL database with ACID transactions. Google's big data products
include BigQuery, which enables high performance analytics at
petabyte scale, Dataflow to run pipelines for
batch and real time transformation, and Pub/Sub to support your application
messaging requirements, all with NoOps. Finally, Google's machine learning
expertise is available via AI Platform to train your own machine learning models and
host the trained models from line or batch prediction, together with best
of breed APIs for analyzing images, text, audio, and video. From the perspective of managing Windows
workloads, each of the Google Cloud products is available via REST
APIs with client libraries. In addition, you'll be able to run your
applications on Google's compute family products. With Compute Engine
offering Windows Server, you'll have support for any Windows
application. For Google Kubernetes Engine, and App Engine. you'll be able to run Microsoft's new
.NET Core environment on Google services. As you'll see on the demo at the end
of this module, it's straightforward to access Google Cloud using a web browser,
and there are two primary techniques. First, the Cloud Console is an easy
to use web application where you can select a product using the Products and
Services menu, and then configure a server
using just a few clicks. Alternatively, there's a set of tools
available via Cloud Shell, a command prompt accessible from your web browser. You also can install the Cloud SDK locally
to run scripts from your own machine. Of particular interest to all of us who are
Windows systems operations professionals, is comprehensive support for
PowerShell for managing Google Cloud, including cmdlets to manage virtual
machines and a file system provider for Google Cloud Storage. We mentioned previously that on
Google Cloud, you always create projects to manage your resources. For
Google Cloud enterprise customers, there's an additional container,
the organization, which is created when you signed up with Google as
a Google Workspace customer. Each developer or systems operations professional will have
a login to access Google Cloud resources. There are a number of distinct options for
customers with Active Directory, including having separate
Google Workspace accounts, synchronized user names from Active
Directory by Google Cloud Directory Sync, passwords with Google Cloud
Password Sync, or single sign-on from Azure
to Google Workspace. Once your users are all set up, then they
log in to access the project resources. There is a flexible identity and access
management system that will enable you to configure role membership for groups
of users to enable them to just have the access levels that they
need to do their work.
<br>

## Hands-on Lab: Create a Windows Virtual Machine in Google Compute Engine
- Launch the Qwiklabs tool for open the Demo
    - Install Chrome RDP for Google Cloud Platform extension
    - Manually create a Windows VM
    - Connect to your Windows VM
    - Disconnect from your Windows VM
<br>

[Go to Next Module](./2_Windows_Workloads_on_Compute_Engine.md)
