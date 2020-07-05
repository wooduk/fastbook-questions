# fastbook-questions
> A tiny script to extract the end-of-chapter fastbook questions to their own notebooks.


This script extracts the end of chapter questionnaires from each of the chapter notebooks and puts them into their own notebooks with additional markdown cells where answers can be written. Also affords you the opportunity to add code cells for some answers.

My suggestion is you clone the [fastbook repo](https://github.com/fastai/fastbook) and run the script there to make your own copy of the questions for private use. 

The questions clearly remain copyright of Jeremy Howard and Sylvain Gugger. Please remember that the fastbook text (including all markdown cells in the notebooks and other prose) is not licensed for any redistribution or change of format or medium, other than making copies of the notebooks or forking this repo for your own private use. No commercial or broadcast use is allowed. 

This script was produced using [nbdev](https://github.com/fastai/nbdev).

## Install

```
pip install fastbook_questions
```

## How to use

Call `fastbook_extract` from the command line to extract all the questions to their own notebooks with cells for your answers.

With no arguments it will look for the fastbook chapters and produce outputs in the current directory.

### Optional Arguments

Use arguments to control where to look for inputs and put the outputs.

```
usage: fastbook_extract [-h] [--path PATH] [--save_path SAVE_PATH]
                        [--xtra XTRA]

optional arguments:
  -h, --help            show this help message and exit
  --path PATH           Path to book notebooks (default is current directory)
                        (default: None)
  --save_path SAVE_PATH
                        Path for saving output (default is current directory)
                        (default: None)
```

For example:
    
```
    fastbook_extract --path ~/fastbook --save_path ./fbq 
```

Will look for the fastbook chapters in ~/fastbook and save the output to a directory called fbq (which will be created if it doesn't exist).

