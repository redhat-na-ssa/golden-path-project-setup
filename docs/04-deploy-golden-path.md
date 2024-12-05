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

Note:  do not copy the first part of the url:  https://

Leave the rest of the default options, and click the 'Review' button to continue.

![](/images/no-https.gif) <br><br>

All of the options you have entered, will now be displayed.  When you are done 'reviewing' the options you have chosen, click the 'Create' button.

![](/images/create-template.gif) <br><br>

The 'ai-template' starts being generated.  When it has finished generating, you will see 'check marks' appear for all of the generation stages:

1. Generating the Source Code Component
1. Publish
1. Generating Deployment Resources
1. Publishing to a Resource Repository
1. Create ArgoCD Resources
1. Register 

![](/images/ai-template.gif) <br><br>

Let's check if our 'ai-app' shows up as one of our components.  Choose the 'Catalog' menu option.  Upon selection, you should see the 'ai-app' in the 'Owned Components' list.

![](/images/owned-components.gif) <br><br>

Click the component Name 'ai-app'.  You will have a view where you can observe ai-app:
1. Links
1. Deployment summary
1. Merge requests statistics.<br><br>


![](/images/view-ai-app.gif) <br><br>


Next, we will install the MLFlow plugin into the Trusted Application Pipeline.  

<p align="center">
<a href="docs/03-clone-mlflow.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/05-install-mlflow-plugin.md">Next</a>
</p>

