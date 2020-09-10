# Azure Policies As Code  
##### [This repo contains all Azure policies for ZenithWorks Organization]

#### Why do we manage Azure policies as code?:
* **Maintain Change History**: Your Azure policy definitions and Assignments are now version controlled. You can see what changes are done, when they were done and who did it.
* **Better Collaboration:** You can collaborate with multiple stakeholders when you raise pull request for changes. You can add approvers for your PRs as well.
* **Safe Deployments through Workflows**: You can follow safe deployment practices for rolling out new policies using GitHub workflows and actions. Check out [Manage Azure Policy Action](https://github.com/marketplace/actions/manage-azure-policy) and [Compliance Scan Action](https://github.com/marketplace/actions/azure-policy-compliance-scan).


#### Best Practices to follow while creating or updating policies:
* Export the existing policies from Azure Portal using the Export button.
* With export a sample workflow file is also generated. You can use the same or customize it based on your needs.
* Only export policies for your resource group and subscriptions.
* If you are not sure of the export changes, export it to a separate branch and raise a pull request to the desired branch.

#### Designing policy as code workflows

As you progress on your journey with Cloud Governance, you'll want to shift from manually managing each policy definition in the Azure portal or through the various SDKs to something more manageable and repeatable at enterprise scale. Two of the predominant approaches to managing systems at scale in the cloud are:
Infrastructure as Code: The practice of treating the content that defines your environments, everything from Azure Resource Manager templates (ARM templates) to Azure Policy definitions to Azure Blueprints, as source code.
DevOps: The union of people, process, and products to enable continuous delivery of value to our end users.

Policy as Code is the combination of these ideas. Essentially, keep your policy definitions in source control and whenever a change is made, test, and validate that change. However, that shouldn't be the extent of policies involvement with Infrastructure as Code or DevOps.

The validation step should also be a component of other continuous integration or continuous deployment workflows. Examples include deploying an application environment or virtual infrastructure. By making Azure Policy validation an early component of the build and deployment process the application and operations teams discover if their changes are non-compliant, long before it's too late and they're attempting to deploy in production.
