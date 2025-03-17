### Steps to create Git Submodules


1. Create a new repository on GitHub
2. Clone the repository to the local machine
3. Add the submodule, where `repository_url` is the repository url and`directory_name` is the name of the folder where you want the sub-module to be saved (it must not exist in the project)
```
git submodule add <repository_url> <directory_name>
```
4. Add changes to the repository (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```
5. Initialize and update sub-modules, when someone clones the repository for the first time, they must run the following command to initialize and update the sub-modules
```
git submodule update --init --recursive
```
6. To update sub-module references
```
git submodule update --remote
```


## Importante
If you are working in the repository that has the sub-modules, **first update and push** the sub-module and **then** the main repository.

If done the other way around, references to submodules in the main repository will be lost and we will have to resolve conflicts.