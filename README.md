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
   In Mac and linux, end of line are indicated with line feeds.<br>
      <img width="473" alt="{3334273A-DFBB-47D2-9669-C56C49A2E7CA}" src="https://github.com/user-attachments/assets/740e27ea-dde0-4610-a424-2d50137b16aa"><br><br>

   We need to set property called `core.autocrlf`.<br>
      <img width="468" alt="{FDC25E64-2EE9-426A-9CC4-4CA738F24AF1}" src="https://github.com/user-attachments/assets/4f1edbba-b5fc-47b0-acdb-e3928c91806b"><br><br>

  Command: For windows:<br> `git config --global core.autocrlf input`
           For Mac and Linux:<br> `git config --global core.autocrlf true`<br><br>

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

## Initilize Repository
Command: `git init`  
Result:  
<img width="660" alt="{9C67759D-DA8E-4A8C-94FA-866C3222FAEC}" src="https://github.com/user-attachments/assets/85895155-6fc6-46b9-8e08-4a68bdf6406f">  

Git stores info about the repo inside this folder which is hidden by default.  
Inside this folder:  
<img width="659" alt="{2BFDEB11-CB23-41FF-BF72-FA3913624B14}" src="https://github.com/user-attachments/assets/c8d08923-a0a1-4d4a-855e-37a1bf807fcf">  

## Basic Git Workflow
We first make changes to our project. We modify some files. When our project reaches a state which we want to record, we commit those changes into our repo. This is a **commit**. 
Creating a commit means taking a snapshot of our project.  
**Staging area** is the place where we will place our files which we are going to commit.  
Staging area will help us review our changes before making a commit.  
We have a couple of files in our repo.  
<img width="372" alt="{A6C7B550-8863-4103-9FF3-94E4CD9A3B37}" src="https://github.com/user-attachments/assets/f0cb7fa0-ec85-46bf-bed1-f86d78839bdf">  

We add these files to the staging area by using the add command.  
<img width="364" alt="{E3A28894-4862-43D9-8F41-709F8F2F24FD}" src="https://github.com/user-attachments/assets/e95e42c8-3966-4472-8ac8-24cc9c9332d1">  

<img width="344" alt="{401BC360-5C69-4120-AD50-DFD30995392D}" src="https://github.com/user-attachments/assets/c19e63ec-3a5e-4eea-a570-261eeb661c7f">  

This is the state we are proposing for the next commit.  
Then we use the commit command to permanently store these files on git repo.  
<img width="353" alt="{9FCF1D01-D65B-4B38-968E-4ECA9A5422A5}" src="https://github.com/user-attachments/assets/2ec7135b-c752-4789-bb2c-7645d2a0f725">  

We also supply a meaningful message.  
In the history, we can see all the commits.  
<img width="281" alt="{DC839974-B6B9-4503-9190-0C8E54D37FFF}" src="https://github.com/user-attachments/assets/a7612c2c-b7f8-44df-a396-6884761feb7c">  

Now, we make changes to file1 to fix some error. We add the file using add command.  
<img width="337" alt="{FF1E0D87-EFB5-4C3B-AD4C-E181CC63C6FE}" src="https://github.com/user-attachments/assets/85eb9452-7cbd-433d-8856-c2bcc09ac918">  

We now commit these changes to the repo using the commit command.  
<img width="349" alt="{518DD660-511A-4DD1-B998-98FD7CFEF599}" src="https://github.com/user-attachments/assets/aaac47ba-b721-4413-a94a-32b918e446e3">  

Each commit in git will have these details:  
<img width="271" alt="{53CCEEF9-E46D-4F1B-892F-FE504ED2359C}" src="https://github.com/user-attachments/assets/7e5c86ff-85c2-44af-bced-d6236009bf92">  

Git stores complete content of our project.  
<img width="399" alt="{C45723AE-BA58-4117-86C5-82F99638F186}" src="https://github.com/user-attachments/assets/180ef6c8-ffac-4cb7-b9b3-20df29a1f51c">  

### Staging Stages
Use `git status` to get the latest status of the git repo.  
<img width="609" alt="{B3B4DB07-C0F2-44C1-B89B-578F2D922D1A}" src="https://github.com/user-attachments/assets/2dc77970-335c-47a8-b256-7bfa4f2d7787">  

We have two untracked files. file1 and file2.  
They are red because they are not being tracked yet.  
To add to staging area, we use `git add file1.txt file2.txt` or we can use `git add .` to add all files recursively.  
See the screenshot:  
<img width="587" alt="{E37D2741-E6D3-4A76-8D37-A52A41932828}" src="https://github.com/user-attachments/assets/35ea09ca-fea5-483f-843e-6d9b9e9d3523">  

Let us modify file1 and see what happens:  
Let us see the git status after modifing file1:  
<img width="520" alt="{6A527778-E386-4C66-A5A7-B4851C832953}" src="https://github.com/user-attachments/assets/5dc57aea-a50c-4741-861e-5b9c3c79e4b8">  

file1 has changes not staged yet.  
<img width="336" alt="{CF5E534A-2D4F-45EB-AE97-773F6A775A25}" src="https://github.com/user-attachments/assets/6492fb7d-f8cc-4bb0-9347-2c5876d68670">  

Let us use `git add file1` or `git add .` to add latest file1 to staging area.  
Git status:  
<img width="483" alt="{C9D1B3F7-80EE-42FC-B611-9BBB9D9EFE4B}" src="https://github.com/user-attachments/assets/233a495d-3c70-4cb4-90ad-dcfa1b2f86a1">  

### Commiting Changes  
Use commit command to commit changes:  
`git commit -m "Initial Commit"` or use `git commit`, the second command opens up a commit message file, where we can write longer commit messages.  
<img width="922" alt="{11BC9F8D-6AF8-44A7-9B7C-BAAB80F4D7A7}" src="https://github.com/user-attachments/assets/b66122a4-8b76-4945-afbf-89f52873d2a9">  

<img width="472" alt="{67A4D9EF-4460-48D3-BB33-D01433B82080}" src="https://github.com/user-attachments/assets/a216cc31-fb1a-461c-943a-754a822617cd">  

### Commiting Best Practices
<img width="469" alt="{ED623B89-042E-449F-8ADA-BDB952AC1860}" src="https://github.com/user-attachments/assets/6235b40b-fb1d-4b4a-8231-97e55698f28b">  

<img width="471" alt="{F1036261-756B-4994-A5AD-FB7D0291E201}" src="https://github.com/user-attachments/assets/d2529b2f-bb4e-4224-ba70-99a2ec81661e">  

Two commits for two different things:  
<img width="472" alt="{EA6400CC-19E1-4345-9A3C-FF4F790D6166}" src="https://github.com/user-attachments/assets/bb94653e-0dba-4399-86c3-01947933fbdf">  

Meaningful commit messages.  

### Skipping Staging Area
Modify file1 and commit in one go.  
Use command `git commit -a -m "This is direct commit"`, here -a means all and -m means message.  
Or you can combine them:  `git commit -am "This is direct commit"`.  

We can remove/delete a file from the working directory/folder as well as the staging area using this command:  
`git rm <file_name/s>`  

### Renaming or moving files
If we move or rename a file, we have to add them again using `git add` command.  
Or git also gives us a command: 
`git mv <old_file_name> <new_file_name>`  
This command will rename file in both directory and staging area.  
After this command the file will be renamed and added to the staging. We only need to commit changes after this.  

### Ignoring files or .gitignore file
We want to ignore files such as log files etc from committing to the repo.  
We can create a .gitignore file in our directory. We can put files names or folder names in this file. These files and folders will be ignored by git for tracking and committing.  
_Note: If you are already tracking a file and later on you add that file to .gitignore file then git is not going to ignore that._  


























































































