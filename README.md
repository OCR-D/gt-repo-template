# 🔑 What does this repo template offer for You?

A template for the creation of a ground truth repo with the following functions and features: 
   - help for the creation of metadata for the Ground Truth Repo
   - guidelines for filing and organizing the Ground Truth Repo
   - automatic functions that control a github-action-workflow:
      - evaluation and generation of metadata in the formats.
         - METS (mets.xml)
         - JSON (metadata.json)
         - YML (metadata.yml)
      - generation of a GithubPage (ph) for the internet users e.g. https://tboenig.github.io/gt_structure_1_1/
      - generation Releases


## 🤖 How to start the automatic functions?

The github-action-workflow is triggered by assigning a version tag at push.
The version tag consists of a three-part number code.
Number code: e.g. 1.8.11
The number code has the following meaning:
- the first number indicates the version number (1).
- the second number indicates the feature (8)
- the third number indicates the fixes, paths... (11)


# 📓 GT repo metadata
You can find metadata about the GT Repo in the following files.
   - mets.xml
   - metadata.json
   - metadata.yml

The content of the metadata files is the same, only the formats vary.
You can find the file at:

   - mets.xml 🠂 included in the zip file of the release
   - metadata.json 🠂 e.g.  https://github.com/tboenig/gt_structure_1_1/blob/gh-pages/metadata.json and alternativ included in the zip file of the release
   - metadata.yml 🠂 e.g.  https://github.com/tboenig/gt_structure_1_1/blob/main/METADATA.yml


# 👷 👷‍♀️ How to use the template

### Step 1


* Create a repository for your ground truth data. Click on the [**Use this Template**](/../../generate) button.
* Save your data to the repository. Your data should be stored in the **Data folder**. See the Organization of folders and files in the Repo <b>[🗀](#myfootnote1)</b> 

### Step 2

* Metadata is necessary to ensure that your repository is documented correctly. It is best to use the <a href="https://tboenig.github.io/gt-metadata/document-your-gt.html" target="_blank" rel="noopener noreferrer">metadata</a> form to record the metadata.


### Step 3

* The template contains tools that automatically create specific web pages from the stored metadata and ground truth data. You can publish these as GitHub pages. 
   -  First, start the [analysis workflow](/../../actions/workflows/gtrepo.yml) and then adjust the GitHub [page setting](/../../settings/pages). Select the [gh-pages branch](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) to do this. 


### Step 4


* Customize the new readme file. 
* In the `<div id="extent">` section, you can additions to the README file

You can find the old readme file in the readme folder.

<hr/>

# <a name="myfootnote1">🗀</a>  Organization of folders and files in the Repo


**Images**: keep images in the same directory as the textual transcription (eg. GT-PAGE).

 The structure of the repo is the following:

```
├── METADATA.yml
├── LICENSE.md
└── data
      └── document_title or identifer
          ├── GT-PAGE
          └── GT-LINE
            
           

```




  
