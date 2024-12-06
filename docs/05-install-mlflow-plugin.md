## Install the MLFlow Plugin

Your plugin has been added to the example app in this repository, meaning you'll be able to access it by running yarn start in the root directory, and then navigating to /mlflow-frontend-dynamic. 

You can also serve the plugin in isolation by running yarn start in the plugin directory. This method of serving the plugin provides quicker iteration speed and a faster startup and hot reloads.

It is only meant for local development, and the setup for it can be found inside the /dev directory.


## Installing the plugin in the TAP demo

To install the mlflow plugin, you need to identify the project janus-idp-gitops in gitlab.

The following files changes must be made in this gitrepo.

1) Replace the file `dynamic-plugins-npmrc.yaml` under `gitops/janus-idp-gitops/-/blob/main/charts/backstage/templates/dynamic-plugins-npmrc.yaml` with `TAPDemoChanges/dynamic-plugins-npmrc.yaml`

2) Update the file `gitops/janus-idp-gitops/-/blob/main/charts/backstage/backstage-rhtap-values.yaml?ref_type=heads` with contents from `TAPDemoChanges/backstage-rhtap-value-changes.yaml`

<BR>

## '1 - Replace the file'

From the Trusted Application Pipeline, Log into GitLab.

![](/images/log-into-gitlab2.gif) <br><br>

From the 'Projects' page change into the 'gitops/janus-idp-gitops' directory.

![](/images/gitlab-projects-page.gif) <br><br>

Under janus-idp-gitops/charts/backstage/templates directory, replace dynamic-plugins-npmrc.yaml 

![](/images/replace1.gif) <br><br>

with rhdh-mlflow-plugin-frontend/TAPDemoChanges/ dynamic-plugins-npmrc.yaml. 

Note:  that the TAPDemoChanges directory is in a different gitlab location:  https://gitlab.consulting.redhat.com/ai-odyssey-2025/na-hobbyists

![](/images/replace2.gif) <br><br>

The easiest way to replace the file, is to download the rhdh-mlflow-plugin-frontend/TAPDemoChanges/ dynamic-plugins-npmrc.yaml file onto your PC.

Then open the janus-idp-gitops/charts/backstage/templates/dynamic-plugins-npmrc.yaml file and select the 'Replace' button.

![](/images/replace3.gif) <br><br>

When the 'Replace dynamic-plugins-npmrc.yaml' file appears, select the 'upload' hyperlink.

![](/images/upload-file.gif) <br><br>

The File Manager will appear for your PC, select the dynamic-plugins-npmrc.yaml file that you downloaded earlier to your PC.

![](/images/select-file.gif) <br><br>

Once the file has been uploaded, select the 'Replace File' button.

![](/images/replace-file2.gif) <br><br>

Your file will be replaced.  Notice that the namespace 'backstage' has been added, and the data '.npmrc' content has changed.

![](/images/file-changes.gif) <br><br>

<BR>

## 2 - Update the File
 
From the Trusted Application Pipeline, Log into GitLab.

![](/images/log-into-gitlab2.gif) <br><br>

From the 'Projects' page change into the 'gitops/janus-idp-gitops' directory.

![](/images/gitlab-projects-page.gif) <br><br>


Under janus-idp-gitops/charts/backstage directory, update backstage-rhtap-values.yaml 

![](/images/replace-backstage-file.gif) <br><br>

with some of the contents of rhdh-mlflow-plugin-frontend/TAPDemoChanges/ backstage-rhtap-value-changes.yaml 

![](/images/replace-backstage-file2.gif) <br><br>

From backstage-rhtap-value-changes.yaml select lines 24-27 

![](/images/copy-file.gif) <br>

![](/images/copy-file-v2.gif) <br><br>

Then paste these changes (after line 229) into the Janus-idp-gitops/charts/backstage/ backstage-rhtap-values.yaml file

![](/images/paste-file.gif) <br>
![](/images/paste-file-v2.gif) <br><br>

Once you have copied the contents over, save the file Janus-idp-gitops/charts/backstage/ backstage-rhtap-values.yaml.


<br><br>
## For the entity to mlflow tab display the annotation needs to be there in  catalog-info.yaml
mlflow.org/experiment-name: <<Experiment Name from MLFLow>>   

<br><br>
<center>Next, we will use the Golden Path Template. &nbsp; </center><br>

<p align="center">
<a href="docs/04-deploy-golden-path.md">Prev</a>
&nbsp;&nbsp;&nbsp;
<a href="/docs/06-using-golden-path.md">Next</a>
</p>