# Data-Engineering-Typical-Topics
![image](https://user-images.githubusercontent.com/70054118/228252780-afd744fa-53aa-4181-90e8-b5000ae23412.png)


![image](https://user-images.githubusercontent.com/70054118/228251023-c7bd0e52-457c-4cc2-b509-a6deaa30a5c5.png)

##  CI/CD Azure Data Factory – DEV to PROD

1. Changes on feature/XXX_name based on dev branch  (entorno ADF DEV)
![image](https://user-images.githubusercontent.com/70054118/228242297-f70bc7db-19f9-418d-ac71-ef6d8ee215bf.png)
2. After change, click on Save when working on feature/XXX_name (entorno ADF DEV)
3. Pull request from feature/XXX_name to DEV. (using DataFactory Repos on DevOps)

![image](https://user-images.githubusercontent.com/70054118/228250419-5e47708b-dae0-4222-ae50-2b3b140bddcc.png)

4. Publish on dev branch in data factory dev

![image](https://user-images.githubusercontent.com/70054118/228244368-38d8e3d4-f5d4-4a10-b33a-a06617431be7.png)

  You will visualize some messages: publishing (“Deploying messages to the factory”)

  Click on ok box in “Pending changes”, you will see the ARM templates are created. 

![image](https://user-images.githubusercontent.com/70054118/228244477-52624e04-88a2-409b-a5e1-52821ca269e3.png)


![image](https://user-images.githubusercontent.com/70054118/228244919-cc968af1-6c96-4c5c-beaa-ef06636d98a4.png)

  
  
5. Pull request from dev to main (using DF Repos on DevOps) in order to run ARM template 
![image](https://user-images.githubusercontent.com/70054118/228245579-db38fa4e-3398-46cc-bd01-0fee1de68f80.png)

  Check out that your changes are in main branch when ADF DEV

![image](https://user-images.githubusercontent.com/70054118/228248926-a10edd62-d830-4ec6-9c5a-1515231c116b.png)

6. Go to Pipelines in Azure DevOps and run Build_ADF_ARM_Project_name. 

![image](https://user-images.githubusercontent.com/70054118/228247734-b2005bb0-df1b-4902-a3fa-c3f29ef3d8dd.png)

7. Go to Releases in Azure DevOps and create new release for “Deploy ADF Project_Name PROD”

![image](https://user-images.githubusercontent.com/70054118/228239782-06a4dd36-eddc-4bce-9793-ad8dfb002228.png)

![image](https://user-images.githubusercontent.com/70054118/228240385-aca6a9a4-36fb-4930-9b5e-985e6333162d.png)


Check in Azure Data Factory Prod if your changes were correctly moved! Congratulations!

![image](https://user-images.githubusercontent.com/70054118/228248748-c5667366-2396-491a-918a-44faaa9c4841.png)
