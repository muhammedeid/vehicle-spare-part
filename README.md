# End To End project to implement DevOps practices.
- I will use azure devops organization (azure repos , azure pipeline) and make project in your organization.

1. In the first you should clone source code from this repo or you can use directly Azure DevOps Demo Generator and create your project using Template if you clone source code use git bash to push your code in azure repos.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide2.PNG)

## 2. Now i will create Continuous Integration (CI) to Build my project and i will use azure pipeline for automated process.

2.1. In the first navigate to pipeline and create new.

2.2. Use the classic editor to create a pipeline without YAML.

2.3. Select a source code repos i select Azure Repos Git and select my Repository and branch.

2.4. Select Template to create tasks.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide3.PNG)

2.5. Now i will delete this tasks we don't need them.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide4.PNG)

2.6. In the first we will select the agent pool (Hosted-Azure Pipelines) and you can use your self hosted agent but first set the configration on your private host.

2.6.1. Then select image you will build in it (windows-2019)

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide6.PNG)

2.7. This is all Tasks we need it.

2.7.1. NuGet restore packages.

2.7.2. Build solution it use to build my .sln project and package my app.

2.7.3. Publish Artifact it publish my package to build Artifact and save it in drop.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide5.PNG)

2.8. We add Command Line Script task to make dir recursive and see path of package.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide7.PNG)

2.8.1. Then we can save and queue.

2.9. Then we see build log and see it build successfully.

![](https://github.com/muhammedeid/vehicle-spare-part/blob/main/assets/CI/Slide8.PNG)

## 3. Now i will create Continuous Deployment (CD) to deploy my web app.

3.1. I will navigate to azure pipeline to Releases and create new i will use Infrastructure as Code (Terraform) to deploy to azure cloud and i will use PaaS web app and sql server.

3.2. In azure devops you need to set some configration to make terraform integrate with azure portal. 

















