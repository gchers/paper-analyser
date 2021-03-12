# Paper analyser
The goal of this project is to enable quantitative analysis of 
academic papers. 

To achieve the goal, the project contains logic for

1. Parsing academic white papers into structured representation
1. Doing analysis on the structured representations

#### Paper dependency graph
The project as it currently stands focuses on the task of taking 
a list of arbitrary papers in the form of PDFs, and then creating
a dependency graph of citations amongst these papers. This graph
then shows how each of the PDFs reference each other. Paper analyser
achieves this by going through the steps:

1. Parse the papers to extract relevant data
   1. Read the PDF files to a format usable in Python
   1. Extract title of a given paper
   1. Extract the raw data of the "References" section
1. Parse the raw "References" section into individual refereces:
   1. Extract the title and authors of the citation
   1. Normalise the data of the extracted citations
1. Do dependency analysis based on the above citation extractions


## Usage 
To see example usage of a simple exmplae look at the [simple_example.md](/docs/simple_example.md)

Paper analyser takes as input PDF files of academic papers and outputs data about these papers. 
For convenience we maintain a list of links to software analysis papers
focused on software security in our sister repository [software-security-paper-list](https://github.com/AdaLogics/software-security-paper-list)

To see an example of doing analysis on many papers look at the explanation here [large_example.md](/docs/larger_example.md)

## Example visualisation

We have also created visualisations for the output of the paper 
analyser, which makes it very nice to rapidly understand the 
relationship between the academic papers in the data set. 

See a link here for an example of the visualisations
[https://adalogics.com/software-security-research-citations-visualiser](https://adalogics.com/software-security-research-citations-visualiser)

These visualistions will be open sourced in the near future.


Citation graph example:

![Alt txt](/example-images/paper-citation-graph.png)

## Installation
```
git clone https://github.com/AdaLogics/paper-analyser
cd paper-analyser
./install.sh
```

## Contribute
We welcome contributions. 

Paper analyser is maintained by Ada Logics, including: 
* [David Korczynski](https://twitter.com/Davkorcz)  
* [Adam Korczynski](https://twitter.com/AdamKorcz4)

We are particularly interested in features for:
1. Improved parsing of the PDF files to get better structured ouput out
1. More data analysis into the project


### Feature suggestions
If you would like to contribute but dont have a feature in mind, please see the list below for suggestions:

* Extraction of authors from papers
* Extraction of the actual text from the papers. This could be used for a lot of cool data analysis
