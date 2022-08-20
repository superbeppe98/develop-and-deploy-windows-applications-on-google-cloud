[Back to Syllabus](/README.md#course-syllabus)

## Learning Objectives
- Understand how to deploy instances across Google Cloud zones
- Use instance groups to create pools of virtual machines
- Load balance Windows applications
<br>

## Configuring Resilient Workloads
The Google cloud provides tools for making
Windows applications highly available. Let's learn about how they work. >> In this module we'll look at how
to enhance the resilience of the web application created with
Microsoft ASP.NET MVC framework and deployed on Google compute engine. To do this we'll employ the Google
network load balancer and other supporting cloud platform resources. This diagram shows the typical
architecture that's used to ensure high availability of your Windows workload
when running on google cloud platform. This involves several different
resources zone, instance template, instance group, autoscalar,
load balancer and health checks. We'll take a closer look at each
of the Google resources over the next few slides but note that Windows resources should also be
deployed with high availability of mind. Google's georedundant architecture
is used to ensure high availability. You'll be able to provision
resources over multiple locations. Recall that Google currently has deployed
multiple regions in the United States, Europe and Asia,
with many more coming on stream. In each region, there are multiple zones. These have independent power and
network and ensure that even in the rare event of his own outage,
your application will continue to run. Should aim to deploy production
applications over multiple zones in a single region as a minimum
level of resiliency. With Windows infrastructure,
you'll want to duplicate Windows features such as
active directory in multiple zones and harness sequel server high availability
instances over multiple zones as well. The next three resources are important
if we need a scalable as well as highly available architecture. Together, they enable your
application to respond to increases in demand by provisioning
a set of machines to handle the load. The first of these is
the instance template. We've already created,
Google compute engine instances and seeing how we can configure
the virtual machine hardware with just the right amount of CPU memory and
disk selecting the appropriate Microsoft Windows server operating
system image to suit our requirements. An instance template allows nearly all
the same configuration options but doesn't create a machine. Instead, it serves as a specification
that can be used to create machines. The instance template works
together with the next resource, the managed instance group to
spin up a set of machines. To create a managements Group, first select a multi zone compute
engine region and an instance template. You can then pick a fixed number
of machines in the group, which will be distributed evenly across
the zones in the selected region. Alternatively, configure
auto scaling behavior and select a minimum a maximum
size of an auto scale pool. The autoscaler can direct the instance
group to create more machines when it determines that load has
exceeded a configured threshold. For example, if CPU usage is higher
than 70%, that the number of requests per second through the load balancer
is higher than the threshold or by using Google stack drivers,
standard or custom metrics. The auto scaling responds
quickly to demand changes and doesn't need any pre-warming. Similarly, when the load falls away, the autoscalar will shut down just
the right number of machines to ensure that all the policies
are under the configured limits. With a managed instance group you'll
also want to make sure that all the instances are working properly. You do this by configuring
health check resources. This makes http requests against
a URL path that you configure. The event of a series of ever responses. An instance will be marked as
unhealthy and automatically shut down. Health check can be simple,
is the home page for my application responding successfully for
example. Or it could be complex. A specific page that verifies
that all the back end resources are responding successfully. The final piece in the high
availability jigsaw is a load balancer. Google Cloud platform offers
multiple load balancers. Google Cloud platform offers
multiple load balances. There's a web load balancer for
http and https traffic and a separate network load balancer for
TCP and UDP traffic. A load balancer can be configured
with a single global IP address and traffic will be directed to the nearest
available set of instances as long as they have capacity. Google load balancers respond quickly to
traffic demand and need no pre-warming. One thing to note is that currently if
you've configured your ISP.net MVC web application to use integrated
Windows authentication, then you have to use
the network load balancer. The web load balancer isn't compatible
with Windows authentication.
<br>

## Hands-on Lab: Load Balance an ASP.NET Application
- Launch the Qwiklabs tool for open the Demo
    - Confirm the lab environment has been setup correctly
    - Install Microsoft Visual Studio 2015 Community Edition
    - Provision a second ASP.NET web server
    - Create a simple MVC application
    - Join the second web server VM to the domain
    - Modify the application and publish to IIS on the second VM
    - Configure the load balancer
<br>

[Go to Next Module](./5_Delivering_Next-Generation_ASP.NET_Core_on_Google_Cloud.md)
