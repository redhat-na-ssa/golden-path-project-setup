## Add and Deploy the Golden Path Template


In this section, we will log into Red Hat Developer Hub, in your cluster, and add the golden path template: https://github.com/redhat-na-ssa/ai-golden-path/blob/main/template.yaml

To log into your Red Hat Developer Hub instance, go back to your Trusted Application Pipeline home page.  Look for the Red Hat Developer Hub instance.

![](/images/start-developer-hub.gif) <br><br>

Using the provided URL, Username and Password, use 'Gitlab' to sign into your account.

![](/images/signin-with-gitlab.gif) <br><br>

![](/images/gitlab-login.gif) <br><br>

You will be asked to 'Authorize keycloak'.  Press the 'Authorize keycloak' button to continue.

![](/images/authorize-key-cloak.gif) <br><br>


Upon successful authorization you will enter the Red Hat Developer Hub Dashboard.

![](/images/developer-hub-dashboard.gif) <br><br>

Now we can create the Golden Path Template!  

Select the 'Create' option from the Developer Hub menu.  The 'Software Templates' dashboard option will appear.  Then click the 'Register Existing Component' button

![](/images/create-register.gif) <br><br>

Use the git URL of the Golden Path Template:  https://github.com/redhat-na-ssa/ai-golden-path/blob/main/template.yaml, and enter that into the 'Select URL' text box and then press the Analyze button

![](/images/golden-path-template-git-url.gif) <br><br>

Developer Hub will analyze the template to determine if it can be imported into the catalog.  Once the template is verfied, press the 'Import' button to import it into the catalog.

Note:  if you have already imported the template (in a previous session), you would see a 'Refresh' button which you would press instead.

![](/images/import.gif) <br><br>

Once the template is registered, choose the 'Create' menu option.  The dashboard will display available templates, including the 'AI Template' which you just created.  Click the 'Choose' button to continue.

![](/images/choose-AITemplate.gif) <br><br>

In your AI Template, provide information about the AI Component.

Add a Project Name (it will automatically default to 'ai-app') and Description.  Then press the 'Next' button.

![](/images/ai-component-info.gif) <br><br>

Next, provide Cluster and Image Registry Information.  Copy the apps.cluster url.  Make certain that it contains the 'opentlc.com' ending.  This is your 'Cluster Host Root' URL.  Replace the current .apps.cluster.com URL which is currently entered.

![](/images/change-url.gif) <br><br>


Click on the 'Image Registry*' text, it will change to 'OpenShift' and automatically populate it's location.  

Note:  if you still only see 'OpenShift' with no 'Image Host' and 'Image Tag' information, double click the OpenShift text to make the default settings appear.  Then press the 'Next' button to continue.

![](/images/image-registry.gif) <br><br>


Next, provide the 'Application Repository Information'.  The Repo Host will be the gitlab instance URL. 

![](/images/repo-host-url.gif) <br><br>

 You can find this URL back in the Trusted Application Pipeline details page.  

![](/images/gitlab-url.gif) <br><br>

Copy the entire URL and paste it into Repo Host url text box.







	The Cluster Host Root will look something like this: ".apps.cluster-9dqks.9dqks.sandbox413.opentlc.com"
	The Repo Host will look something like this: "gitlab-gitlab.apps.cluster-9dqks.9dqks.sandbox413.opentlc.com"
		Notice this does NOT have the leading https://

<p align="center">
<a href="docs/03-clone-mlflow.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/05-using-golden-path.md">Next</a>
</p>