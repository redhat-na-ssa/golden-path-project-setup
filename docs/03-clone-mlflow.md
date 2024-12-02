## Clone MLFlow to your cluster

Using a terminal window, log into your openshift cluster. 



From the 'admin' menu option, choose 'Copy login command'.  

![](/images/copy-login-command.gif) <br><br>

A login screen will appear.  Click the 'rhsso' option.  

![](/images/choose-rhsso.gif) <br><br>

Login with your cluster username and password.

![](/images/rhsso-login.gif) <br><br>

After logging in, copy the 'Display Token'.

![](/images/copy-display-token.gif) <br><br>

In the page that appears, choose 'Log in with this token' option.  Copy the 'oc login command' and press enter.  Press 'Y' to use the insecure connections? (y/n)



You are now logged into your openshift cluster, from your terminal window.



In the terminal window, clone https://github.com/redhat-na-ssa/mlflow-on-ocp and follow the README. 




![](/images/loginOCP.gif) <br><br>


<p align="center">Next, deploy the 'Golden Path'. &nbsp;
<a href="docs/02-deploy-service-mesh-rhoai.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/04-deploy-golden-path">Next</a>
</p>