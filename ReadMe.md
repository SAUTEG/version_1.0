```
               ######        ###       ##     ##    ########    ########     ######   
              ##    ##      ## ##      ##     ##       ##       ##          ##    ##  
              ##           ##   ##     ##     ##       ##       ##          ##        
               ######     ##     ##    ##     ##       ##       ######      ##   #### 
                    ##    #########    ##     ##       ##       ##          ##    ##  
              ##    ##    ##     ##    ##     ##       ##       ##          ##    ##  
               ######     ##     ##     #######        ##       ########     ######  

```

# SAUTAG English Document

![SAUTEG.Oryza sativa L](DataSet.jpg)

>Dataset picture display

## Project Introduction

&emsp;SAUTEG is an open agricultural pest and disease image dataset, and the project aims to provide an open agricultural pest and disease image dataset collection platform.

## Operating Instruction

You should understand the dataset file structure before using the project

### Directory Structure

```
//The names of crop species, pests and diseases involved should be given priority to Latin scientific names
SATEG
├─Oryza sativa L        //Latin scientific name for a crop species
│  ├─Diseases           //This folder is used to hold the diseases dataset of the crop
│  │  ├─!Phytophthora fragariae Hickm.var.oryzo-bladis Wang et Lu    //"!"The sign indicates that there are not enough samples
│  │  ├─Entyloma oryzae Syd
│  │  └─Fusarium moniliforme Sheld
│  └─Pests             //This folder is used to hold the Pets dataset of the crop
│      ├─!Ancyllomia japonica zeller
│      ├─Aleurocybotus indicus David et Subramaniam
│      ├─Ampullaria gigas Spix
└─Sample               //This folder is used to store the optimized pest and disease training samples
   └─Oryza sativa L.Pests     //One of the training samples,semi-colon separated crop species and sample type
        ├─test                //This is the test dataset folder
        │  ├─Aleurocybotus indicus David et Subramaniam
        │  └─Ampullaria gigas Spix
        |─train               //This is the train dataset folder
        |   ├─Aleurocybotus indicus David et Subramaniam
        |   └─Ampullaria gigas Spix
        └─README             //The documentation for the training sample should be described here when the dataset has been specially processed.
                             // For example by changing the default directory structure of the training sample document
                              
```

+ The names of crop species, pests and diseases involved should be given priority to **Latin scientific names**.
+ Folder name before `!` represents too few samples. <br>
Such as:<br>
`!Phytophthora fragariae Hickm.var.oryzo-bladis Wang et Lu //The sample is insufficient`
+ The folder of the Latin name of the crop in the root directory contains the original data of the crop, with `Diseases` holding the disease data and `Pets` holding the pest data.
+ Data in the `Diseases` and `Pets` folders should be classified as folders under Latin names.
+ The folder name `&` connects different kinds of data, which access similar diseases or pests. <br>
Such as:<br>
`Cletus punctiger&Clketus trigonus //This folder holds two types of familiar pests`
>In the use of this method, species have great similarity, there is no need to separate in the prevention view.

+ When the Latin name of some folders exceeds **the maximum length of GitHub**, the use of the acronym format, in the corresponding root directory has `README` file to explain. <br>
Such as:<br>
`H.S.2F.M` <br>
*The name of the folder that is too long after the merging of 5 kinds of acquaintance.Using the abbreviation form, create the `README` file in the root directory to explain.*
+ The `Sample` folder stores samples that can be used for training directly. The Sample folder name adopts the naming method of `cropName. Category`
+ The sample folder root may have a `README` file that describes the dataset sample

### Manual

#### Quick Start

&emsp;If you want to quickly build your recognition model, just find the pre-designed dataset in the `Sample` folder as needed, and the dataset has been named according to the `cropName. Category`.<br>
>*There may be a `README` file in the folder that explains the sample details*

#### Original Data

&emsp;The original data is stored in the root directory of the dataset with the crop Latin scientific name as the folder, and the `Diseases` folder holds the disease data and the `Pets` folder holds the pest data.


## Version History 

### version_1.0

+ updated rice pests and diseases.
+ Oryza sativa L.Pests training samples were added to the `Sample` folder.

## Upload Rules

You can upload and modify the project data, perfect the dataset, upload your dataset, or upload your carefully designed training sample.

Upload must according to **the directory structure requirements** and comply with **the following rules**:

1. Priority should be given to **Latin scientific name** for the names of crop species, pests and diseases involved.

2. If the sample quantity is too small, `!`should be added before the sample folder.<br>
For example:<br>
`!Phytophthora fragariae Hickm.var.oryzo-bladis Wang et Lu //The sample is insufficient`

3. The folder with the Latin scientific name of the crop in the root directory should contain the original data of the crop, with `Diseases` for disease data and `Pets` for pest data.Data in the `Diseases` and `Pets` folders should be classified as folders under Latin names.

4. You can use a folder to access several similar diseases and pests, different kinds of Latin scientific name application `&` division.<br>
For example: <br>
`Cletus punctiger&Clketus trigonus //This folder holds two types of familiar pests`
>In the use of this method, species have great similarity, there is no need to separate in the prevention view.

5. When the Latin name of the folder exceeds **GitHub's maximum length**, you can use the acronym format, should be in the corresponding root directory to create a `README` file to explain.<br>
For example: <br>
`H.S.2F.M` <br>
*The name of the folder that is too long after the merging of 5 kinds of acquaintance.Using the abbreviation form, create the `README` file in the root directory to explain.*

6. `Sample` folder stores samples that can be directly used for training, and the Sample folder name adopts the naming method of `cropName. Category`.

7. The `README` file can be created in the root directory of the sample folder to explain the dataset.<br>
&emsp;For example,changed the default directory structure of the training sample document or adopted a special dataset processing method.

## Copyright 

&emsp;SAUTEG aims to provide a public collection platform for agricultural pest and disease image datasets.The copyright of the project dataset is returned to the original author. If there is any infringement, please contact us to delete.The data of this project is only for research and other non-commercial purposes, and it shall not bear any legal liability for infringement caused by commercial use of any organization or individual.