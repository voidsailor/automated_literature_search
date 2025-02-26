[![DOI](https://zenodo.org/badge/732757380.svg)](https://zenodo.org/doi/10.5281/zenodo.10402352)

# Automated Literature Search

## Motivation

Finding the most relevant articles in a research domain! 🎯

This repo contains a [jupyter notebook](https://jupyter.org/) (automated_literature_search.ipynb) which queries PubMed based on keywords you provide and receives a list of articles. From these articles, all references are extracted and counted how often these references are cited among the initial articles. The references with the most citations are the (supposedly) most important articles for the research domain linked to your search keyword.

You can use this script to obtain an overview of one research domain.

We used the script to extract a list of potentially interesting articles for our literature review "Microbiome modeling: A beginner's guide" ([Frontiers in Microbiology](https://doi.org/10.3389/fmicb.2024.1368377)). The original literature search output files of this publication can be found in ["./review_query_outputs"](https://github.com/voidsailor/automated_literature_search/tree/main/review_query_outputs).

## How it works

1. Create a PubMed query. This query can be constructed according to the [PMC advanced search](https://www.ncbi.nlm.nih.gov/pmc/advanced) (e.g., "(microbiome) AND (computational model)" to query articles on computational modeling of microbiomes)
2. Retrieve a list of n articles for your query (we used 100 initial articles for our manuscript).
3. Collect all references of the initial **n** articles (**Notice: The script does only consider references of the initial articles**). The script counts how often each reference is cited in the initial **n** articles.
4. Represent all articles as a citation network. Each article is represented as a node. An edge between articles represents a citation. The number of incoming edges at a node (in **degree**) represents the number of citations of the corresponding article. The higher the in degree, the more citations.
5. An xlsx file is generated containing the list of initial and reference articles, their PubMed id, title, first author, year, doi, and degree (see below).
   An html is generated containing an **interactive network visualization** to explore the citation network (see below).

| pmid     | title                                      | first author | year | degree | doi                | is reference | references      |
| -------- | ------------------------------------------ | ------------ | ---- | ------ | ------------------ | ------------ | --------------- |
| 29171095 | The Gastrointestinal Microbiome: A Review. | Barko        | 2017 | 0      | 10.1111/jvim.14875 | False        | [25394236, ...] |
| ...      | ...                                        | ...          | ...  | ...    | ...                | ...          | ...             |

![Screen recording of an interactive network visualization](./interactive_graph.gif)

## How to install

### Execution in the browser using Google Colab

1. Create a Google account, log in, and open [google colab](https://colab.research.google.com).
2. Copy the URL to the jupyter notebook file to your clipboard (https://github.com/voidsailor/automated_literature_search/blob/main/automated_literature_search.ipynb).
3. In colab, click on "file", "open notebook", "GitHub" and paste the url.
4. Uncomment the code line in the first code cell and execute the script.

### Local installation using ANACONDA

1. Install the [ANACONDA Navigator](https://docs.anaconda.com/free/navigator/index.html).
2. Clone this repo with git or download the repo.
3. Open ANACONDA navigator, go to "Environments", "Import", Select the file "automated_literature_search.yaml" and click "Import". This will install all required dependencies locally. This may take a while.
4. Activate the environment by clicking on it, press the green "Play" button, and select "open with jupyter notebook"
5. The Jupyter file browser opens in your web browser. Navigate to the script (automated_literature_search.ipynb) and open it.

## How to use

1. [register at NCBI and get an API key](https://ncbiinsights.ncbi.nlm.nih.gov/2017/11/02/new-api-keys-for-the-e-utilities/).
2. Open the notebook (automated_literature_search.ipynb). Execute every code cell until you are at section 3 ("Execute Search")
3. Enter a query. We recommend doing a "dry run" on [PubMed](https://pubmed.ncbi.nlm.nih.gov/) to check the returned articles. Try different queries to determine the one with the best-fitting search results.
4. Define a prefix for output files.
5. Enter your NCBI credentials (These information are stored in the notebook, remove your credentials if you share or publish your script!)
6. Execute the search by running "get_articles_and_primary_references". Tweak the number of initially retrieved articles (parameter "number_of_initial_articles"). The higher, the more articles retrieved, the longer the search. The output xlsx is generated automatically.
7. Execute "build_graph" to create the interactive graph. You can open the generated html in any modern web browser.

## Dependencies

We use **pandas** for xlsx export, **networkx** to generate force-directed network layouts, **bokeh** for interactive figures. All dependencies are listed in the file "automated_literature_search.yaml".

## Publication
"Microbiome modeling: A beginner's guide" has been published in [Frontiers in Microbiology](https://doi.org/10.3389/fmicb.2024.1368377).
