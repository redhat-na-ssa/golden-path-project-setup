## Add Red Hat OpenShift AI and Service Mesh to your cluster

You will need to log into OpenShift.  From the Trusted Application Pipeline options, look for the Red Hat OpenShift option.  Use the displayed Console URL, and supplied Username and Password to log into OpenShfit.

![](/images/loginOCP.gif) <br>

Upon login, you should see an OpenShift dashboard.<br>

![](/images/OCPDashboard.gif) <br>

We will use this dashboard to install KServe and Red Hat OpenShift AI (RHOAI). 
 First, we will need to switch from 'All Clusters' to your 'local-cluster'.  
 
 In the upper left hand corner of the dashboard, click on the 'All Clusters' drop down.  Choose 'local-cluster'<br>

![](/images/Change2-localCluster.gif) <br>

Now you will be in 'your' local OpenShift cluster.

![](/images/your-local-cluster.gif)





<br><br>
Next, you will next need to clone MLFlow  

<p align="center">
<a href="docs/01-add-trusted-pipeline.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/03-clone-mlflow.md">Next</a>
</p>