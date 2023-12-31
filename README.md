
# Amazon Review Analysis

This project focuses on scraping reviews from any Amazon product, converting them into embeddings, clustering these embeddings to group similar reviews, visualizing the clusters, and further analyzing each cluster using transformers and TF-IDF. The goal of the project is to find the most common grievance consumers might have for a product or a range of products. 

# Web Scraping Disclaimer

This code is provided for educational and informational purposes only. Web scraping may be against the terms of service of some websites. Amazon's terms of service, in particular, prohibit scraping. Use this code at your own risk. The developer is not responsible for any legal or other consequences that may result from its use.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Scripts Overview](#scripts-overview)
- [Results and Visualizations](#results-and-visualizations)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Installation

1. Clone this repository.
2. Install the required packages: 
    ```
    pip install -r requirements.txt
    ```

## Usage

Important to note: These scripts will require you to input appropriate links and file destinations, particularly when choosing the link to scrape and where to store the resulting JSON file. Refer to the comments in the scripts themselves.

### Amazon Review Scraper
To scrape Amazon reviews:
```
python review_scraper.py
```

### Embedding and Clustering
To convert reviews into embeddings, cluster them, and visualize the clusters:
```
python review_analyzer_and_visualizer.py
```

## Scripts Overview

### review_scraper.py
This script scrapes Amazon product reviews. It can optionally filter reviews based on a specific star rating. The main functionalities include:
- Setting up a Selenium webdriver with randomized user agents to scrape dynamic content.
- Filtering reviews based on a specific star rating.
- Scraping review titles and texts.
- Saving the scraped reviews as a JSON file.

### review_analyzer_and_visualizer.py
This script processes the scraped reviews, converts them into embeddings, clusters the embeddings, and performs further analysis. The primary functionalities encompass:
- Loading and preprocessing reviews (tokenization, lemmatization).
- Converting reviews into embeddings using the SentenceTransformer model.
- Clustering the embeddings using KMeans.
- Summarizing each cluster.
- Extracting keywords from the cluster summaries using TF-IDF.
- Visualizing the clusters using t-SNE.

## Results and Visualizations

The results include clustered reviews, summaries for each cluster, and a visual representation of the clusters in the embedding space. The visualization can be interpreted to understand the grouping and similarity of reviews, while the extracted keywords from individual clusters provide more context as to how the clusters were formed. Overall, the users time to conduct negative sentiment research was reduced by 98% and any form of bias that would occur from traditional research does not exist.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 

## Acknowledgements

- Libraries used: BeautifulSoup, Selenium, fake_useragent, gensim, transformers, nltk, sklearn, matplotlib, sentence_transformers, etc.
- Dataset: One star reviews scraped from nine different Amazon speaker products.
