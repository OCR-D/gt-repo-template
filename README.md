# 🔑 What must they do?

A template for the creation of a ground truth repo with the following functions and features: 
   - help for the creation of metadata for the Ground Truth Repo
   - guidelines for filing and organizing the Ground Truth Repo
   - automatic functions that control a github-action-workflow:
      - evaluation and generation of metadata in the formats.
         - METS (mets.xml)
         - JSON (metadata.json)
         - YML (metadata.yml)
      - generation of a GithubPage (ph) for the internet users e.g. https://OCR-D.github.io/gt_structure_1_1/
      - generation Releases
      - referenced your Ground Truth Repo in [HTR-United GT Record catalog](https://htr-united.github.io/catalog.html)


# 👷 👷‍♀️ How to use the template

### Step 1


* Create a repository for your ground truth data. Click on the [**Use this Template**](/../../generate) button.
* Save your data to the repository. Your data should be stored in the **Data folder**. See the **[Organization of folders and files in the Repo](https://github.com/OCR-D/gt-repo-template/blob/main/README.md#--organization-of-folders-and-files-in-the-gt-repo)**.
* The creation of a **README.md file is not necessary**.
* The **README.md file** is at first created automatically and can be expanded manually in **a subsequent step**.
* The **LICENSE.md** file should match the license of your data. Use [Choose an open source license](https://choosealicense.com/non-software/) to assign the suitable license.  

### Step 2

* **Create metadata** data for your ground truth dataset.
* Metadata is necessary to ensure that your repository is **correctly documented**. Use the **[metadata form](https://tboenig.github.io/gt-metadata/document-your-gt.html)** to record the metadata correctly.


### Step 3

- The template contains tools that automatically create specific web pages from the stored metadata and ground truth data. You can publish these as GitHub pages. What do you do for this.
   1. The analysis we started through a tag. see **[How to start the automatic functions?](https://github.com/OCR-D/gt-repo-template/blob/main/README.md#-how-to-start-the-automatic-functions)**   
   2. Adjust the GitHub [page setting](/../../settings/pages). Select the [gh-pages branch](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) to do this.


### Step 4

* **After** creating the repository, saving and pushing the data and automatically analyzing the data with the Github workflow, you can customize the README.md file.   
* The README.md file is also created during the analysis. This contains the metadata, data about the corpus and a section extent part that you can customize.
* Do you want to **customize the README.md** file?
* In the **`<div id="extent">` section**, you can additions to the **README.md** file.
* You can find the **old version of README.md** file in the `readme_old` folder. The **current version of README.md** file can be found in the main branch.

<hr/>

# <a name="myfootnote1">🗉</a>  METS File

The **gt-repo-template** has the capability to generate METS files for GT data, involving an analysis of both the data structure and PAGE files. Despite the availability of this automated functionality, it is recommended to consider creating a custom METS file.

This METS file can contain various elements, including bibliographic and provenance data. It is essential to ensure compliance with the [OCR-D METS specification](https://ocr-d.de/en/spec/mets#requirements-on-handling-metspage). 

It's important to note that referencing PAGE files using URLs/URIs is not permitted. PAGE files should be stored in the repository and referenced within the METS file as follows:
```xml
<mets:FLocat xlink:href="GT-PAGE/[optional folder]/[PAGE-File.xml]" LOCTYPE="OTHER" OTHERLOCTYPE="FILE"/>
```
The image file should either be referenced via a URL/URI in the METS file or, if the image files are stored in the repository, specified as a file reference in the METS file.
- URL/URI: 
```xml
<mets:FLocat xlink:href="https://opendata.uni-halle.de/retrieve/0775684d-82e9-4cb0-8e03-02f34c97949a/00000412.jpg" LOCTYPE="URL"/>
```
- File Reference:
```xml
<mets:FLocat xlink:href="GT-PAGE/[optional folder]/[image folder optional]/00000412.jpg" LOCTYPE="OTHER" OTHERLOCTYPE="FILE"/>
```

<hr/>


# <a name="myfootnote1">🗀</a>  Organization of folders and files in the GT-Repo

 The structure of the repo is the following:

```
├── METADATA.yml
├── LICENSE.md
└── data
      └── document_title or identifer
          ├── GT-PAGE
          └── mets.xml
          
 ```        
**Cached Image files:**
- In a separate directory.
- In the same directory as the text transcription (inside the GT-PAGE folder).

If you use your own METS file, the images must be referenced in it.

**Linked image files as URL/URI**:
- May be referenced in the transcribus PAGE file as a URL/URI.
Example:
``<TranscribusMetadata docId="1256538" pageId="50892347" pageNr="1" tsid="105748322" status="GT" userId="48446" imgUrl="https://files.transkribus.eu/Get?id=SFNIJNJBHWZPNRYZCAIWBJIA&amp;fileType=view" xmlUrl="https://files.transkribus.eu/Get?id=TWZJHYTDEPJDGTXDWJQAXHXH" imageId="27308940"/>`

If you use your own METS file, the images must be referenced in it.
- Can be referenced in the METS file as URL/URI
Example:
``<mets:FLocat xlink:href="https://opendata.uni-halle.de/retrieve/0775684d-82e9-4cb0-8e03-02f34c97949a/00000412.jpg" LOCTYPE="URL"/>``


## 🤖 How to start the automatic functions?

The github-action-workflow is triggered by assigning a version tag (e.g. `v1.8.11`) at push.
The version tag consists of **the lowercase letter `v`** (stands for version) and **a three-part numerical code**. 
Number code: e.g. `1.8.11`
The number code has the following meaning:
- the first number indicates the version number (1).
- the second number indicates the feature (8)
- the third number indicates the fixes, paths... (11)


# 📓 GT repo metadata
You can find metadata about the GT Repo in the following files.
   - mets.xml
   - metadata.json
   - metadata.yml
   - CITATION.cff

The content of the metadata files is the same, only the formats vary.
You can find the file at:

   - mets.xml 🠂 included in the zip file of the release
   - metadata.json 🠂 e.g.  https://github.com/OCR-D/gt_structure_1_1/blob/gh-pages/metadata.json and alternativ included in the zip file of the release
   - metadata.yml 🠂 e.g.  https://github.com/OCR-D/gt_structure_1_1/blob/main/METADATA.yml
   - CITATION.cff 🠂 e.g.  https://github.com/OCR-D/gt_structure_1_1/blob/main/CITATION.cff

            
           





  
