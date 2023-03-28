# Data-Engineering-Typical-Topics
![image](https://user-images.githubusercontent.com/70054118/228237253-e7a2b0fe-b71e-49ec-9eb5-db04b4b18629.png)

#####  Azure Data Factory – DEV to PROD

1. Changes on feature/XXX_name based on dev branch  (entorno ADF DEV)
![image](https://user-images.githubusercontent.com/70054118/228242297-f70bc7db-19f9-418d-ac71-ef6d8ee215bf.png)
2. After change, click on Save when working on feature/XXX_name (entorno ADF DEV)
3. Pull request from feature/XXX_name to DEV. (using DataFactory Repos on DevOps)
![image](https://user-images.githubusercontent.com/70054118/228242742-760b2ea1-1579-4195-a013-b836dd48461e.png)
4. Publish on dev branch in data factory dev
![image](https://user-images.githubusercontent.com/70054118/228242852-3a875f1d-c3ee-4dab-9943-ae61ba89a1f7.png)
![image](https://user-images.githubusercontent.com/70054118/228243022-160c3789-78b5-4243-8045-e8530f5f5eae.png)
![image](https://user-images.githubusercontent.com/70054118/228243093-578bee8a-e3e8-48a5-a271-5e0af2a0aef2.png)

  You will visualize some messages: publishing (“Deploying messages to the factory”)
  Click on ok box in “Pending changes”, you will see the ARM templates are created. 
5. Pull request from dev to main (using DF Repos on DevOps) in order to run ARM template 
  Check out that your changes are in main branch when ADF DEV
6. Go to Pipelines in Azure DevOps and run Build_ADF_ARM_Project_name. 
7. Go to Releases in Azure DevOps and create new release for “Deploy ADF Project_Name PROD”
![image](https://user-images.githubusercontent.com/70054118/228239782-06a4dd36-eddc-4bce-9793-ad8dfb002228.png)
![image](https://user-images.githubusercontent.com/70054118/228240385-aca6a9a4-36fb-4930-9b5e-985e6333162d.png)
  Check in Azure Data Factory Prod if your changes were correctly moved! Congratulations!
