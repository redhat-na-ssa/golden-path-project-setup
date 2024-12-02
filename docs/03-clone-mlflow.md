## Clone MLFlow to your cluster

Using a terminal window, log into your openshift cluster. 



From the 'admin' menu option, choose 'Copy login command'.  

![](/images/copy-login-command.gif) <br><br>

A login screen will appear.  Click the 'rhsso' option.  

![](/images/choose-rhsso.gif) <br><br>

Login with your cluster username and password.

![](/images/rhsso-login.gif) <br><br>

After logging in, copy the 'oc login' token.

![](/images/copy-display-token.gif) <br><br>

Paste the token into your terminal window and press the 'enter' key.

![](/images/paste-token.gif) <br><br>

Press 'Y' to use the insecure connections? (y/n).  You are now logged into your openshift cluster, from your terminal window.

![](/images/press-Y.gif) <br><br>

In the terminal window, 'git clone https://github.com/redhat-na-ssa/mlflow-on-ocp' and follow the README. 

![](/images/git-clone.gif) <br><br>

In your terminal window, run the below README instructions.

![](/images/MLflow-readme.gif) <br><br>



<p align="center">Next, deploy the 'Golden Path'. &nbsp;
<a href="docs/02-deploy-service-mesh-rhoai.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/04-deploy-golden-path">Next</a>
</p>