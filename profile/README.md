# Overview 

TS Public Projects exist within three organizations:
* **UMCG-TS-Development** : While projects are still in development
* **UMCG-TS-Release** : Projects available for use and still supported
* **UMCG-TS-Archive** : Previously released projects/versions that are no longer actively supported

## Access

By default, accounts granted access to the organization have no permissions. To access repositories, accounts must either be added to a Team or granted individual access to a single repository. General access to TS Organizations is restricted. When creating a repository as a Member of the organization, the creating account is automatically given direct admin access over the repository. Access to additional members can be given by creating a new Team and assigning the appropriate level of access. 
> [!NOTE]
> If allowing teams access for specific projects, please see the documentation for [Repository Roles](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization) when granting permissions.

# Adding Existing Repositories 

If you wish to create a version of an existing repository, there are multiple ways to do so dependent on what the owner of the original repository has enabled. 

## Download ZIP 

This means downloading the files directly to your local machine. You can then create a repository using the steps above and place the downloaded files into it. 

## Template 

If a repository allows use as a template, it will have a button at the top right of its project main page: “Use this template.” This will open the repository creation page using the selected template as a new project. 

> [!WARNING]
> Creating a project from a template will separate it from the parent project completely. It will have no version or commit history. 

## Fork a Project 

Creating a fork of a repository preserves the commit data and allows the user to pull updates made from the original repository. This should be exercised with caution if the project will undergo significant changes from its source. 

>[!CAUTION]
>Transfer from Another Account/Org: <br>
>If you have permission to transfer a repository, this is an easy option. However, GitHub does not see this as "Creating” a repository and direct access permissions are not generated. To gain access after transferring a repository, it must be granted by an organization admin. 

# Setting Up Permissions 
To view access and grant permissions, go to the repository's Settings page and select Collaborators and teams. This gives an overview of current access to the project.

* **Base Role** : Everyone in the organization has this level of access. Default is No Permissions.
* **Direct Access** : People and teams granted access through the repository access page.
* **Organization Access** : People and teams whose access is based on their privileges within the organization. For example, Org_Write teams have write access to all projects within the organization. 

If the project has multiple people that require access, it can be more beneficial to set up a team specifically for the project (or multiple projects). In this instance, create a new team and assign it directly to the approprite repository. 
