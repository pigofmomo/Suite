# Creating a new model repository.

1. If you are an OSP community member: create a model repository as described in step 3. 

2. Otherwise (in case you are **not** an OSP community member): post an Issue in the [Forum](https://github.com/Open-Systems-Pharmacology/Forum/issues) and ask to create an empty model repository for you. For this, please provide the information below (s. step 3 for the details). 

    * name of your model (e.g. *Midazolam*, check if already exists, otherwise use another name)
    
    * short description of the model repository (e.g. *Whole-body PBPK model of midazolam as CYP3A4 DDI victim drug*)
    
    * repository topics (e.g. *pbpk*, *pbpd*, *ddi*, *pediatrics*, ...)

    As soon as an empty model repository is created: continue with step 4.

3. Creating a model repository:
    * Please create **one repository per substance** (where possible)

    * Repository name: `<Substance>-Model` (e.g. `Midazolam-Model`)

    * Initialize Repository with Readme (see screenshot below)

    * (Optional) short description of the Repository           <br><br><img width="451" alt="UploadModel_02" src="https://user-images.githubusercontent.com/25061876/68377694-2a2d2c80-014b-11ea-8d0e-08cc856be755.PNG">

    * Define [Repository-topics](https://help.github.com/articles/classifying-your-repository-with-topics/):

      * Mandatory topic for model repositories: **osp-model**
      * Further topics: Optional. Topics are free text; however try to use predefined topics if available. Some predefined topics are:
        * *pbpk*
        * *pbpd*
        * *pk-sim*
        * *mobi*
        * *ddi*
        * *pediatrics*
<img width="292" alt="UploadModel_03" src="https://user-images.githubusercontent.com/25061876/68377845-5ea0e880-014b-11ea-83e4-70652f0ad519.PNG">

4. Create a so called *Fork* of the OSP Model repository. This will create your own personal copy of the OSP repository, where you can upload and modify files (this copy is still **public and visible to everybody**). S. https://guides.github.com/activities/forking/ for more details.

   <img width="496" alt="UploadModel_04" src="https://user-images.githubusercontent.com/25061876/68378146-e5ee5c00-014b-11ea-97c5-9dd77fcdbd4b.PNG">
   
5. To upload files in your fork, just click on the “upload files” button and select your
   local files (**[this works for files <=25 MB](https://help.github.com/en/github/managing-files-in-a-repository/adding-a-file-to-a-repository)**. For files between 25 and 100 MB [use the command line](https://help.github.com/en/github/managing-files-in-a-repository/adding-a-file-to-a-repository-using-the-command-line) )

   * If you need to *modify* a file: you can do it locally and simply upload the modified file version. It will automatically overwrite the previous version. <br><br>

6. Every model repository must contain project snapshots of all PK-Sim projects and ideally also the projects itself. Also a description of the repository in the **README.md** file (s. step 7.). E.g. <img width="422" alt="UploadModel_05" src="https://user-images.githubusercontent.com/25061876/68380417-159f6300-0150-11ea-9c18-661e0cfe2d97.PNG">

7. **README.md** is written in the _Markdown-Format_ (s. [here](https://guides.github.com/features/mastering-markdown) and [here](https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax) for details.). It can be edited directly on GitHub in your Fork of a model repository when you click on the Edit button.

    * A template is provided under [MODEL_REPO_README_TEMPLATE](MODEL_REPO_README_TEMPLATE.md). 

    * Copy the content of the template into your README.md and fill the description of the model and of the repository files and the list of references (e.g. where the model was published)

    * Some README examples
      * [Alfentanil-Model README](https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/blob/master/README.md)
      * [Glucose-Insulin-Model README](https://github.com/Open-Systems-Pharmacology/Glucose-Insulin-Model/blob/master/README.md)

8. When you are finished with uploading files and Readme in your fork of the model repository, you must create a so called [_Pull Request_](https://guides.github.com/activities/forking/#making-a-pull-request) (PR). This is so to say a proposal for the OSP to integrate your work back into the the original repository. For this, click on the “Code” tab first and then on “New pull Request”.
<img width="242" src="https://user-images.githubusercontent.com/25061876/68391340-b3eaf300-0167-11ea-9cd4-fd863b4b3a1e.PNG">

9. On the next page, click on "Create Pull Request".
<img width="637" src="https://user-images.githubusercontent.com/25061876/68391555-396ea300-0168-11ea-8841-b82a4f267fe3.png">

10. On the next page you can **optionally** select reviewers for your PR. Finally, click on “Create Pull Request” button.
<img width="514" alt="UploadModel_08" src="https://user-images.githubusercontent.com/25061876/68391844-c154ad00-0168-11ea-9b74-44265deae0d3.png">
Now somebody from the OSP maintainers team can integrate your work backt into the OSP (or ask you for changes if e.g. something needs to be modified before the PR can be accepted).

