# Movie Mind

## Overview
Movie Mind is a movie recommendation system that utilizes a content-based algorithm to suggest films based on a user's preferences. The project preprocesses the IMDb dataset, applying a weighted rating formula to identify the top 250 movies. It further enhances the dataset by sanitizing it and creating a "soup" of relevant information, including cast, crew (directors), keywords, and movie overviews.

## Features
- **Weighted Rating Calculation**: Identify the top movies based on a weighted rating formula.
- **Data Sanitization**: Clean the dataset by removing unnecessary spaces.
- **Content-Based Recommendations**: Implement a content-based algorithm to recommend movies using fuzzy search on key features.
- **Interactive Visualization**: Explore the dataset interactively within a Jupyter Notebook.

## Weighted Rating Formula
### The weighted rating (WR) formula used in this project is defined as:

```python
def Weight_rating(x, m=m, C=C):
    v = x['vote_count']
    R = x['vote_average']
    WR = (v / (v + m) * R) + (m / (v + m) * C)
    return WR
```
```bash
Where:

𝑣 = v is the number of votes.
𝑅 = R is the average rating.
𝑚 = m is the minimum votes required to be considered.
𝐶 = C is the mean rating across all movies.
```
## Getting Started
### Prerequisites
```
To run this project, you will need:

Python 3.x
Jupyter Notebook
Necessary Python libraries (e.g., Pandas, NumPy, FuzzyWuzzy, etc.)
```

### Installation
### Clone the repository:
```bash
git clone https://github.com/yourusername/Movie-Mind.git
Navigate to the project directory:
cd Movie-Mind
Install the required libraries:
pip install -r requirements.txt
```

## Dataset
### The dataset used in this project is sourced from IMDb and includes detailed information on various films, including:

- **Movie title
- **Cast
- **Crew (directors)
- **Keywords
- **Overview
  
## Contributing
Contributions are welcome! If you would like to contribute, please fork the repository and create a pull request.

## Acknowledgments
- **IMDb for the dataset.
- **Jupyter and its community for providing a powerful interactive environment.
