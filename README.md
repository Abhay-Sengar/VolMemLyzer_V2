
# VolMemLyzer-V2
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/) ![Static Badge](https://img.shields.io/badge/Tech_Stack-Volatility-red?link=https%3A%2F%2Fgithub.com%2Fvolatilityfoundation%2Fvolatility)


Memory forensics is essential in cybersecurity and digital forensics, especially for fighting advanced threats and malware. In this dynamic environment, memory analysis tools and methods must be efficient. By prioritising the prominent features in a memory, investigators can speed up their analysis.
The **VolMemLyzer** (Volatility Memory Analyzer) can extract over **250 features** from memory snapshots, speeding up analysis and enabling deeper explorations. It serves as a catalyst for memory forensics research and innovation.

The new VolMemLyzer-V2 is a tool based on **functional programming paradigm** with dependencies on updated Volatility3 Framework based on python 3.

## Extracted Features

The taxonoy of the features produced by VolMemLyzer which based on plugin structure is summarised below using this interactive sunburst chart:


![VolMemLyzerBurstGIF](https://drive.google.com/file/d/1ajkqJsfKdJWMR20tMD9xtV20d_kqBnTb/view?usp=drive_link)


## Pre-requisites

#### Volatility

For Linux, install **volatility** via apt:
```bash
  sudo apt install volatility 
```
For other Linux distributions, look for corresponding built-in software repositories, or install https://github.com/volatilityfoundation/volatility from source code.
#### Other Pre-requisites

Out of all libraries used, only **pandas** library is not part of the Python standard library and must be installed separately using pip via:
```bash
  pip install pandas
```


## Deployment

#### Step 1:
Complete pre-requisites and download the VolMemLyzer script from above to the desired folder. Navigate to the folder where the script was downloaded and initiate terminal/powershell in the folder.

#### Step 2:
Use the command given below:

```bash
  python3 VolMemLyzer-V2.py -f <Path to Memory Dump Folder> -o <Path to Output Folder> -V <Path to Volatility3>
```

The Placeholders should strictly follow:
- **Path to Memory Dump Folder** - This should be an absolute path to the folder containing memory dump files. Ex: */home/user1/Desktop/MemoryDumps*
- **Path to Output Folder** - This should be an absolute path to the folder where the *output.csv* is to be stored. Ex: */home/user1/Desktop/VolMemLyzerOutput*
- **Path to Volatility3** - This should be an absolute path to the *vol.py* file in the downloaded volatility folder from official Volatility3 Github. Ex: */home/user1/Desktop/Volatility3/vol.py*




## Improvements (V2 vs V1)


- Now supports 250+ features compared to less than 75 earlier.
- Supports latest Volatility 3 Framework rather than outdated Volatility 2 Framework.
- Now runs on python 3 rather than python 2.
- Improved redundancy - Exception handling support if dataframe is not created or incorrectly created.
- Improved computability with pandas.
- Scope of types of files supported increased.

NOTE: Future updates should include support for more third party plugins and better exception handling capabilities.


## Team Members
- [Arash Habibi Lashkari](https://github.com/ahlashkari): Founder and Project Owner
- [Abhay Pratap Singh](https://github.com/Abhay-Sengar): Researcher and Developer (VolMemLyzer-V2)


## Acknowledgements

This project has been made possible through funding from MITACS, Canada.
