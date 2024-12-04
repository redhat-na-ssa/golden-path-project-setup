## Add Red Hat OpenShift AI and Service Mesh to your cluster

Log into your OpenShift cluster

From the Trusted Application Pipeline options, look for the Red Hat OpenShift option.  Use the displayed Console URL, and supplied Username and Password to log into OpenShfit.

![](/images/loginOCP.gif) <br><br>

Upon login, you will see an OpenShift dashboard.<br>

![](/images/OCPDashboard.gif) <br>

We will use this dashboard to install Service Mesh and Red Hat OpenShift AI (RHOAI). 
 First, we will need to switch from 'All Clusters' to your 'local-cluster'.  <br><br>


 
 In the upper left hand corner of the dashboard, click on the 'All Clusters' drop down.  Choose 'local-cluster'<br>

![](/images/Change2-localCluster.gif) <br><br>

Now you will be in 'your' local OpenShift cluster.

![](/images/your-local-cluster.gif)<br>

Let's install the RHOAI Operator:  
1. From the 'Operators' menu:  choose 'OperatorHub' 
1. In the search field search for 'Red Hat OpenShift AI'
1. Select the "Red Hat OpenShift AI" placard to install RHOAI <br>


![](/images/install-RHOAI.gif)<br><br>

The 'Install' screen will appear.  Press 'Install' to begin the installation process.

![](/images/install-RHOAI2.gif)<br><br>

An 'Install Operator' screen will appear with default RHOAI options.  Keep the default options, and press 'Install' to continue the installation.<br>

![](/images/continue-RHOAI-install.gif)<br><br>

The RHOAI operator will begin to install.  Upon completion, next install the DataScience Cluster 'DSC' custom resource.  Press the 'Create DataScience Cluster' button to start the DSC installation.

![](/images/DSC-install.gif)<br><br>

The Create DataScience Cluster form will appear with default options.  Keep the default options, and press 'Create' to create the DataScience Cluster.

![](/images/create-DSC.gif)<br><br>

Notice that the DataScience cluster appears within the Red Hat OpenShift AI Operator details.

![](/images/DSC-details.gif)<br><br>

To check your RHOAI operator installation, from the left hand menu (of the OpenShift dashboard), choose 'Operators->Installed Operators'.  &nbsp; Search for the 'Red Hat OpenShift AI' operator.

![](/images/RHOAI-installed-operator.gif)<br><br>

Now that RHOAI Operator has been installed, you will need to install the Service Mesh operator.

1. From the 'Operators' menu: choose 'OperatorHub'
1. In the search field search for 'Service Mesh'
1. Select the "Red Hat OpenShift Service Mesh" placard to install Service Mesh <br><br>

![](/images/service-mesh.gif)<br><br>

An 'Install' screen will appear with default Red Hat OpenShift Service Mesh channel options.  Keep the default channel options, and press 'Install'.<br>

![](/images/install-service-mesh.gif)<br><br>

Next, an 'Install Operator' screen will appear with remaining Service Mesh options.  Keep the default options and press 'Install' to being the installation process.

![](/images/install-service-mesh2.gif)<br><br>

The operator will begin to install.  This will take a few minutes.  Wait for the installation to finish.

![](/images/install-service-mesh-msg.gif)<br>

![](/images/service-mesh-operator-ready.gif)<br><br>

Once the operator is installed, press the 'View Operator' button to view the operator.  

![](/images/view-service-mesh-op.gif)<br><br>

<p align="center">Next, you will next need to clone MLflow in your cluster. &nbsp;
<a href="docs/01-add-trusted-pipeline.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/03-clone-mlflow.md">Next</a>
</p>