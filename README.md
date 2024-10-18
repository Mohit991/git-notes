# Git-Notes
## Introduction to Version Control
Git is a version control system. A version control system records the changes made to our code over time in a special database called repository.  
We can look at our project history and see who has made what changes, when and why.  
<img width="470" alt="{116516C9-E889-431C-841B-98678080CA8D}" src="https://github.com/user-attachments/assets/33ed5c79-bc7a-47ca-a0de-ce510e30e55a">  

If something goes wrong, we can move back to an earlier state.  
Without a version control system, we will have to constantly store our entire project in various folders.  
<img width="469" alt="{C6366196-F8DD-4865-AE23-46C165B72D4A}" src="https://github.com/user-attachments/assets/41bad707-a906-4d2a-85b0-29601471d4ea">  

This is especially probelmatic when multiple people have to work on a single project.  
<img width="470" alt="{2C91C08B-EBA7-4BC0-B847-FEC0D1FDD3BC}" src="https://github.com/user-attachments/assets/1427d1e9-a208-48ef-a6ba-020bc056ce51">  

<img width="468" alt="{6AE8D1EA-A28E-439A-82A1-2B8F7A24B118}" src="https://github.com/user-attachments/assets/57437740-3778-4562-93f1-b0be19560408">  

## Types
<img width="467" alt="{53046ABD-E688-49AA-B2D9-9D945ED4BE87}" src="https://github.com/user-attachments/assets/0dbae807-66e5-4ffb-86c4-65b979ae95b9">  

### Centralized Version Control Systems
All team members connect to a central server to get the latest copy of the code and share changes with others. Subversion or Team Foundation Server are examples of centralized version control systems.  
<img width="469" alt="{0C017AA4-1BCC-4B51-BE91-8E1373D4C8D8}" src="https://github.com/user-attachments/assets/e37f5cdc-4ff0-4683-bfb1-cedfe4923f03">  

The problem with this system is single point of failure. If server goes down, the team cannot colleborate.  

### Distributed Version Control Systems
Each team member will have a copy of the project and its history on their own machine.  
So, we can save snapshots of our project locally on our machine.  
If central server is down, we can synchronize our work directly with others.
Git is an example of Distributed Version Control Systems.  
<img width="468" alt="{8110ED87-E60A-4321-809C-7388B16A2C33}" src="https://github.com/user-attachments/assets/566e664b-b069-4df3-b769-8d717ce83777">  

## Why Git? 
<img width="467" alt="{CEDBB274-6AD0-415F-8373-8097C01DF510}" src="https://github.com/user-attachments/assets/03c2e2b2-e4eb-408d-ab10-f7684ac460b0">  

## Using Git
<img width="467" alt="{EE7454CA-BA53-491C-B0DC-F74E7D37B2DA}" src="https://github.com/user-attachments/assets/f99fe592-4a0c-4526-a600-9d13d9a4294d">  

In VSCode:  
<img width="470" alt="{A1EA9380-D3EB-4684-B4FB-C81A42E198F6}" src="https://github.com/user-attachments/assets/f71ad34b-ab8e-4004-b1e3-9194a1c72588">  

For VSCode, most popular extension for Git features is GetLens.  
<img width="470" alt="{4FD63ADA-C052-4ED0-8BE4-95749C3F3639}" src="https://github.com/user-attachments/assets/4b0fd850-9327-41d9-878f-b8f945efbaf7">  

For GUI, we have git GUI clients:  
<img width="470" alt="{CC5645D6-28A1-48BA-B1A7-E484F465F7A2}" src="https://github.com/user-attachments/assets/fc7eb7da-3f07-4d57-97b9-7f4404b3e171">  

Another tool is GitKraken:  
<img width="476" alt="{62D6BE88-F0BB-4416-95B6-7501104DE436}" src="https://github.com/user-attachments/assets/eefdc2f9-a3fa-45d0-b56f-5e23bd662f50">  

Issues with GUI tools:  
<img width="470" alt="{01688375-A94C-4BD6-8B2C-DAE4A76B4ED6}" src="https://github.com/user-attachments/assets/2b67822c-11c0-42b2-9b78-5cfb08471cc3">  

## Installing Git
To see which git version you are using use below command on the terminal:  
`git -v`  
<img width="277" alt="{DE070AB1-F6FE-44D3-B510-7421F631753F}" src="https://github.com/user-attachments/assets/650a8e77-a3fe-4701-b7f8-1e374d95b9b6">  

## Configuring Git
First time we use git or later on also, we need to set some setting.  
We can specify settings at three levels:  
<img width="470" alt="{3824BD5D-D8FA-4E6B-BC0E-830B07B6D1ED}" src="https://github.com/user-attachments/assets/dc35d66a-981d-44ea-a0d1-abc0ae429f79">  

We need to specify below settings: 
1. Name: Setting the name of the user.
   Command: `git config --global user.name "<name>"`

2. Email: Setting the email of the user.
   Command: `git config --global user.email "<email>"`

3. Default Code Editor: Setting default code editor.
   Command: `git config --global core.editor "code --wait"`

4. End of Line: In windows end of line is marked in two ways. Line feed and carriage return.
   In Mac and linux, end of line are indicated with line feeds.
   <img width="473" alt="{3334273A-DFBB-47D2-9669-C56C49A2E7CA}" src="https://github.com/user-attachments/assets/740e27ea-dde0-4610-a424-2d50137b16aa">

   We need to set property called `core.autocrlf`.
   <img width="468" alt="{FDC25E64-2EE9-426A-9CC4-4CA738F24AF1}" src="https://github.com/user-attachments/assets/4f1edbba-b5fc-47b0-acdb-e3928c91806b">

  Command: For windows: `git config --global core.autocrlf input`
           For Mac and Linux: `git config --global core.autocrlf true`

The --global option allows you to configure settings that apply to all repositories you work with on your system. These settings are stored in a .gitconfig file in your home directory.  
We can edit the .gitconfig file using below command:  
`git config --global -e`  

## Getting Help
Command: `git config --help`
This gives complete information.  
If you just need a refresher. Use:
`git config --h`  

## Creating a directory  
Creating a directory:  
Command: `mkdir <folder_name/directory_name>`  
Getting into this directory.  
Command: `cd <folder_name/directory_name>`  



































