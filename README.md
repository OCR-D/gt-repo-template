### Step 1


* Create a repository for your ground truth data. Click on the [**Use this Template**](/../../generate) button.
* Save your data to the repository. Your data should be stored in the **Data folder**. See the Organization of folders and files in the Repo <b>[🗀](#myfootnote1)</b> 

### Step 2

* Metadata is necessary to ensure that your repository is documented correctly. It is best to use the <a href="https://tboenig.github.io/gt-metadata/document-your-data.html" target="_blank" rel="noopener noreferrer">metadata</a> form to record the metadata.


### Step 3

* The template contains tools that automatically create specific web pages from the stored metadata and ground truth data. You can publish these as GitHub pages. 
   -  First, start the [analysis workflow](/../../actions/workflows/gtrepo.yml) and then adjust the GitHub [page setting](/../../settings/pages). Select the [gh-pages branch](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) to do this. 


### Step 4


* Adapt the readme file. You can use the following paragraphs as a template.

<hr/>

# Title of your dataset

You can delete the following three paragraphs, they are just there to explain what's going on.

## License

To specify an appropriate license for the ground truth, please use the following information and notes.

:information_source:  Licensing a repository: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository

:information_source: Choose your licenses: https://choosealicense.com/

It is recommended to use a Creative Commons Zero v1.0 Universal license. 

## Description

Complete here

## Extent

Complete here

## Transcription guidelines

Complete here.

## Sources

Complete here.


________________

# <a name="myfootnote1">🗀</a>  Organization of folders and files in the Repo


**Images**: keep images in the same directory as the textual transcription (eg. GT-PAGE).

 The structure of the repo is the following:

```
├── METADATA.yml
├── LICENSE.md
└── data
      └── document_title or identifer
          ├── GT-PAGE
          ├── GT-ALTO
          └── GT-LINE
            
           

```




  
