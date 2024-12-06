## Install the MLFlow Plugin

Your plugin has been added to the example app in this repository, meaning you'll be able to access it by running yarn start in the root directory, and then navigating to /mlflow-frontend-dynamic. 

You can also serve the plugin in isolation by running yarn start in the plugin directory. This method of serving the plugin provides quicker iteration speed and a faster startup and hot reloads.
It is only meant for local development, and the setup for it can be found inside the /dev directory.

To install the mlflow plugin, you need to identify the project janus-idp-gitops in gitlab.

From the Trusted Application Pipeline, Log into GitLab.

![](/images/log-into-gitlab2.gif) <br><br>

From the 'Projects' page change into the 'gitops/janus-idp-gitops' directory.

![](/images/gitlab-projects-page.gif) <br><br>

Under janus-idp-gitops/charts/backstage/templates, replace dynamic-plugins-npmrc.yaml with TAPDemoChanges/dynamic-plugins-npmrc.yaml

![](/images/replace-file.gif) <br><br>


<BR><BR><BR>
Next, we will use the Golden Path Template.  

<p align="center">
<a href="docs/04-deploy-golden-path.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/06-using-golden-path.md">Next</a>
</p>